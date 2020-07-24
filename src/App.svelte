<script>
  import Timer from './Timer.svelte'
  import HandTool from './HowTo.svelte'
  let audio;
  function timerEnds(e) {
	//   console.log(e) 
	  audio.play();
  }
</script>

<style>
  h1,
  h3 {
    text-align: center;
  }
</style>

<main>
  <h1>Handwashing App!</h1>
  <!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
  <Timer on:end={timerEnds}/>
  <HandTool />

  <audio bind:this={audio}>
  <source src="sound.mp3">
  </audio>
</main>
