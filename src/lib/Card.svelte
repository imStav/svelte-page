<script>
  export let title
  export let tags = []
  export let text
  export let src
</script>

<div class="card">
  <h2>{title}</h2>
  <div class="inline-tags">
    {#each tags as tag}
    <span>#{tag}</span>
    {/each}
  </div>
  <p>{text}</p>
  <a href={src}>Read more</a>
</div>

<style>
  .card {
    max-width: 300px;
    padding: 1.5rem 1rem;
    border: 1px solid;
    border-radius: 6px;
  }

  .card h2 {
    margin-bottom: 1rem;
  }

  .card p {
    margin-top: 1rem;
    margin-bottom: 1.5rem;
  }

  .card a {
    text-decoration: none;
    color: whitesmoke;
    background-color: #00a2ff;
    padding: .5rem 1.5rem;
    border-radius: 100px;
  }

  .inline-tags {
    display: flex;
  }

  .inline-tags span {
    font-size: .9rem;
    margin-top: -.7rem;
    margin-right: 1rem;
    padding: .1rem 1rem;
    border-radius: 100px;
    filter: opacity(.7);
  }

  @media (prefers-color-scheme: dark) {
    .card {
      border-color: #ffffff49;
    }

    .inline-tags span {
      background-color: #ffffff49;
    }
  }

  @media (prefers-color-scheme: light) {
    .card {
      border-color: #00000049;
    }

    .inline-tags span {
      background-color: #00000014;
    }
  }
</style>