<script>
  export let title
  export let text
</script>


<div class="about">
    <h2>{title}</h2>
    <p>{text}</p>
</div>

<style>
    .about h2{
        margin-bottom: 1rem;
    }

    .about p {
        filter: opacity(.9);
    }
</style>