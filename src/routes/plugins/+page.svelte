<script>
  let plugins = [
    {
      title: "Mouse Transformer",
      creator: "LiTHiuM",
      description:
        "A custom mouse accelerator made specifically for Ricochet. Only works on resolutions that aren't widescreen.",
      downloadLink:
        "https://cdn.discordapp.com/attachments/1061091726741221446/1061796987239927838/ricochet_client_dll.rar",
    },
    {
      title: "Ricochet Enhanced",
      creator: "saudi305",
      description:
        "Ricochet Enhanced focuses on user preferences (which means better user experience and user freedom), bug fixes, code optimization, and useful & fun additions.",
      downloadLink: "https://gamebanana.com/mods/550956",
    },
  ];

  let showPopup = false;
  let currentPlugin = {};

  const openPopup = (plugin) => {
    currentPlugin = plugin;
    showPopup = true;
  };

  const closePopup = () => {
    showPopup = false;
  };
</script>

<main>
  <h1><img src="ricosite plugins.png" alt="Ricochet Plugins" /></h1>

  <div class="plugin-list">
    {#each plugins as plugin}
      <div class="plugin-item" on:click={() => openPopup(plugin)}>
        <h3 style="font-family: 'seeds';">{plugin.title}</h3>
        <p>{plugin.description}</p>
      </div>
    {/each}
  </div>

  <div class="popup" class:active={showPopup}>
    <div class="popup-content">
      <h2 style="font-family: 'seeds';">{currentPlugin.title}</h2>
      <p>Created by: {currentPlugin.creator}</p>
      <p>{currentPlugin.description}</p>
      <a href={currentPlugin.downloadLink} target="_blank">DOWNLOAD HERE</a>
      <div class="close-btn" on:click={closePopup}>Close</div>
    </div>
  </div>

  <div class="mod-footer">
    <h3>Want more mods?</h3>
    <p>
      Check out more mods on <a
        href="https://gamebanana.com/games/270"
        target="_blank">Gamebanana!</a
      >
    </p>
  </div>

  <a href="/">
    <img
      src="arrowanim.gif"
      style="transform:scaleX(-1);"
      alt="Back to homepage"
    />
    <img src="main.png" alt="Main Icon" style="margin-top: 20px;" />
  </a>
</main>

<style>
  @font-face {
    font-family: "seeds";
    src: url(/SEEDS.TTF);
  }

  body {
    margin: 0;
    padding: 0;
    background-color: #111;
    color: #f0f0f0;
  }

  main {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }

  h1 {
    color: #ffcc00;
    margin-bottom: 20px;
  }

  h1 img {
    max-width: 100%;
    height: auto;
  }

  .plugin-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }

  .plugin-item {
    background-color: #1a1a1a;
    border: 1px solid #333;
    border-radius: 8px;
    padding: 15px;
    text-align: center;
    cursor: pointer;
    transition:
      transform 0.3s ease,
      background-color 0.3s ease;
    color: #ffcc00;
  }

  .plugin-item:hover {
    transform: scale(1.05);
    background-color: #333;
  }

  .plugin-item h3 {
    color: #ffcc00;
    margin: 10px 0;
  }

  .plugin-item p {
    font-size: 120%;
    color: #ddd;
  }

  .popup {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.9);
    z-index: 1000;
    justify-content: center;
    align-items: center;
    display: none;
  }

  .popup.active {
    display: flex;
  }

  .popup-content {
    background-color: #222;
    padding: 20px;
    border-radius: 8px;
    max-width: 500px;
    width: 80%;
    text-align: center;
    color: #f0f0f0;
  }

  .popup-content h2 {
    color: #ffcc00;
  }

  .popup-content p {
    font-size: 120%;
    margin-bottom: 20px;
  }

  .popup-content a {
    display: inline-block;
    background-color: #0066cc;
    color: #f0f0f0;
    padding: 10px 20px;
    text-decoration: none;
    border-radius: 5px;
    font-size: 18px;
    transition: background-color 0.3s ease;
  }

  .popup-content a:hover {
    background-color: #005bb5;
  }

  .close-btn {
    margin-top: 20px;
    font-size: 18px;
    color: #ffcc00;
    cursor: pointer;
  }

  .mod-footer {
    margin-top: 40px;
    text-align: center;
    color: #f0f0f0;
  }

  .mod-footer a {
    text-decoration: none;
    color: #0066cc;
    font-weight: bold;
  }

  .mod-footer a:hover {
    color: #0044aa;
  }

  @media (max-width: 600px) {
    h2 {
      font-size: 160%;
    }

    p {
      font-size: 120%;
    }

    .popup-content a {
      font-size: 16px;
      padding: 8px 16px;
    }

    .mod-footer a {
      font-size: 14px;
    }
  }
</style>
