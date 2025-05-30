<script>
    // No form logic needed, just contact info
</script>

<svelte:head>
    <title>Contact Me - Get in Touch</title>
    <meta name="description" content="Contact me for business inquiries, collaborations, or just to say hello!" />
</svelte:head>

<main class="contact-page">
    <div class="container">
        <header class="contact-header">
            <h1 class="contact-title">Get in Touch</h1>
            <p class="robotix contact-subtitle">
                For any business inquiries, collaboration opportunities, or just to say hello - I'd love to hear from you!
            </p>
        </header>

        <div class="contact-content">
            <div class="contact-info">
                <div class="contact-method">
                    <div class="method-icon">📧</div>
                    <div class="method-content">
                        <h4>Email</h4>
                        <a href="mailto:ongrive@gmail.com" class="contact-link">ongrive@gmail.com</a>
                        <p class="method-description">Best way to reach me for business inquiries</p>
                    </div>
                </div>

                <div class="contact-method">
                    <div class="method-icon">💼</div>
                    <div class="method-content">
                        <h4>LinkedIn</h4>
                        <a href="https://www.linkedin.com/in/ong-gabriel-riverine-susanto/" target="_blank" rel="noopener noreferrer" class="contact-link">
                            Connect with me
                        </a>
                        <p class="method-description">Let's connect professionally</p>
                    </div>
                </div>

                <div class="contact-method">
                    <div class="method-icon">💻</div>
                    <div class="method-content">
                        <h4>GitHub</h4>
                        <a href="https://github.com/Riveong" target="_blank" rel="noopener noreferrer" class="contact-link">
                            View my work
                        </a>
                        <p class="method-description">Check out my projects and contributions</p>
                    </div>
                </div>

                <div class="contact-method">
                    <div class="method-icon">📝</div>
                    <div class="method-content">
                        <h4>Blog</h4>
                        <a href="https://shoul.krotify.com" target="_blank" rel="noopener noreferrer" class="contact-link">
                            Visit my blog
                        </a>
                        <p class="method-description">Read my thoughts and technical articles</p>
                    </div>
                </div>
            </div>

            <div class="response-info">
                <h3 class="info-title">Response Time</h3>
                <p class="robotix">
                    I typically respond within <strong>24-48 hours</strong> during weekdays. 
                    Feel free to reach out for any collaboration opportunities, project discussions, 
                    or just to say hello!
                </p>
            </div>
        </div>
    </div>
</main>

<style>
    .contact-page {
        min-height: 100vh;
        background: white;
        padding: 4rem 0;
    }

    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    .contact-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .contact-title {
        font-size: 4rem;
        color: #333;
        margin-bottom: 1.5rem;
        font-weight: 700;
        line-height: 1.2;
    }

    .robotix {
        font-family: "DM Mono", monospace;
        font-weight: 400;
        font-style: normal;
    }

    .contact-subtitle {
        font-size: 1.25rem;
        color: #666;
        line-height: 1.8;
        max-width: 600px;
        margin: 0 auto;
    }

    .contact-content {
        display: flex;
        flex-direction: column;
        gap: 3rem;
    }

    .contact-info {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
    }

    .contact-method {
        display: flex;
        align-items: flex-start;
        gap: 1.5rem;
        padding: 2rem;
        background: #f8f8f8;
        border: 1px solid #ccc;
        border-radius: 8px;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .contact-method:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    }

    .method-icon {
        font-size: 2rem;
        width: 60px;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #333;
        color: white;
        border-radius: 50%;
        flex-shrink: 0;
    }

    .method-content {
        flex: 1;
    }

    .method-content h4 {
        color: #333;
        margin-bottom: 0.5rem;
        font-size: 1.5rem;
    }

    .contact-link {
        color: #333;
        text-decoration: none;
        font-family: "DM Mono", monospace;
        font-size: 1rem;
        font-weight: 600;
        transition: color 0.3s ease;
        display: inline-block;
        margin-bottom: 0.5rem;
    }

    .contact-link:hover {
        color: #666;
        text-decoration: underline;
    }

    .method-description {
        color: #666;
        font-size: 0.9rem;
        margin: 0;
        line-height: 1.5;
    }

    .response-info {
        background: #f8f8f8;
        border: 1px solid #ccc;
        border-radius: 8px;
        padding: 2rem;
        text-align: center;
    }

    .info-title {
        font-size: 1.75rem;
        color: #333;
        margin-bottom: 1rem;
        font-weight: 600;
    }

    .response-info p {
        font-size: 1.1rem;
        color: #555;
        margin: 0;
        line-height: 1.8;
    }

    /* Responsive Design */
    @media (max-width: 992px) {
        .contact-title {
            font-size: 3rem;
        }
        
        .contact-subtitle {
            font-size: 1.1rem;
        }
    }

    @media (max-width: 768px) {
        .container {
            padding: 0 1rem;
        }

        .contact-title {
            font-size: 2.5rem;
        }

        .contact-info {
            grid-template-columns: 1fr;
        }

        .contact-method {
            padding: 1.5rem;
        }

        .method-icon {
            width: 50px;
            height: 50px;
            font-size: 1.5rem;
        }

        .method-content h4 {
            font-size: 1.25rem;
        }
    }

    @media (max-width: 480px) {
        .contact-page {
            padding: 2rem 0;
        }

        .contact-title {
            font-size: 2rem;
        }

        .contact-subtitle {
            font-size: 1rem;
        }

        .contact-method {
            padding: 1rem;
            flex-direction: column;
            text-align: center;
            gap: 1rem;
        }

        .response-info {
            padding: 1.5rem;
        }

        .info-title {
            font-size: 1.5rem;
        }
    }
</style>