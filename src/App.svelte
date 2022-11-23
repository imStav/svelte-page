<script>
  import Card from './lib/Card.svelte'

  let ref = 'https://github.com/'
  let githubProfile = 'https://github.com/imStav'
</script>

<main>
  <h1 class="header">Svelte Page</h1>

  <div class="grid">
    <Card title={'Card title'} text={'lorem ipsum dolor sit amet consectetur'} />
    <Card title={'Card title'} text={'lorem ipsum dolor sit amet consectetur'} />
    <Card title={'Card title'} text={'lorem ipsum dolor sit amet consectetur'} />
    <Card title={'Card title'} text={'lorem ipsum dolor sit amet consectetur'} />
  </div>

  <!-- Replace with your content -->
  <p>
    Check out our <a href={ref} rel="noreferrer">Terms of Services</a>
  </p>

  <p class="credits">
    Made by <a href={githubProfile}>imStav</a> | Powered by Svelte & Vite
  </p>
</main>

<style>
  .header {
    margin-top: 2rem;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
    margin-block: 3rem;
  }

  .credits {
    color: #888;
  }
</style>
