<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Simulator Pro</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a3a, #2c3e50);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .container {
            max-width: 1000px;
            width: 90%;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
            margin: 20px auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            background: linear-gradient(to right, #1abc9c, #3498db);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .tagline {
            font-size: 1.4rem;
            opacity: 0.9;
            max-width: 700px;
            margin: 0 auto 25px;
            line-height: 1.6;
        }
        
        .description-box {
            background: rgba(0, 0, 0, 0.2);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 40px;
        }
        
        .description-box h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #1abc9c;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .description-box p {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 20px;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }
        
        .feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .feature-card i {
            font-size: 2.5rem;
            color: #3498db;
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #1abc9c;
        }
        
        .feature-card p {
            font-size: 1.1rem;
            line-height: 1.6;
            opacity: 0.9;
        }
        
        .tech-stack {
            background: rgba(0, 0, 0, 0.2);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 40px;
        }
        
        .tech-stack h2 {
            font-size: 2rem;
            margin-bottom: 25px;
            color: #1abc9c;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            margin-top: 20px;
        }
        
        .tech-icon {
            background: rgba(255, 255, 255, 0.05);
            width: 100px;
            height: 100px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .tech-icon:hover {
            transform: scale(1.1);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .tech-icon i {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #3498db;
        }
        
        .tech-icon span {
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        .github-link {
            display: inline-block;
            background: linear-gradient(to right, #1abc9c, #3498db);
            color: white;
            text-decoration: none;
            font-size: 1.3rem;
            font-weight: 600;
            padding: 18px 40px;
            border-radius: 50px;
            margin-top: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .github-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            opacity: 0.8;
            font-size: 1.1rem;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .description-box, .tech-stack {
                padding: 20px;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Portfolio Simulator Pro</h1>
            <p class="tagline">Advanced portfolio growth simulation with customizable trading strategies</p>
        </header>
        
        <div class="description-box">
            <h2><i class="fas fa-info-circle"></i> Project Description</h2>
            <p>Portfolio Simulator Pro is a sophisticated web application designed to simulate portfolio growth through repeated transactions with customizable parameters. It enables traders and investors to test strategies by simulating daily transactions with variable gain percentages.</p>
            <p>The application features a professional interface with bilingual support (English/Romanian), detailed performance analytics, and comprehensive transaction reporting. Users can customize initial portfolio value, simulation duration, trades per day, and gain percentage ranges to model various trading scenarios.</p>
        </div>
        
        <div class="features">
            <div class="feature-card">
                <i class="fas fa-sliders-h"></i>
                <h3>Customizable Parameters</h3>
                <p>Set initial portfolio value, simulation duration (days/months/years), trades per day, and gain percentage ranges to match your trading strategy.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-chart-line"></i>
                <h3>Detailed Analytics</h3>
                <p>Get comprehensive performance reports including initial value, final value, total profit, and portfolio growth percentage with visual highlights.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-table"></i>
                <h3>Transaction Tracking</h3>
                <p>View detailed transaction records showing day, trade number, gain percentage, profit per trade, and updated portfolio value after each transaction.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-language"></i>
                <h3>Bilingual Interface</h3>
                <p>Switch seamlessly between English and Romanian with the language toggle. All interface elements are fully translated for both languages.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-mobile-alt"></i>
                <h3>Responsive Design</h3>
                <p>Fully responsive layout that works perfectly on desktops, tablets, and mobile devices with a professional, modern aesthetic.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-random"></i>
                <h3>Randomized Simulation</h3>
                <p>Simulations use randomized gain percentages within user-defined ranges to model real-world trading variability and uncertainty.</p>
            </div>
        </div>
        
        <div class="tech-stack">
            <h2><i class="fas fa-code"></i> Technology Stack</h2>
            <p>The application is built with modern web technologies:</p>
            
            <div class="tech-icons">
                <div class="tech-icon">
                    <i class="fab fa-html5"></i>
                    <span>HTML5</span>
                </div>
                <div class="tech-icon">
                    <i class="fab fa-css3-alt"></i>
                    <span>CSS3</span>
                </div>
                <div class="tech-icon">
                    <i class="fab fa-js"></i>
                    <span>JavaScript</span>
                </div>
                <div class="tech-icon">
                    <i class="fab fa-font-awesome"></i>
                    <span>Font Awesome</span>
                </div>
                <div class="tech-icon">
                    <i class="fas fa-mobile-alt"></i>
                    <span>Responsive</span>
                </div>
            </div>
        </div>
        
        <div style="text-align: center; margin-top: 30px;">
            <a href="https://github.com/yourusername/portfolio-simulator-pro" class="github-link" target="_blank">
                <i class="fab fa-github"></i> View on GitHub
            </a>
        </div>
    </div>
    
    <footer>
        <p>Portfolio Simulator Pro | An advanced trading strategy simulation tool</p>
    </footer>
</body>
</html>
