<script>
    import { onMount } from 'svelte';
  
    let isClient = false;
    let discs = [];
    let audio;
  
    onMount(() => {
      isClient = true;
      audio = new Audio('/triggerjump.wav');
      
      const isMobile = window.innerWidth < 768;
      const numDiscs = isMobile ? 80 : 150;
  
      for (let i = 0; i < numDiscs; i++) {
        const color = Math.random() > 0.5 ? '#ff0000' : '#0000ff';
        discs.push({
          id: i,
          top: `${Math.random() * 100}vh`,
          left: `${Math.random() * 100}vw`,
          size: `${Math.random() * (isMobile ? 30 : 50) + 20}px`,
          animationDuration: Math.random() * 3 + 2,
          color: color,
        });
      }
    });
  
    function playSound() {
      if (audio) {
        audio.currentTime = 0;
        audio.play();
      }
    }
  </script>
  
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body { width: 100vw; height: 100vh; overflow: hidden; background: #121212; }
  
    .home-container {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      background: #121212;
      font-family: 'Press Start 2P', cursive;
      color: #fff;
      overflow: hidden;
    }
  
    .neon-text {
      max-width: 80%;
      font-size: clamp(1.5rem, 5vw, 3rem);
      text-shadow: 0 0 10px #ff0000, 0 0 20px #0000ff;
      animation: textGlow 1.5s infinite alternate;
      z-index: 10;
      cursor: pointer;
    }
  
    @keyframes textGlow {
      0% { text-shadow: 0 0 10px #ff0000, 0 0 20px #0000ff; }
      100% { text-shadow: 0 0 20px #ff0000, 0 0 40px #0000ff; }
    }
  
    .neon-button {
      margin-top: 1rem;
      padding: 1rem 2rem;
      font-size: clamp(0.8rem, 4vw, 1.2rem);
      background: #ff0000;
      border: 3px solid #0000ff;
      color: #fff;
      cursor: pointer;
      text-transform: uppercase;
      box-shadow: 0 0 10px rgba(255, 0, 255, 0.8);
      z-index: 10;
    }
  
    .neon-button:hover {
      background: #0000ff;
      color: #ff0000;
      box-shadow: 0 0 20px rgba(255, 0, 255, 0.9);
    }
  
    .disc {
      position: absolute;
      border-radius: 50%;
      box-shadow: 0 0 10px rgba(255, 0, 255, 0.8);
      animation: float 5s ease-in-out infinite, rotate 8s linear infinite;
      z-index: 1;
    }
  
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0); }
    }
  
    @keyframes rotate {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
  
    .scanline {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: repeating-linear-gradient(
        0deg,
        rgba(0, 0, 0, 0.5) 0,
        rgba(0, 0, 0, 0.5) 1px,
        transparent 1px,
        transparent 2px
      );
      pointer-events: none;
      z-index: 2;
    }
  </style>
  
  <section class="home-container">
    <div class="scanline"></div>
  
    <h1 class="neon-text" on:mouseenter={playSound}>Welcome to Ricochet Revival</h1>
  
    <p class="neon-button">THIS IS A LANDING PAGE UNTIL A WEBSITE IS SORTED</p>
  
    {#if isClient}
      {#each discs as disc (disc.id)}
        <div 
          class="disc" 
          style="top: {disc.top}; left: {disc.left}; width: {disc.size}; height: {disc.size}; background: {disc.color}; animation-duration: {disc.animationDuration}s;">
        </div>
      {/each}
    {/if}
  </section>
  