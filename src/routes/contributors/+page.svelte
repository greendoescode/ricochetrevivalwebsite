<script>
  let contributors = [
    {
      name: "TheBasicDog",
      title: "Owner of the Server, Creator of Ricochet Revival",
      role: "THE ONE BEHIND IT ALL",
    },
    {
      name: "ImGreen",
      title: "Server Hoster",
      role: "MAIN CONTRIBUTORS",
    },
    {
      name: "NintenGunner",
      title: "Website Maintainer, Graphic Designer",
      role: "MAIN CONTRIBUTORS",
    },
    {
      name: "ReactedDrop",
      title: "Graphic Designer",
      role: "MAIN CONTRIBUTORS",
    },
    {
      name: "LiTHiuM",
      title: "Created the Mouse Accelerator Client Plugin",
      role: "PLUGIN CREATORS",
    },
    {
      name: "trk305",
      title: "Ricochet Enhanced Creator",
      role: "PLUGIN CREATORS",
    },
    {
      name:"The Ricochet Lovers",
      title:"Keeping the game alive",
      role:"Players",
    },
  ];

  let groupedContributors = contributors.reduce((acc, contributor) => {
    if (!acc[contributor.role]) {
      acc[contributor.role] = [];
    }
    acc[contributor.role].push(contributor);
    return acc;
  }, {});
</script>

<main>
  <h1><img src="ricosite contribs.png" alt="Ricochet Revival Team" /></h1>
  <h1><strong>Meet the Ricochet Revival Team</strong></h1>

  {#each Object.entries(groupedContributors) as [role, contributorsList]}
    <section>
      <h3>{role}</h3>
      {#each contributorsList as { name, title }}
        <p><strong>{name}</strong></p>
        <p class="role">{title}</p>
      {/each}
    </section>
  {/each}

  <a href="/">
    <img
      src="arrowanim.gif"
      style="transform:scaleX(-1);"
      alt="Back to homepage"
    />
    <img src="main.png" alt="Main Icon" />
  </a>
</main>

<style>
  main {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
  }

  h1 {
    color: red;
    text-align: center;
    margin-bottom: 20px;
  }

  h1 img {
    max-width: 100%;
    height: auto;
  }

  h3 {
    color: blue;
    font-size: 170%;
    margin-top: 20px;
    text-align: center;
  }

  p {
    font-size: 150%;
    text-align: center;
  }

  .role {
    font-size: 125%;
    text-align: center;
  }

  section {
    margin-bottom: 40px;
  }

  a {
    display: block;
    text-align: center;
    margin-top: 40px;
  }

  a img:first-child {
    width: 32px;
    vertical-align: middle;
  }

  a img:last-child {
    max-width: 100%;
    height: auto;
    width: 120px;
  }

  @media (max-width: 600px) {
    h3 {
      font-size: 150%;
    }

    p {
      font-size: 120%;
    }

    .role {
      font-size: 110%;
    }

    a img:first-child {
      width: 24px;
    }

    a img:last-child {
      width: 100px;
    }
  }
</style>
