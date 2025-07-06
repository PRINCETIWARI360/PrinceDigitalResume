# PrinceDigitalResume
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aniket Kumar Singh - Resume</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0d47a1;
            --secondary: #1976d2;
            --accent: #ff6f00;
            --light: #f5f5f5;
            --dark: #212121;
            --gray: #757575;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f0f4f8;
            color: #333;
            line-height: 1.6;
            padding: 20px;
        }

        .resume-container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
        }

        .name {
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .title {
            font-size: 1.4rem;
            font-weight: 400;
            opacity: 0.9;
            margin-bottom: 25px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.05rem;
        }

        .contact-icon {
            background: rgba(255, 255, 255, 0.2);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .resume-body {
            padding: 40px;
        }

        .section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--accent);
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--secondary);
        }

        .section-content {
            padding-left: 20px;
        }

        .career-objective {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--dark);
        }

        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 15px;
        }

        .skill-category {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }

        .skill-category h3 {
            color: var(--secondary);
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-item {
            background: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.95rem;
            border: 1px solid #e0e0e0;
            transition: all 0.3s ease;
        }

        .skill-item:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(25, 118, 210, 0.3);
        }

        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .education-item {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            position: relative;
            border-left: 4px solid var(--accent);
        }

        .education-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--dark);
        }

        .education-subtitle {
            font-size: 1.1rem;
            color: var(--secondary);
            margin-bottom: 8px;
        }

        .education-meta {
            display: flex;
            justify-content: space-between;
            color: var(--gray);
            font-size: 0.95rem;
            margin-top: 10px;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            border-top: 4px solid var(--accent);
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .project-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-description {
            font-size: 1rem;
            color: var(--gray);
            margin-bottom: 15px;
            line-height: 1.6;
        }

        .certifications-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }

        .certification-item {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            border-right: 4px solid var(--accent);
        }

        .certification-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--dark);
        }

        .certification-issuer {
            color: var(--secondary);
            font-size: 1rem;
        }

        .footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .header {
                padding: 30px 20px;
            }

            .name {
                font-size: 2.2rem;
            }

            .title {
                font-size: 1.2rem;
            }

            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }

            .resume-body {
                padding: 30px 20px;
            }

            .skills-container,
            .education-grid,
            .project-grid,
            .certifications-list {
                grid-template-columns: 1fr;
            }
        }

        /* Animation effects */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section {
            animation: fadeIn 0.6s ease-out forwards;
        }

        .section:nth-child(2) { animation-delay: 0.1s; }
        .section:nth-child(3) { animation-delay: 0.2s; }
        .section:nth-child(4) { animation-delay: 0.3s; }
        .section:nth-child(5) { animation-delay: 0.4s; }
        .section:nth-child(6) { animation-delay: 0.5s; }

        .skill-item, .project-card, .education-item, .certification-item {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body>
    <div class="resume-container">
        <header class="header">
            <h1 class="name">Prince Tiwari</h1>
            <div class="title">Software Developer | Web Developer</div>

            <div class="contact-info">
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <span>+91 6203811578</span>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <span>tiwariprince340@gmail.com</span>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <span>Gopalganj, Bihar</span>
                </div>
            </div>
        </header>

        <div class="resume-body">
            <!-- Career Objective Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-bullseye"></i> Career Objective
                </h2>
                <div class="section-content">
                    <p class="career-objective">
                        Looking for a role to utilize my
                        technical skills for the growth of
                        the organization as well as to
                        enhance my knowledge.
                    </p>
                </div>
            </section>

            <!-- Technical Skills Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-laptop-code"></i> Technical & Skills
                </h2>
                <div class="section-content">
                    <div class="skills-container">
                        <div class="skill-category">
                            <h3><i class="fas fa-brain"></i> Core Concepts</h3>
                            <ul class="skill-list">
                                <li class="skill-item">Data Structures & Algorithms</li>
                                <li class="skill-item">Database Management System</li>
                                <li class="skill-item">Object-Oriented Programming</li>
                            </ul>
                        </div>


                        <div class="skill-category">
                            <h3><i class="fas fa-code"></i> Programming Languages</h3>
                            <ul class="skill-list">
                                <li class="skill-item">C</li>
                                <li class="skill-item">C++</li>
                                <li class="skill-item">Java</li>
                                <li class="skill-item">JavaScript</li>
                                <li class="skill-item">Python</li>
                            </ul>
                        </div>

                        <div class="skill-category">
                            <h3><i class="fas fa-tools"></i> Technologies & Tools</h3>
                            <ul class="skill-list">
                                <li class="skill-item">MySQL</li>
                                <li class="skill-item">GitHub</li>
                                <li class="skill-item">HTML5</li>
                                <li class="skill-item">CSS3</li>
                                <li class="skill-item">React</li>
                                <li class="skill-item">Node.js</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h3><i class="fas fa-brain"></i> PERSONAL ATTRIBUTE</h3>
                            <ul class="skill-list">
                                <li class="skill-item">Adaptability</li>
                                <li class="skill-item">Communication</li>
                                <li class="skill-item">Problem-solving</li>
                                <li class="skill-item">Leadership</li>
                                <li class="skill-item">Teamwork</li>
                            </ul>
                        </div>

                    </div>
                </div>

            </section>


            <!-- Education Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-graduation-cap"></i> Education
                </h2>
                <div class="section-content">
                    <div class="education-grid">
                        <div class="education-item">
                            <div class="education-title">Master of Computer Applications (MCA)</div>
                            <div class="education-subtitle">Galgotias University</div>
                            <div class="education-meta">
                                <span>2024 - 2026</span>
                                <span>Greater Noida, UP</span>
                            </div>
                        </div>

                        <div class="education-item">
                            <div class="education-title">Bachelor of Computer Applications (BCA)</div>
                            <div class="education-subtitle">SunderDeep Group Of Instutations</div>
                            <div class="education-meta">
                                <span>2021 - 2024</span>
                                <span>Ghaziabad, UP</span>
                            </div>
                        </div>

                        <div class="education-item">
                            <div class="education-title">Senior Secondary (12th)</div>
                            <div class="education-subtitle">Mentors Eduserv</div>
                            <div class="education-meta">
                                <span>2019 - 2020</span>
                                <span>Patna, Bihar</span>
                            </div>
                        </div>

                        <div class="education-item">
                            <div class="education-title">Secondary (10th)</div>
                            <div class="education-subtitle">St Merry Public Schol</div>
                            <div class="education-meta">
                                <span>2017 - 2018</span>
                                <span>Gopalganj, Bihar</span>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Projects Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-project-diagram"></i> Projects
                </h2>
                <div class="section-content">
                    <div class="project-grid">
                        <div class="project-card">
                            <h3 class="project-title">
                                <i class="fas fa-code"></i> Programming in Java
                            </h3>
                            <p class="project-description">
                                Developed multiple Java applications focusing on core programming concepts,
                                data structures, and algorithms. Implemented OOP principles to create modular
                                and reusable code.
                            </p>
                            <div class="skill-list">
                                <span class="skill-item">Java</span>
                                <span class="skill-item">OOP</span>
                                <span class="skill-item">Algorithms</span>
                            </div>
                        </div>

                        <div class="project-card">
                            <h3 class="project-title">
                                <i class="fas fa-dumbbell"></i> Gym Course Website
                            </h3>
                            <p class="project-description">
                                Designed and developed a responsive website for fitness enthusiasts featuring
                                workout programs, nutrition guides, and progress tracking.
                            </p>
                            <div class="skill-list">
                                <span class="skill-item">HTML/CSS</span>
                                <span class="skill-item">JavaScript</span>
                                <span class="skill-item">Node.js</span>
                            </div>
                        </div>

                        <div class="project-card">
                            <h3 class="project-title">
                                <i class="fas fa-book"></i> Find My Notes
                            </h3>
                            <p class="project-description">
                                Created an educational platform for students to access and share study materials
                                across various subjects. Features include search functionality, categorization,
                                and user ratings.
                            </p>
                            <div class="skill-list">
                                <span class="skill-item">React</span>
                                <span class="skill-item">MySQL</span>
                                <span class="skill-item">API Integration</span>
                            </div>
                        </div>
                        <div class="project-card">
                            <h3 class="project-title">
                                <i class="fas fa-dumbbell"></i> Health Care Application
                            </h3>
                            <p class="project-description">
                                A Web App that recommends Health Tips and provide
                                Online health supplement And Suggest Diet Plane with many more Advancde features that will help in Daily Life.
                            </p>
                            <div class="skill-list">
                                <span class="skill-item">HTML/CSS</span>
                                <span class="skill-item">JavaScript</span>
                                <span class="skill-item">Java</span>
                                <!-- <span class="skill-item">SQL</span> -->
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Certifications Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-award"></i> Certifications
                </h2>
                <div class="section-content">
                    <div class="certifications-list">
                        <div class="certification-item">
                            <div class="certification-title">Programming in Java</div>
                            <div class="certification-issuer">ACSM</div>
                        </div>

                        <div class="certification-item">
                            <div class="certification-title">Programming in C++</div>
                            <div class="certification-issuer">SDGI Ghaziabad</div>
                        </div>

                        <div class="certification-item">
                            <div class="certification-title">Developing Soft Skills and Personality</div>
                            <div class="certification-issuer">SDGI Ghaziabad</div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Work Experience Section -->
            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-briefcase"></i> Work Experience
                </h2>
                <div class="section-content">
                    <div class="education-item">
                        <div class="education-title">Fresher</div>
                        <div class="education-subtitle">Seeking Entry-Level Opportunities</div>
                        <p style="margin-top: 10px; color: var(--gray);">
                            Eager to apply technical knowledge and problem-solving skills in a professional
                            environment. Quick learner with strong foundational knowledge in Software Development & Web Development.
                        </p>
                    </div>
                </div>
            </section>
        </div>

        <footer class="footer">
            <p>Designed with ❤️ | Prince Tiwari | 2025</p>
        </footer>
    </div>
</body>
</html>
