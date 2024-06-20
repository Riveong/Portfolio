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
  
  <div class="floating-menu">

      <button class="menu-item" on:click={toggleMute}>
        <img src={Icon1} style="width: 15px;" alt="Speaker Icon">
      </button>


        <a class="menu-item" href="https://www.linkedin.com/in/ong-gabriel-riverine-susanto/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/640px-LinkedIn_logo_initials.png" style="width: 20px;" alt="Speaker Icon">
        </a>

        <a class="menu-item" href="mailto:ongrive@gmail.com">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Gmail_icon_%282020%29.svg/2560px-Gmail_icon_%282020%29.svg.png" style="width: 20px;" alt="Speaker Icon">
          </a>
        
          <a class="menu-item" href="https://github.com/Riveong">
            <img src="https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png" style="width: 20px;" alt="Speaker Icon">
            </a>

          </div>




  <style>
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
    }
  
    .menu-item {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;
      color: white;
      text-decoration: none;
      border-bottom: 1px solid #a0a0a0;
    }
  
    .menu-item:last-child {
      border-bottom: none;
    }
  
    .menu-item:hover {
      background: #a5c0ff;
    }
  
    .menu-item i {
      font-size: 24px;
    }
    /* Media query for screens less than 768px wide */
    @media (max-width: 768px) {
        .floating-menu {
            top: auto;
            bottom: 20px;
            right: 20px;
            flex-direction: row;
            border-radius: 8px;
        }

        .menu-item {
            width: 40px;
            height: 40px;
        }
    }

    /* Media query for screens less than 480px wide */
    @media (max-width: 480px) {
        .floating-menu {
            bottom: 90%;
            right: 9%;
        }

        .menu-item {
            width: 35px;
            height: 35px;
        }
    }
  </style>
  