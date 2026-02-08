<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepeka Gurunathan - Lead Data Scientist | AI/ML Engineer</title>
    <style>
        /* CSS Variables for Theme */
        :root {
            --bg-color: #ffffff;
            --text-color: #333333;
            --secondary-bg: #f8f9fa;
            --card-bg: #ffffff;
            --border-color: #e0e0e0;
            --link-color: #0066cc;
            --link-hover: #004999;
            --header-bg: #2c3e50;
            --header-text: #ffffff;
            --shadow: rgba(0, 0, 0, 0.1);
            --code-bg: #f4f4f4;
            --highlight-bg: #e3f2fd;
        }

        [data-theme="dark"] {
            --bg-color: #1a1a1a;
            --text-color: #e0e0e0;
            --secondary-bg: #2d2d2d;
            --card-bg: #252525;
            --border-color: #404040;
            --link-color: #4d9fff;
            --link-hover: #80b3ff;
            --header-bg: #1a252f;
            --header-text: #e0e0e0;
            --shadow: rgba(0, 0, 0, 0.4);
            --code-bg: #2d2d2d;
            --highlight-bg: #1e3a5f;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background-color: var(--bg-color);
            color: var(--text-color);
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        /* Theme Toggle Button */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--secondary-bg);
            border: 2px solid var(--border-color);
            border-radius: 50px;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 24px;
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px var(--shadow);
        }

        .theme-toggle:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 12px var(--shadow);
        }

        /* Header */
        header {
            background: var(--header-bg);
            color: var(--header-text);
            padding: 2rem 0;
            text-align: center;
            transition: background-color 0.3s ease;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 1rem 0;
            border: 4px solid var(--header-text);
        }

        /* Navigation */
        nav {
            background: var(--secondary-bg);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 999;
            box-shadow: 0 2px 4px var(--shadow);
            transition: background-color 0.3s ease;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        nav a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--link-color);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Sections */
        section {
            margin: 3rem 0;
            padding: 2rem;
            background: var(--card-bg);
            border-radius: 8px;
            box-shadow: 0 2px 8px var(--shadow);
            transition: background-color 0.3s ease, box-shadow 0.3s ease;
        }

        section h2 {
            color: var(--link-color);
            border-bottom: 3px solid var(--link-color);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
        }

        /* Project Cards */
        .project {
            margin: 2rem 0;
            padding: 1.5rem;
            background: var(--secondary-bg);
            border-radius: 8px;
            border-left: 4px solid var(--link-color);
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .project:hover {
            transform: translateX(5px);
        }

        .project h3 {
            color: var(--link-color);
            margin-bottom: 1rem;
        }

        .project img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin: 1rem 0;
            box-shadow: 0 4px 12px var(--shadow);
        }

        .project ul {
            margin-left: 2rem;
            margin-top: 1rem;
        }

        .project li {
            margin: 0.5rem 0;
        }

        /* Skills & Experience */
        .experience-item, .education-item {
            margin: 1.5rem 0;
            padding: 1rem;
            background: var(--secondary-bg);
            border-radius: 6px;
            transition: background-color 0.3s ease;
        }

        .experience-item h3, .education-item h3 {
            color: var(--link-color);
            margin-bottom: 0.5rem;
        }

        .date {
            color: var(--text-color);
            opacity: 0.7;
            font-style: italic;
        }

        /* Links */
        a {
            color: var(--link-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--link-hover);
            text-decoration: underline;
        }

        /* Contact Badges */
        .contact-badges {
            display: flex;
            gap: 1rem;
            align-items: center;
            flex-wrap: wrap;
        }

        .contact-badges img {
            transition: transform 0.3s ease;
        }

        .contact-badges img:hover {
            transform: scale(1.1);
        }

        /* Back to Top */
        .back-to-top {
            text-align: center;
            margin: 2rem 0;
            padding: 1rem;
        }

        .back-to-top a {
            display: inline-block;
            padding: 0.8rem 2rem;
            background: var(--link-color);
            color: white;
            border-radius: 25px;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .back-to-top a:hover {
            background: var(--link-hover);
            transform: translateY(-2px);
            text-decoration: none;
        }

        /* Tech Stack Tags */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tech-tag {
            background: var(--highlight-bg);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: background-color 0.3s ease;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8rem;
            }

            nav ul {
                gap: 1rem;
            }

            .container {
                padding: 1rem;
            }

            section {
                padding: 1rem;
            }

            .theme-toggle {
                top: 10px;
                right: 10px;
                padding: 8px 15px;
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Theme Toggle Button -->
    <button class="theme-toggle" id="theme-toggle" aria-label="Toggle dark mode">
        <span class="sun">☀️</span>
        <span class="moon" style="display: none;">🌙</span>
    </button>

    <!-- Header -->
    <header id="home">
        <h1>Lead Data Scientist | AI/ML Engineer</h1>
        <img src="https://github.com/deepekaguru/Portfolio/blob/main/profile.png?raw=true" alt="Deepeka Gurunathan" class="profile-img">
        <h2>Deepeka Gurunathan</h2>
    </header>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about-me">About Me</a></li>
            <li><a href="#education-section">Education</a></li>
            <li><a href="#work-experience">Work Experience</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Main Content -->
    <div class="container">
        <!-- About Me Section -->
        <section id="about-me">
            <h2>About Me</h2>
            <p>Lead Data Scientist with 9+ years of experience across data science, machine learning, data engineering, and applied AI in healthcare, banking, and large-scale analytics environments. I specialize in building end-to-end AI systems—from scalable ETL and MLOps pipelines to production-grade ML and AI-driven solutions.</p>
            
            <p>I've worked across healthcare, pharma, banking, and telecommunications, transforming complex, high-volume datasets into reliable models and analytics platforms that improve accuracy, efficiency, and data-driven decision-making at scale.</p>
            
            <p>Currently pursuing an MS in Advanced Data Analytics (GPA: 4.0) while serving as a Graduate Teaching Assistant and Research Assistant. My work focuses on machine learning, statistical modeling, simulation, and applied AI, including AI-driven automation and intelligent validation frameworks.</p>
            
            <p>I'm particularly interested in applying Machine Learning, Generative AI, and scalable AI systems to solve complex, real-world problems in healthcare, analytics platforms, and intelligent automation.</p>
            
            <p><strong>Always open to connecting and discussing data, AI, and applied machine learning.</strong></p>
        </section>

        <!-- Education Section -->
        <section id="education-section">
            <h2>Education</h2>
            <div class="education-item">
                <h3>MS, Advanced Data Analytics</h3>
                <p>University of North Texas, Denton</p>
                <p class="date">Expected May 2026 | GPA: 4.0</p>
            </div>
            <div class="education-item">
                <h3>B.E Computer Science</h3>
                <p>Anna University, India</p>
                <p class="date">June 2012</p>
            </div>
        </section>

        <!-- Work Experience Section -->
        <section id="work-experience">
            <h2>Work Experience</h2>
            
            <div class="experience-item">
                <h3>Senior Data Scientist</h3>
                <p><strong>Lloyds Bank</strong></p>
                <p class="date">December 2020 – May 2022</p>
            </div>

            <div class="experience-item">
                <h3>Data Scientist</h3>
                <p><strong>GlaxoSmithKline</strong></p>
                <p class="date">August 2018 – December 2020</p>
            </div>

            <div class="experience-item">
                <h3>Data Engineer</h3>
                <p><strong>UnitedHealth Group</strong></p>
                <p class="date">August 2016 – July 2018</p>
            </div>

            <div class="experience-item">
                <h3>ETL Developer</h3>
                <p><strong>Telkomsel</strong></p>
                <p class="date">March 2013 – July 2016</p>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h2>Projects</h2>

            <!-- Project 1 -->
            <div class="project">
                <h3>1. Agentic AI - Clinical Trial Research Agent</h3>
                <img src="https://raw.githubusercontent.com/deepekaguru/Portfolio/main/Medical-research-agent.png" alt="Clinical Trial Research Agent">
                
                <p><strong>Key Highlights:</strong></p>
                <ul>
                    <li><strong>Local Execution:</strong> Runs entirely on-device (via Ollama) to ensure 100% data privacy—a critical requirement for healthcare applications.</li>
                    <li><strong>Stateful Orchestration:</strong> Utilizes LangGraph to manage complex cycles between reasoning, tool usage (API calls), and safety verification.</li>
                    <li><strong>Built-in Safety:</strong> Features an integrated Safety Node that detects high-risk medical queries and automatically appends regulatory disclaimers.</li>
                    <li><strong>Interactive Dashboard:</strong> A custom Streamlit UI that provides clickable links to official NIH study records and live status tracking of the agent's "thinking" process.</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">LangGraph</span>
                    <span class="tech-tag">Llama 3.2 (Ollama)</span>
                    <span class="tech-tag">Streamlit</span>
                    <span class="tech-tag">ClinicalTrials.gov API</span>
                    <span class="tech-tag">Custom CSS</span>
                </div>
            </div>

            <!-- Project 2 -->
            <div class="project">
                <h3>2. Integrated Business Analytics Dashboard (PostgreSQL + Power BI)</h3>
                <img src="https://raw.githubusercontent.com/deepekaguru/Portfolio/main/Postgresql_project.png" alt="Business Analytics Dashboard">
                
                <p>Designed and implemented an interactive Business Analytics dashboard using PostgreSQL and Power BI to analyze multi-domain business performance across sales, HR, and marketing.</p>
                
                <p><strong>Key Highlights:</strong></p>
                <ul>
                    <li>Developed normalized relational schema in PostgreSQL with sales, products, employees, departments, and campaign data.</li>
                    <li>Built Power BI connection via Npgsql for live data import and created measures using DAX for KPIs such as Total Revenue, ROI %, Average Transaction Value, Fraud Rate %, and Department Salary Analysis.</li>
                    <li>Designed interactive visuals including bar charts, line trends, donut charts, and KPIs to track product sales, employee performance, and fraud patterns.</li>
                    <li>Applied data storytelling principles to highlight key insights such as top-performing products, salary variance across departments, and monthly revenue fluctuations.</li>
                    <li>Delivered a professional end-to-end workflow: database design → data modeling → visualization → insight generation.</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">PostgreSQL</span>
                    <span class="tech-tag">Power BI</span>
                    <span class="tech-tag">DAX</span>
                    <span class="tech-tag">SQL</span>
                    <span class="tech-tag">Data Modeling</span>
                    <span class="tech-tag">Visualization</span>
                </div>
            </div>

            <!-- Project 3 -->
            <div class="project">
                <h3>3. DrugInfoGen – AI-Powered Drug Information Assistant</h3>
                <img src="https://raw.githubusercontent.com/deepekaguru/Portfolio/main/DrugInfoGen.png" alt="DrugInfoGen">
                
                <p>Built an interactive Streamlit application that generates human-readable drug information based on user-input drug names or selected health conditions. The app uses OpenAI's GPT-4 model to return structured details including usage, side effects, precautions, and summaries in markdown format.</p>
                
                <p><strong>Key Highlights:</strong></p>
                <ul>
                    <li>Integrated OpenAI's LLM to dynamically generate concise, patient-friendly medication details</li>
                    <li>Designed dual search modes: by drug name (typed input) and by condition (dropdown)</li>
                    <li>Used regex logic to extract and display markdown content into expandable Streamlit sections</li>
                    <li>Applied custom theming and CSS for a polished medical assistant-style user experience</li>
                    <li>Secured API key management with .env, and prepared app for deployment on Streamlit Cloud</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Streamlit</span>
                    <span class="tech-tag">OpenAI API (GPT-4)</span>
                    <span class="tech-tag">Regex</span>
                    <span class="tech-tag">dotenv</span>
                    <span class="tech-tag">Git</span>
                </div>
            </div>

            <!-- Project 4 -->
            <div class="project">
                <h3>4. Retail Sales Tax Forecasting - Machine Learning</h3>
                <img src="https://github.com/user-attachments/assets/5281054d-8adc-48b6-858d-af55beb9c671?raw=true" alt="Retail Sales Tax Forecasting">
                
                <p>Developed an interactive forecasting tool using Facebook Prophet to predict quarterly retail sales tax revenue across Iowa cities and counties. The app was built with Streamlit and enables users to select a location, define forecast horizons (1–8 quarters), and visualize trends using dynamic charts.</p>
                
                <p><strong>Key Highlights:</strong></p>
                <ul>
                    <li>Implemented time series modeling with Prophet, fine-tuned for quarterly seasonality</li>
                    <li>Calculated evaluation metrics including MAPE, MAE, RMSE, and R²</li>
                    <li>Designed a user-friendly interface with Streamlit, supporting tooltip guidance and data filtering</li>
                    <li>Deployed the interactive app on Streamlit Community Cloud with shareable forecasting visualizations</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Streamlit</span>
                    <span class="tech-tag">Facebook Prophet</span>
                    <span class="tech-tag">Pandas</span>
                    <span class="tech-tag">Matplotlib</span>
                    <span class="tech-tag">Plotly</span>
                    <span class="tech-tag">Scikit-learn</span>
                </div>
            </div>

            <!-- Project 5 -->
            <div class="project">
                <h3>5. Hospital Performance Dashboard - Power BI</h3>
                <img src="https://raw.githubusercontent.com/deepekaguru/Portfolio/main/Hospital-Dashboard.png" alt="Hospital Performance Dashboard">
                
                <ul>
                    <li>Designed and built an interactive hospital analytics dashboard using Power BI, providing insights into admissions, bed occupancy, and rejection trends of claims.</li>
                    <li>Optimized various DAX measures and Power Query transformations, including randomized patient IDs, age group categorization, and peak-hour designation.</li>
                    <li>Improved bed occupancy reporting by removing flawed calculations to yield hospital resource utilization real-time monitoring.</li>
                    <li>Processed claim denial patterns by insurance providers, establishing high-rejection carriers and emergency and urgent care admission trends.</li>
                    <li>Combined financial analyses, presenting insurance-paid funds vs. patient out-of-pocket costs, facilitating hospital billing and revenue analysis.</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">Power BI</span>
                    <span class="tech-tag">DAX</span>
                    <span class="tech-tag">Power Query</span>
                    <span class="tech-tag">Data Visualization</span>
                    <span class="tech-tag">Healthcare Analytics</span>
                </div>
            </div>

            <!-- Project 6 -->
            <div class="project">
                <h3>6. Personal Financial Dashboard - Microsoft Excel</h3>
                <img src="https://raw.githubusercontent.com/deepekaguru/Portfolio/main/Finance.png" alt="Personal Financial Dashboard">
                
                <ul>
                    <li>Created and optimized Pivot Tables and Pivot Charts, incorporating slicers for month-wise and category-wise filtering to enhance user experience.</li>
                    <li>Implemented dynamic calculations for Total Net Worth, Income Goal Progress, and Expense Tracking, leveraging advanced Excel functions and automated data aggregation.</li>
                    <li>Developed KPI tracking metrics, identifying max and min expenses, ensuring better financial decision-making and cost control.</li>
                    <li>Integrated income vs. expenses trend analysis through dual-line charts, enabling comparison of financial inflows and outflows.</li>
                    <li>Applied conditional formatting for highlighting overdue bills, spending patterns, and financial progress insights in real-time.</li>
                    <li>Suggested improvements, including automated debt tracking, forecasting financial trends, and enhanced data validation mechanisms for accurate financial planning.</li>
                </ul>
                
                <div class="tech-stack">
                    <span class="tech-tag">Excel</span>
                    <span class="tech-tag">Pivot Tables</span>
                    <span class="tech-tag">Data Visualization</span>
                    <span class="tech-tag">Financial Analytics</span>
                    <span class="tech-tag">Dashboard Design</span>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2>Contact</h2>
            <div class="contact-badges">
                <p><strong>E-mail:</strong> <a href="mailto:Deepekagurunathan@gmail.com">Deepekagurunathan@gmail.com</a></p>
                <a href="https://www.linkedin.com/in/deepeka-gurunathan/" target="_blank">
                    <img src="https://img.shields.io/badge/LinkedIn-Deepeka_Gurunathan-blue?style=flat&logo=linkedin" alt="LinkedIn">
                </a>
            </div>
        </section>

        <!-- Back to Top -->
        <div class="back-to-top">
            <a href="#home">Back To Top</a>
        </div>
    </div>

    <!-- JavaScript for Theme Toggle -->
    <script>
        // Theme toggle functionality
        const themeToggle = document.getElementById('theme-toggle');
        const html = document.documentElement;
        const sunIcon = document.querySelector('.sun');
        const moonIcon = document.querySelector('.moon');

        // Check for saved theme preference or default to light mode
        const currentTheme = localStorage.getItem('theme') || 'light';
        html.setAttribute('data-theme', currentTheme);

        // Update icon based on current theme
        if (currentTheme === 'dark') {
            sunIcon.style.display = 'none';
            moonIcon.style.display = 'inline';
        }

        // Toggle theme on button click
        themeToggle.addEventListener('click', () => {
            const currentTheme = html.getAttribute('data-theme');
            const newTheme = currentTheme === 'light' ? 'dark' : 'light';
            
            html.setAttribute('data-theme', newTheme);
            localStorage.setItem('theme', newTheme);
            
            // Toggle icons
            if (newTheme === 'dark') {
                sunIcon.style.display = 'none';
                moonIcon.style.display = 'inline';
            } else {
                sunIcon.style.display = 'inline';
                moonIcon.style.display = 'none';
            }
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
