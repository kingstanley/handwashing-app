<script>
  import Progressbar from './Progressbar.svelte'
  
  const totalSeconds = 20
  let secondsLeft = totalSeconds;
//   const incrementor = 100 / totalSeconds;
  $: progress = ((totalSeconds - secondsLeft) / totalSeconds) * 100;
let isRunning = false;
  function startTimer() {
      console.log("Starting timer");
      isRunning = true;
      
    let timer = setInterval(() => {
      secondsLeft -= 1;
    //   progress += incrementor;
      if (secondsLeft === 0) {
        clearInterval(timer);
        secondsLeft = totalSeconds;
        isRunning = false;
        progress = 0;
      }
    }, 1000)
  }
</script>

<style>
  h2 {
    margin: 0;
  }
  .start {
    background-color: rgb(154, 73, 73);
    width: 100%;
    margin: 10px 0;
    /* color: #fff;
    height: 20px; */
  }
  .start[disabled]{
      background-color: rgb(194, 194, 194);
      cursor: not-allowed;
  }
</style>

<Progressbar {progress} />
<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsLeft}</h2>
  <button bp="offset-5@md 4@md 12@sm" class="start" disabled={isRunning} on:click={startTimer}>
    Start
  </button>
</div>
