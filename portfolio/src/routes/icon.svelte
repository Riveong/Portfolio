<script>
    import { onMount } from 'svelte';
    import Icon1 from '$lib/assets/speaker.png';
  
    let isMuted = false;
  

    function toggleMute() {
      const audioElements = document.querySelectorAll('audio');
      isMuted = !isMuted;
      audioElements.forEach(audio => {
        audio.muted = isMuted;
      });
    }
  </script>
  
  <!-- Blog link in top left -->
  <div class="blog-link">
    <a href="https://shoul.krotify.com">Visit my blog@</a>
  </div>

  <div class="floating-menu">

      <button class="menu-item" on:click={toggleMute}>
        <img src={Icon1} style="width: 15px;" alt="Speaker Icon">
      </button>

      <a class="menu-item" href="https://www.linkedin.com/in/ong-gabriel-riverine-susanto/" target="_blank" rel="noopener noreferrer">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/640px-LinkedIn_logo_initials.png" style="width: 20px;" alt="LinkedIn Icon">
      </a>

      <a class="menu-item" href="mailto:ongrive@gmail.com">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Gmail_icon_%282020%29.svg/2560px-Gmail_icon_%282020%29.svg.png" style="width: 20px;" alt="Gmail Icon">
      </a>
      
      <a class="menu-item" href="https://github.com/Riveong" target="_blank" rel="noopener noreferrer">
        <img src="https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png" style="width: 20px;" alt="GitHub Icon">
      </a>

  </div>

  <style>
    /* Blog link styles */
    .blog-link {
      position: fixed;
      top: 20px;
      left: 20px;
      z-index: 9999;
    }

    .blog-link a {
      font-family: "DM Mono", monospace;
      font-size: 1rem;
      color: #333;
      text-decoration: none;
      padding: 0.5rem 1rem;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid #333;
      border-radius: 4px;
      transition: all 0.3s ease;
      backdrop-filter: blur(5px);
    }

    .blog-link a:hover {
      background: #333;
      color: white;
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    .floating-menu {    
      position: fixed;
      top: 20%;
      right: 0;
      transform: translateY(-50%);
      display: flex;
      flex-direction: column;
      background: #ffffff;
      border: 0.5px solid black;
      border-radius: 8px 0 0 8px;
      overflow: hidden;
      z-index: 9999; /* Ensures it's in front of all components */
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    }
  
    .menu-item {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;
      color: #333;
      text-decoration: none;
      border-bottom: 1px solid #e0e0e0;
      background: transparent;
      border: none;
      cursor: pointer;
      transition: all 0.3s ease;
    }
  
    .menu-item:last-child {
      border-bottom: none;
    }
  
    .menu-item:hover {
      background: #a5c0ff;
      transform: translateX(-2px);
    }

    .menu-item:active {
      transform: translateX(-1px);
    }
  
    .menu-item i {
      font-size: 24px;
    }

    .menu-item svg {
      color: #333;
      transition: color 0.3s ease;
    }

    .menu-item:hover svg {
      color: #fff;
    }

    /* Tablet styles */
    @media (max-width: 1024px) {
      .floating-menu {
        top: 15%;
        right: 5px;
      }

      .menu-item {
        width: 45px;
        height: 45px;
      }

      .blog-link {
        top: 15px;
        left: 15px;
      }

      .blog-link a {
        font-size: 0.9rem;
        padding: 0.4rem 0.8rem;
      }
    }

    /* Mobile landscape and smaller tablets */
    @media (max-width: 768px) {
      .floating-menu {
        top: auto;
        bottom: 20px;
        right: 20px;
        flex-direction: row;
        border-radius: 25px;
        border: 0.5px solid black;
        padding: 5px;
      }

      .menu-item {
        width: 40px;
        height: 40px;
        border-bottom: none;
        border-right: 1px solid #e0e0e0;
        border-radius: 50%;
        margin: 2px;
      }

      .menu-item:last-child {
        border-right: none;
      }

      .menu-item:hover {
        transform: translateY(-2px);
      }

      .blog-link {
        top: 15px;
        left: 15px;
      }

      .blog-link a {
        font-size: 0.85rem;
        padding: 0.35rem 0.7rem;
      }
    }

    /* Small mobile devices */
    @media (max-width: 480px) {
      .floating-menu {
        bottom: 15px;
        right: 15px;
        padding: 3px;
      }

      .menu-item {
        width: 35px;
        height: 35px;
        margin: 1px;
      }

      .menu-item img {
        width: 15px !important;
      }

      .menu-item svg {
        width: 15px;
        height: 15px;
      }

      .blog-link {
        top: 10px;
        left: 10px;
      }

      .blog-link a {
        font-size: 0.8rem;
        padding: 0.3rem 0.6rem;
      }
    }

    /* Extra small devices */
    @media (max-width: 320px) {
      .floating-menu {
        bottom: 10px;
        right: 10px;
      }

      .menu-item {
        width: 30px;
        height: 30px;
      }

      .menu-item img {
        width: 12px !important;
      }

      .menu-item svg {
        width: 12px;
        height: 12px;
      }

      .blog-link a {
        font-size: 0.75rem;
        padding: 0.25rem 0.5rem;
      }
    }

    /* Large screens */
    @media (min-width: 1200px) {
      .floating-menu {
        right: 10px;
      }

      .menu-item {
        width: 55px;
        height: 55px;
      }

      .blog-link a {
        font-size: 1.1rem;
        padding: 0.6rem 1.2rem;
      }
    }
  </style>
