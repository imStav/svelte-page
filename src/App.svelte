<script>
  import svelteLogo from './assets/svelte.svg'
  import Card from './lib/Card.svelte'

  let link = 'https://github.com/'
  let githubProfile = 'https://github.com/imStav'

  // Spread props method
  const props = {
    title: 'Card title',
    tags: ['tag'],
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    src: 'https://github.com/'
  }
</script>

<main class="border">
  <div class="header">
    <img src={svelteLogo} alt="Svelte Page logo">
    <h1 class="heading">Svelte Page</h1>
  </div>

  <div class="grid">
    <!-- Spread props method -->
    <Card {...props} />

    <Card 
      title={'Card title'} 
      tags={['tag', 'tag']}
      text={'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'} 
      src={'https://github.com/'}
    />

    <Card 
      title={'Card title'} 
      tags={['tag', 'tag', 'tag']}
      text={'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'} 
      src={'https://github.com/'}
    />

    <Card 
      title={'Card title'} 
      tags={['tag']}
      text={'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'} 
      src={'https://github.com/'}
    />
  </div>

  <!-- Replace with your content -->
  <p>
    Check out our <a href={link} rel="noreferrer">Terms of Services</a>
  </p>

  <p class="credits">
    Made by <a href={githubProfile}>imStav</a> | Powered by Svelte & Vite
  </p>
</main>

<style>
  main {
    max-width: 50%;
    margin-inline: auto;
  }

  .header {
    display: flex;
    margin-top: 2rem;
    place-items: center;
  }

  .header img {
    filter: saturate(1);
  }

  .heading {
    margin-left: 1rem;
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

  @media screen and (max-width: 1200px) {
    main {
      max-width: 60%;
    }
  }

  @media screen and (max-width: 1000px) {
    main {
      max-width: 70%;
    }
  }

  @media screen and (max-width: 780px) {
    .grid {
      grid-template-columns: repeat(1, 1fr);
    }
  }
</style>
