<style>
  .progress-container {
    margin: 20px 0;
    border: solid rgb(194, 194, 194) 1px;
  }
  .progress-bar {
    height: 30px;
    background-color: rgb(77, 199, 55);
  }
</style>

<script>
    export let progress = 20;
</script>

<div bp="grid">

  <div bp="offset-5@md 4@md 12@sm">
    <div class="progress-container">
      <div class="progress-bar" style="width: {progress}%" />
    </div>
  </div>
</div>
