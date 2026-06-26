# Naomi-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Naomi - Personal Website</title>
    <style>
        :root {
            --primary-color: #007bff;
            --dark-color: #333;
            --bg-color: #f8f9fa;
            --text-color: #333;
            --card-bg: white;
            --card-border: #eee;
        }

        [data-theme="dark"] {
            --primary-color: #4da6ff;
            --dark-color: #f8f9fa;
            --bg-color: #121212;
            --text-color: #e0e0e0;
            --card-bg: #1e1e1e;
            --card-border: #333;
        }
        
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), #0056b3);
            color: white;
            text-align: center;
            padding: 5rem 1rem;
            position: relative;
        }
        
        header h1 {
            font-size: 3rem;
            margin: 0;
        }
        
        header p {
            font-size: 1.4rem;
            margin: 0.5rem 0 0;
            opacity: 0.9;
        }
        
        nav {
            background: var(--dark-color);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        nav a {
            color: white;
            margin: 0 1.2rem;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--primary-color);
        }
        
        main {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        
        section {
            margin-bottom: 4rem;
            padding: 2rem;
            background: var(--card-bg);
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            border: 1px solid var(--card-border);
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--card-border);
            padding-bottom: 0.5rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            margin: 10px 8px 10px 0;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1.05rem;
        }
        
        .btn:hover {
            background: #0056b3;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 123, 255, 0.3);
        }
        
        .btn-secondary {
            background: #6c757d;
        }
        
        .btn-secondary:hover {
            background: #5a6268;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .project-card {
            border: 1px solid var(--card-border);
            background: var(--card-bg);
            border-radius: 10px;
            padding: 1.5rem;
            transition: transform 0.3s, background 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-8px);
        }

        /* Media Section Styles */
        .media-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .video-container {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 1rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        video {
            width: 100%;
            border-radius: 8px;
            background: #000;
        }

        .download-list {
            list-style: none;
            padding: 0;
        }

        .download-list li {
            padding: 12px 0;
            border-bottom: 1px solid var(--card-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .upload-area {
            border: 2px dashed var(--primary-color);
            border-radius: 12px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            margin-top: 1.5rem;
        }

        .upload-area.dragover {
            background: rgba(0, 123, 255, 0.1);
            border-color: #0056b3;
        }

        .upload-area input[type="file"] {
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Naomi</h1>
        <p>Web Developer • Designer • Creator</p>
        
        <div class="hero-buttons">
            <a href="#about" class="btn">Learn More About Me</a>
            <a href="#projects" class="btn">View My Work</a>
            <a href="#media" class="btn">Media Gallery</a>
            <a href="#contact" class="btn btn-secondary">Get In Touch</a>
            
            <!-- Dark mode toggle -->
            <button id="theme-toggle" class="btn" style="background: rgba(255,255,255,0.2); border: 2px solid white; padding: 10px 16px; font-size: 1.1rem; min-width: 48px;" aria-label="Toggle dark mode">🌙</button>
        </div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#media">Media</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>I'm a passionate developer and designer with experience building beautiful digital experiences. Replace this text with your own bio.</p>
            
            <a href="#" class="btn" onclick="alert('Resume would download here in a real site!')">📄 Download Resume</a>
        </section>
        
        <section id="projects">
            <h2>Featured Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <h3>Project One</h3>
                    <p>A short description of your first project. What problem did it solve?</p>
                    <a href="#" class="btn" onclick="alert('This would link to the live demo!')">View Live Demo</a>
                    <a href="#" class="btn btn-secondary" onclick="alert('This would open the GitHub repo!')">GitHub</a>
                </div>
                <a href="your-audio-file.mp3" download>Download Audio Track</a>
                
                <div class="project-card">
                    <h3>Project Two</h3>
                    <p>Another impressive project. Highlight technologies used.</p>
                    <a href="#" class="btn" onclick="alert('Live demo clicked!')">View Live Demo</a>
                    <a href="#" class="btn btn-secondary" onclick="alert('GitHub link clicked!')">GitHub</a>
                </div>
            </div>
        </section>

        <!-- New Media Section -->
        <section id="media">
            <h2>Media Gallery &amp; Downloads</h2>
            <p>Explore video streaming demos, download media files, and try the file upload feature (demo).</p>
            
            <div class="media-grid">
                <!-- Video Streaming -->
                <div class="video-container">
                    <h3>Video Streaming</h3>
                    <p>Sample video player (demo content)</p>
                    <video id="demo-video" controls>
                        <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div style="margin-top: 1rem;">
                        <button onclick="document.getElementById('demo-video').play()" class="btn">▶ Play</button>
                        <button onclick="document.getElementById('demo-video').pause()" class="btn btn-secondary">⏸ Pause</button>
                    </div>
                </div>

                <!-- Downloads -->
                <div class="video-container">
                    <h3>Downloads</h3>
                    <p>Media and project files available for download</p>
                    <ul class="download-list">
                        <li>
                            <span>📹 Sample Video (Big Buck Bunny)</span>
                            <a href="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" download class="btn" style="padding: 8px 16px; font-size: 0.95rem;">Download</a>
                        </li>
                        <li>
                            <span>📸 Sample Image</span>
                            <a href="https://picsum.photos/id/1015/1920/1080" download="sample-image.jpg" class="btn" style="padding: 8px 16px; font-size: 0.95rem;">Download</a>
                        </li>
                        <li>
                            <span>📄 Project PDF (Demo)</span>
                            <a href="#" onclick="alert('In a real site this would trigger a PDF download')" class="btn" style="padding: 8px 16px; font-size: 0.95rem;">Download</a>
                        </li>
                    </ul>
                </div>

                <!-- File Upload -->
                <div class="video-container">
                    <h3>File Upload</h3>
                    <p>Upload your media files (demo - files are processed client-side only)</p>
                    
                    <div id="upload-area" class="upload-area">
                        <p>Drag &amp; drop files here or</p>
                        <label class="btn" style="cursor: pointer;">
                            Choose File
                            <input type="file" id="file-input" multiple>
                        </label>
                        <div id="upload-status" style="margin-top: 1rem; font-size: 0.9rem;"></div>
                    </div>

                    <div id="uploaded-files" style="margin-top: 1.5rem;"></div>
                </div>
            </div>
        </section>
        
        <section id="contact">
            <h2>Contact Me</h2>
            <p>Interested in working together? Let's talk!</p>
            
            <div>
                <a href="mailto:you@example.com" class="btn">📧 Email Me</a>
                <a href="https://twitter.com/yourhandle" target="_blank" class="btn btn-secondary">🐦 Twitter</a>
                <a href="https://linkedin.com/in/yourprofile" target="_blank" class="btn">💼 LinkedIn</a>
            </div>
            
            <!-- Simple contact form -->
            <form style="margin-top: 2rem; max-width: 500px;" onsubmit="handleSubmit(event)">
                <input type="text" placeholder="Your Name" style="width: 100%; padding: 12px; margin: 8px 0; border: 1px solid var(--card-border); border-radius: 6px; background: var(--card-bg); color: var(--text-color);" required><br>
                <input type="email" placeholder="Your Email" style="width: 100%; padding: 12px; margin: 8px 0; border: 1px solid var(--card-border); border-radius: 6px; background: var(--card-bg); color: var(--text-color);" required><br>
                <textarea placeholder="Your Message" rows="5" style="width: 100%; padding: 12px; margin: 8px 0; border: 1px solid var(--card-border); border-radius: 6px; background: var(--card-bg); color: var(--text-color);" required></textarea><br>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2026 Naomi. Built with ❤️ and HTML/CSS.</p>
        <p>
            <a href="#" style="color: white; margin: 0 10px;">Privacy</a> • 
            <a href="#" style="color: white; margin: 0 10px;">Terms</a>
        </p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });
        
        // Form submission handler
        function handleSubmit(e) {
            e.preventDefault();
            alert("Thank you! Your message has been received. (This is a demo — connect a real backend for actual emails)");
            e.target.reset();
        }
        
        console.log("%cWebsite loaded successfully! 🚀", "color: #007bff; font-size: 14px;");

        // Dark Mode Toggle
        const toggleButton = document.getElementById('theme-toggle');
        const currentTheme = localStorage.getItem('theme') || 'light';

        if (currentTheme === 'dark') {
            document.documentElement.setAttribute('data-theme', 'dark');
            toggleButton.textContent = '☀️';
        }

        toggleButton.addEventListener('click', () => {
            const isDark = document.documentElement.getAttribute('data-theme') === 'dark';
            
            if (isDark) {
                document.documentElement.removeAttribute('data-theme');
                toggleButton.textContent = '🌙';
                localStorage.setItem('theme', 'light');
            } else {
                document.documentElement.setAttribute('data-theme', 'dark');
                toggleButton.textContent = '☀️';
                localStorage.setItem('theme', 'dark');
            }
        });

        // File Upload Demo
        const uploadArea = document.getElementById('upload-area');
        const fileInput = document.getElementById('file-input');
        const uploadStatus = document.getElementById('upload-status');
        const uploadedFilesContainer = document.getElementById('uploaded-files');

        // Click to upload
        uploadArea.addEventListener('click', () => {
            fileInput.click();
        });

        // Drag and drop
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.classList.add('dragover');
        });

        uploadArea.addEventListener('dragleave', () => {
            uploadArea.classList.remove('dragover');
        });

        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('dragover');
            handleFiles(e.dataTransfer.files);
        });

        fileInput.addEventListener('change', (e) => {
            handleFiles(e.target.files);
        });

        function handleFiles(files) {
            uploadStatus.textContent = `Processing ${files.length} file(s)...`;
            
            Array.from(files).forEach(file => {
                const fileDiv = document.createElement('div');
                fileDiv.style.cssText = 'padding: 10px; margin: 8px 0; background: var(--card-bg); border: 1px solid var(--card-border); border-radius: 6px;';
                fileDiv.innerHTML = `
                    <strong>\( {file.name}</strong> ( \){(file.size / 1024 / 1024).toFixed(2)} MB)<br>
                    <small>Uploaded successfully (demo)</small>
                `;
                uploadedFilesContainer.appendChild(fileDiv);
            });

            setTimeout(() => {
                uploadStatus.textContent = `${files.length} file(s) uploaded successfully! 🎉`;
            }, 800);
        }
    </script>
</body>
</html>
