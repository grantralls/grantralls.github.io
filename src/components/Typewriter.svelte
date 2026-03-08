<script lang="ts">
  class TypeWriter {
    private STRS = ["Fullstack Engineer", "Frontend to Infrastructure", "Book Worm"];
    private currWord = 0;
    private nextCh = 0;
    public display = $state("");
    private interval;

    constructor() {
      this.interval = setInterval(() => this.typeForward(), 80);
    }

    private typeForward() {
      if (this.display.length < this.STRS[this.currWord].length) {
        this.display += this.STRS[this.currWord].charAt(this.nextCh);
        this.nextCh++;
      } else {
        console.log("STOPPED");
        clearInterval(this.interval);
        const timeout = setTimeout(() => {
          this.interval = setInterval(() => this.typeBackward(), 80);
        }, 500);
      }
    }

    private typeBackward() {
      if (this.display.length > 0) {
        let newDisplay = this.display.split("");
        newDisplay.pop();
        this.display = newDisplay.join("");
      } else {
        clearInterval(this.interval);
        this.currWord = (this.currWord + 1) % this.STRS.length;
        this.nextCh = 0;
        this.interval = setInterval(() => this.typeForward(), 80);
      }
    }
  }

  const typeWriter = new TypeWriter();
</script>

<p>Grant Ralls | {typeWriter.display}</p>
