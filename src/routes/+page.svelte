<main>
  <header>
    <h1><img src="ricositelogo.png" alt="Ricochet Revival Logo" /></h1>
    <h1><b>Welcome to Ricochet Revival.</b></h1>
  </header>

  <section>
    <p>
      Ricochet is an officially made Half-Life modification created by Valve,
      released on November 1st, 2000. It was included as part of the 1.1.1.0
      update for Half-Life. It involves shooting discs and jumping around
      platforms in the void of space all with a futuristic aesthetic. Alas, it
      fell into obscurity, and became one of the many laughingstocks of Valve.
    </p>
    <p>
      But this time, we're returning to Ricochet to revive it once and for all,
      and see at least some interest for it come into the Valve community.
    </p>
    <p>
      But I hear ye ask; "who are you all?"<br />
      Well, simply put, we're a community for Ricochet, first launched in 2023.<br
      />
      Started as but a mere "haha wouldn't it be funny to play ricochet" gag, our
      purpose is to revive Ricochet, to some degree.<br />
      We think that Ricochet is very neat, and surprisingly fun, and there's still
      plenty to do with the game, even in these current years.<br />
      We have a server in the game, a Discord server, and a few other Ricochet-based
      things, such as a client plugin or two and a manual.<br />
      If you've ever wanted to check out Ricochet, why not check us out, too?
    </p>
    <p>
      Click on the links below for information, where we're found, and more!
    </p>
  </section>

  <section class="image-links">
    <figure>
      <a href="/manual"><img src="links/linksmanual.png" alt="Manual" /></a>
      <figcaption>
        <a href="/manual" style="font-family:seeds;">manual</a>
      </figcaption>
    </figure>
    <figure>
      <a href="https://discord.gg/GYuduTcDmg"
        ><img src="links/linksdiscord.png" alt="Discord" /></a
      >
      <figcaption>
        <a href="https://discord.gg/GYuduTcDmg" style="font-family:seeds;"
          >discord</a
        >
      </figcaption>
    </figure>
    <figure>
      <a href="contributors"
        ><img src="links/linksteam.png" alt="Contributors" /></a
      >
      <figcaption>
        <a href="contributors" style="font-family:seeds;">contributors</a>
      </figcaption>
    </figure>
    <figure>
      <a href="blog"><img src="links/linkblog.png" alt="Blog" /></a>
      <figcaption>
        <a href="blog" style="font-family:seeds;">blog</a>
      </figcaption>
    </figure>
    <figure>
      <a href="plugins"><img src="links/linkplugins.png" alt="Plugins" /></a>
      <figcaption>
        <a href="plugins" style="font-family:seeds;">plugins</a>
      </figcaption>
    </figure>
    <figure>
      <a href="serverlist"><img src="links/linkservers.png" alt="Servers" /></a>
      <figcaption>
        <a href="serverlist" style="font-family:seeds;">servers</a>
      </figcaption>
    </figure>
  </section>

  <section class="cta-links">
    <div>
      <img src="arrowanim.gif" width="10" height="10" alt="arrow gif" /><a
        href="https://steamcommunity.com/groups/ricorev"
        >Join our Steam Group!</a
      ><br /><br />
      <img src="arrowanim.gif" width="10" height="10" alt="arrow gif" /><a
        href="https://twitter.com/RicochetRevival">Check out our Twitter!</a
      ><br /><br />
      <img src="arrowanim.gif" width="10" height="10" alt="arrow gif" /><a
        href="https://store.steampowered.com/app/60/Ricochet/"
        >Don't have Ricochet? Buy it here!</a
      ><br /><br />
    </div>
  </section>

  <footer>
    <small class="small-text">
      website © the ricochet revival team<br />
      ricochet © valve corporation<br />
      ricochet revival is unaffiliated with valve corporation.
    </small>
    <h1><img src="ricositebottom.png" alt="Ricochet Revival Footer Logo" /></h1>
  </footer>
</main>

<style>
  @font-face {
    font-family: seeds;
    src: url(/SEEDS.TTF);
  }

  h1 {
    text-align: center;
    color: red;
    font-weight: bold;
    font-size: 2.2rem;
    margin-top: 20px;
    text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.7);
  }

  header,
  footer {
    width: 100%;
    text-align: center;
    padding: 20px 0;
  }

  header img,
  footer img {
    max-width: 300px;
    width: 100%;
    height: auto;
    margin: 20px 0;
  }

  section {
    padding: 20px;
    margin: 0 auto;
    max-width: 1000px;
    background: rgba(0, 0, 0, 0.5);
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.6);
  }

  section p {
    margin-bottom: 20px;
    font-size: 1.1rem;
  }

  .image-links {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    gap: 20px;
    justify-items: center;
    margin-top: 40px;
  }

  .image-links figure {
    text-align: center;
    margin-bottom: 20px;
    transition: transform 0.3s ease;
  }

  .image-links img {
    max-width: 160px;
    width: 100%;
    height: auto;
    border-radius: 8px;
    transition:
      transform 0.3s ease,
      box-shadow 0.3s ease;
  }

  .image-links figure:hover {
    transform: scale(1.05);
  }

  .image-links figure:hover img {
    box-shadow: 0 10px 20px rgba(255, 0, 0, 0.6);
  }

  .image-links figcaption a {
    font-family: seeds;
    color: red;
    font-size: 1rem;
    text-decoration: none;
    display: block;
    margin-top: 10px;
    transition: color 0.3s ease;
  }

  .image-links figcaption a:hover {
    color: #fff;
  }

  .cta-links {
    text-align: center;
    margin-top: 40px;
  }

  .cta-links img {
    width: 12px;
    height: 12px;
    margin-right: 8px;
  }

  .cta-links a {
    color: red;
    text-decoration: none;
    font-size: 1.2rem;
    margin-top: 10px;
    display: inline-flex;
    align-items: center;
    transition: color 0.3s ease;
  }

  .cta-links a:hover {
    color: #fff;
  }

  footer {
    text-align: center;
    margin-top: 40px;
    font-size: 0.8rem;
    color: #888;
    padding: 20px 0;
  }

  footer h1 {
    margin-top: 20px;
  }

  .small-text {
    font-size: 0.8em;
    text-align: center;
    display: block;
    margin-top: 20px;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 2rem;
    }

    .image-links {
      grid-template-columns: 1fr 1fr;
    }

    .image-links img {
      max-width: 120px;
    }

    .cta-links a {
      font-size: 1.1rem;
    }

    footer {
      font-size: 0.7rem;
    }
  }

  @media (max-width: 480px) {
    .image-links {
      grid-template-columns: 1fr;
    }

    .cta-links a {
      font-size: 1rem;
    }

    footer {
      font-size: 0.6rem;
    }
  }
</style>
