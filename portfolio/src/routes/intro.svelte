<script>
    // Project data
    const projects = [
      {
        title: "Techwaste",
        imageUrl: "https://github.com/Techwaste/.github/raw/main/assets/image.png",
        description: "Contributing for making Techwaste E-waste management system, I made Techwaste Backend API using FastAPI, Over 22 Endpoints were created and deployed to GCP's CloudRun.",
        category: "Backend",
        link: "https://github.com/Techwaste",
        linkText: "Visit Repository"
      },
      {
        title: "Perita",
        imageUrl: "https://i.ibb.co/7p3b2zb/Screenshot-2024-06-21-041001.png",
        description: "A social app to share your story. Allows you to share your story with the world. With Perita, you can create and share stories in a variety of formats, including text and photos. You can also see others story share your interests.",
        category: "Android",
        link: "https://github.com/Riveong/Perita",
        linkText: "Visit Repository"
      },
      {
        title: "Tutoreal",
        imageUrl: "https://avatars.githubusercontent.com/u/148473853?s=48&v=4",
        description: "A Private tutor app personalized with users' personalities. Contributing + my thesis title about personality based matchmaking between individuals. I made the backend with FastAPI, Using MAB concept.",
        category: "RecSys",
        link: "https://github.com/Riveong/Perita",
        linkText: "Visit Repository"
      },
      {
        title: "Octavia",
        imageUrl: "https://i.ibb.co/LhxPfmK/97411bff-9626-47ae-bcf3-9dcca346268a-width-1024-height-1024.jpg",
        isRounded: true,
        description: "Octavia is a all in one cashier app with stock management, and warehouse management. Octavia can be defined as the app you need for your business. I made this project using Svelte (front-end) and FastAPI for the backend.",
        category: "Fullstack",
        link: "https://github.com/Riveong/Octavia",
        linkText: "Visit Repository"
      },
      {
        title: "Istana Keramik",
        description: "A website for selling ceramics and other building materials. Simple elegant and fast website made with html, css, javascript and svelte as the javascript framework.",
        category: "Fullstack",
        link: "https://istanakeramik.com",
        linkText: "Visit Website"
      },
      {
        title: "Adivasa",
        description: "A Website profile",
        category: "Fullstack",
        link: "https://github.com/Riveong/Tailor-website",
        linkText: "Visit Website"
      },
      {
        title: "Penjahit Trend Tailor Semarang",
        description: "A Tailor landing page website, made with HTML, CSS, JavaScript. Using Sveltekit as the framework, I made this Modern concept website.",
        category: "Fullstack",
        link: "https://github.com/Riveong/Tailor-website",
        linkText: "Visit Website"
      },
      {
        title: "dox3",
        description: "Getting bored of normal to do / jounaling apps, I tried to make my own to do app. I made it with Svelte and Express Js. Using sqlite as for the database.",
        category: "Fullstack",
        link: "https://github.com/Riveong/dox3",
        linkText: "Visit Repository"
      }
    ];
  </script>
  
  <div>
    <div class="quote-banner">
      <p class="robotix text-white">"There's Courage In Being Terrified, But Still Going Forward." -Karlach</p>
    </div>
    
    <section class="section about-section" style="background-image: url('/api/placeholder/1200/600');">
      <div class="section-overlay">
        <div class="section-content">
          <div class="flex-container">
            <div class="flex-item-left">
              <h1 class="section-title">Who am I?</h1>
            </div>
            <div class="flex-item-right">
              <p class="robotix">I'm <b>Ong Gabriel Riverine Susanto</b> also known as Riveong. I'm an adventurous software engineer and also an ex 2023 Bangkit cohort.</p>
              <p class="robotix">As a bachelor of informatics, I have a strong passion in software engineering. I am a lover of tech and all its wonders. I marvel at the power of Back-end dev, Mobile dev, UI/UX and the infinite possibilities it offers. I delight in learning new things and expanding my horizons. <b>I cherish writing, debugging, problem solving, working under pressure</b> as art forms of expression and creativity.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <section class="section projects-section" style="background-image: url('/api/placeholder/1200/600');">
      <div class="section-overlay">
        <div class="section-content">
          <div class="flex-container">
            <div class="flex-item-left">
              <h1 class="section-title">What do I do?</h1>
            </div>
            <div class="flex-item-right">
              <p class="robotix mb-8">I do software engineering! I have done over <b>100+ projects</b>, here are the most notable projects I've finished.</p>
            </div>
          </div>
          
          <div class="projects-grid">
            {#each projects as project}
              <div class="project-card">
                {#if project.imageUrl}
                  <img 
                    src={project.imageUrl} 
                    alt={project.title} 
                    class="project-image {project.isRounded ? 'rounded' : ''}"
                  />
                {/if}
                <h2 class="project-title">{project.title}</h2>
                <p class="project-description">{project.description}</p>
                <div class="project-footer">
                  <span class="category-tag">{project.category}</span>
                  <a href={project.link} class="project-link">{project.linkText}</a>
                </div>
              </div>
            {/each}
          </div>
        </div>
      </div>
    </section>
  </div>
  
  <style>
    :global(*) {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    .quote-banner {
      background-color: black;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    
    .section {
      position: relative;
      background-size: cover;
      background-position: center;
    }
    
    .section-overlay {
      width: 100%;
      height: 100%;
      background-color: rgba(255, 255, 255, 0.85);
      padding: 5% 8%;
    }
    
    .section-content {
      position: relative;
      z-index: 2;
    }
    
    .flex-container {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
    }
    
    .flex-item-left {
      flex: 1 1 300px;
    }
    
    .flex-item-right {
      flex: 1 1 300px;
    }
    
    .section-title {
      font-size: 4rem;
      margin-bottom: 1.5rem;
      line-height: 1.2;
    }
    
    .robotix {
      font-family: "DM Mono", monospace;
      font-weight: 400;
      font-size: 1.25rem;
      line-height: 1.8;
    }
    
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.5rem;
      margin: 2rem 0;
    }
    
    .project-card {
      background-color: #f8f8f8;
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      height: 100%;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .project-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    }
    
    .project-image {
      width: 70px;
      height: 70px;
      object-fit: cover;
      margin: 0 auto 1rem;
    }
    
    .project-image.rounded {
      border-radius: 15px;
    }
    
    .project-title {
      font-size: 1.75rem;
      margin-bottom: 1rem;
    }
    
    .project-description {
      font-size: 0.9rem;
      flex-grow: 1;
      margin-bottom: 1.5rem;
    }
    
    .project-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: auto;
    }
    
    .category-tag {
      background-color: #ccc;
      padding: 0.5rem 1rem;
      font-size: 0.75rem;
      border-radius: 4px;
    }
    
    .project-link {
      background-color: black;
      color: white;
      text-decoration: none;
      padding: 0.5rem 1rem;
      font-size: 0.75rem;
      border-radius: 4px;
      transition: opacity 0.3s ease;
    }
    
    .project-link:hover {
      opacity: 0.9;
    }
    
    /* Media queries for responsiveness */
    @media (max-width: 992px) {
      .section-title {
        font-size: 3rem;
      }
      
      .robotix {
        font-size: 1.1rem;
      }
    }
    
    @media (max-width: 768px) {
      .section-overlay {
        padding: 3rem 1.5rem;
      }
      
      .section-title {
        font-size: 2.5rem;
      }
      
      .flex-container {
        flex-direction: column;
        gap: 1rem;
      }
      
      .flex-item-left, .flex-item-right {
        flex: 1 1 100%;
      }
      
      .projects-grid {
        grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      }
    }
    
    @media (max-width: 480px) {
      .section-title {
        font-size: 2rem;
      }
      
      .robotix {
        font-size: 1rem;
        line-height: 1.6;
      }
      
      .projects-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>