<script>
  import {
    Blob,
    DotGrid,
    FilmGrain,
    LinearGradient,
    Liquify,
    Shader,
  } from "shaders/svelte";
</script>

<Shader class="absolute inset-0">
  <LinearGradient
    colorA="#be04cf"
    colorB="#0000f7"
    colorSpace="oklch"
    edges="mirror"
    end={{ x: 0.67, y: 0.28 }}
    start={{ x: 0.23, y: 0.7 }}
    visible={true}
  />
  <Blob
    blendMode="normal-oklch"
    colorA="#7835ff"
    colorB="#cd0ced"
    colorSpace="oklch"
    deformation={0.9}
    size={1}
    softness={2}
    speed={1}
  />
  <DotGrid blendMode="linearDodge" density={40} dotSize={0.05} opacity={0.15} />
  <Liquify decay={1} edges="mirror" intensity={2} radius={2} />
  <FilmGrain strength={0.09} />
</Shader>
