<script>
  const servers = [
    {
      name: "Ricochet Revival - NA",
      link: "steam://connect/23.148.201.40:27015",
    },
    {
      name: "Ricochet Revival - EU",
      link: "steam://connect/216.21.6.133:27015",
    },
  ];
</script>

<main>
  <h1><img src="ricosite serverlist.png" alt="Server List" /></h1>

  <div class="server-list">
    {#each servers as server}
      <div class="server-item" on:click={(window.location = server.link)}>
        <img src="arrowanim.gif" width="20" height="20" alt="Arrow Icon" />
        <a href={server.link} target="_blank">{server.name}</a>
      </div>
    {/each}
  </div>

  <a href="/">
    <img
      src="arrowanim.gif"
      style="transform:scaleX(-1);"
      alt="Back to homepage"
    />
    <img src="main.png" alt="Main Icon" height="32" style="margin-top: 20px;" />
  </a>
</main>

<style>
  @font-face {
    font-family: "seeds";
    src: url(/SEEDS.TTF);
  }

  main {
    max-width: 1000px;
    margin: 0 auto;
    padding: 40px;
    text-align: center;
  }

  h1 {
    font-size: 3rem;
    color: #ffcc00;
    margin-bottom: 20px;
    text-shadow: 2px 2px #000;
  }

  h1 img {
    max-width: 100%;
    height: auto;
  }

  .server-list {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 20px;
  }

  .server-item {
    background-color: #222222;
    border: 2px solid #ffcc00;
    border-radius: 12px;
    padding: 20px;
    cursor: pointer;
    font-size: 1.5rem;
    text-align: center;
    transition: all 0.2s ease;
    box-shadow: 0 0 10px rgba(255, 204, 0, 0.8);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .server-item:hover {
    background-color: #333333;
    box-shadow: 0 0 20px rgba(255, 204, 0, 1);
  }

  .server-item a {
    text-decoration: none;
    color: #ffcc00;
    font-weight: bold;
  }

  .server-item img {
    vertical-align: middle;
    margin-right: 10px;
  }

  .mod-footer a:hover {
    color: #0099cc;
  }

  .server-item {
    font-family: "seeds", Courier, monospace;
    background: #000;
    color: #00ff00;
    padding: 20px;
    font-size: 1.8rem;
    cursor: pointer;
    position: relative;
    transition: all 0.3s ease;
  }

  .server-item:hover {
    background-color: #111;
    border-color: #ffcc00;
  }

  .server-item a {
    text-decoration: none;
    color: #ffcc00;
  }

  .server-item img {
    vertical-align: middle;
    margin-right: 15px;
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2rem;
    }

    .server-item a {
      font-size: 1.2rem;
    }

    .mod-footer a {
      font-size: 14px;
    }
  }

  .popup {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.7);
    color: #ffcc00;
    display: none;
    align-items: center;
    justify-content: center;
  }

  .popup.active {
    display: flex;
  }

  .popup-content {
    background-color: #222;
    padding: 40px;
    text-align: center;
    width: 80%;
    max-width: 500px;
  }

  .popup-content h2 {
    font-size: 2rem;
    color: #ffcc00;
  }

  .popup-content p {
    font-size: 1.2rem;
    color: #fff;
  }

  .close-btn {
    background-color: #ffcc00;
    color: #000;
    border: none;
    padding: 10px 20px;
    margin-top: 20px;
    cursor: pointer;
    font-size: 1.5rem;
    border-radius: 8px;
    transition: all 0.3s ease;
  }
</style>
