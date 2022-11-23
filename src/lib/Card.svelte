<script>
  export let title
  export let text
</script>

<div class="card">
  <h2>{ title }</h2>
  <p>{ text }</p>
</div>

<style>
  .card {
    padding: 1rem;
    border: 1px solid;
    border-radius: 6px;
  }

  .card h2 {
    margin-bottom: 1rem;
  }
</style>