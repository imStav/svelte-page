<script>
  import svelteLogo from './assets/svelte.svg'
  import Card from './lib/Card.svelte'
  import Block from './lib/Block.svelte'

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

<main>
  <div class="header">
    <img src={svelteLogo} alt="Svelte Page logo">
    <h1 class="heading">Svelte Page</h1>
  </div>

  <hr>

  <div class="catchline">
    <h2>Our services</h2>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
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

  <div class="grid">
    <div>
      <h2>About</h2>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>

    <Block />
    <Block />

    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
  </div>

  <div>
    <!-- Replace with your content -->
    <p>
      Check out our <a href={link} rel="noreferrer">Terms of Services</a>
    </p>

    <p class="credits">
      Made by <a href={githubProfile}>imStav</a> | Powered by Svelte & Vite
    </p>
  </div>
</main>

<style>
  main {
    max-width: 40%;
    margin-inline: auto;
  }

  hr {
    border: 1px solid #ff390749;
    margin-bottom: 2rem;
  }

  .catchline h2 { margin-bottom: 1rem; }

  .header {
    display: flex;
    margin-block: 2rem;
    place-items: center;
  }

  .heading { margin-left: 1rem; }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
    margin-block: 3rem;
  }

  .grid h2 { margin-bottom: 1rem; }

  .credits { color: #888; }

  @media screen and (max-width: 1400px) {
    main { max-width: 50%; }
  }

  @media screen and (max-width: 1200px) {
    main { max-width: 60%; }
  }

  @media screen and (max-width: 1000px) {
    main { max-width: 70%; }
  }

  @media screen and (max-width: 900px) {
    main { max-width: 80%; }
  }

  @media screen and (max-width: 780px) {
    .grid { grid-template-columns: repeat(1, 1fr); }
  }
</style>
