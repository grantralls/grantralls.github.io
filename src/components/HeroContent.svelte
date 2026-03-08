<script>
  import {
    GithubIcon,
    LinkedinIcon,
    MailPlusIcon,
    NotepadTextIcon,
  } from "@lucide/svelte";
  import Typewriter from "./Typewriter.svelte";
</script>

<div class="relative z-10 flex h-full items-center justify-center text-center">
  <div>
    <!-- Hero -->
    <h1 class="text-4xl font-bold text-white text-left">
      <!-- Grant Ralls | Fullstack Software Engineer -->
      <Typewriter />
    </h1>
    <!-- CTA Cluster -->
    <div class="mt-4 flex flex-wrap justify-center gap-2">
      <button class="btn"><NotepadTextIcon size={16} />Resume</button>
      <button class="btn"><LinkedinIcon size={16} />LinkedIn</button>
      <button class="btn"><GithubIcon size={16} />Github</button>
      <button class="btn"><MailPlusIcon size={16} />Email</button>
    </div>
  </div>
</div>
