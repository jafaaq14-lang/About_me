<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aaqil Jaffer | Systems & Software Architecture</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,300;0,400;0,700;1,400&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- Core System Variables & Themes --- */
        :root[data-theme="dark"] {
            --bg-primary: #0F172A;
            --bg-secondary: #1E293B;
            --bg-terminal: #020617;
            --border-color: #334155;
            --accent-color: #10B981; /* Precision Emerald */
            --accent-glow: rgba(16, 185, 129, 0.15);
            --text-main: #F8FAFC;
            --text-muted: #94A3B8;
            --terminal-user: #38BDF8;
        }

        :root[data-theme="light"] {
            --bg-primary: #F8FAFC;
            --bg-secondary: #FFFFFF;
            --bg-terminal: #0F172A;
            --border-color: #E2E8F0;
            --accent-color: #0070F3; /* Vercel Blue */
            --accent-glow: rgba(0, 112, 243, 0.1);
            --text-main: #0F172A;
            --text-muted: #64748B;
            --terminal-user: #38BDF8;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s ease, border-color 0.3s ease, color 0.3s ease;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, .mono {
            font-family: 'JetBrains Mono', monospace;
            font-weight: 600;
        }

        /* --- Header / Branding --- */
        header {
            background-color: var(--bg-secondary);
            border-bottom: 1px solid var(--border-color);
            padding: 24px 40px;
            position: sticky;
            top: 0;
            z-index: 90;
            backdrop-filter: blur(8px);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .logo {
            font-size: 1.75rem;
            letter-spacing: -0.05em;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--accent-color);
        }

        .subtitle {
            color: var(--text-muted);
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        /* --- Hero Section (System Terminal Mockup) --- */
        .hero {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .terminal-container {
            background-color: var(--bg-terminal);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            overflow: hidden;
        }

        .terminal-header {
            background-color: rgba(255, 255, 255, 0.03);
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
            padding: 12px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .terminal-buttons {
            display: flex;
            gap: 8px;
        }

        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        .dot-red { background-color: #EF4444; }
        .dot-yellow { background-color: #F59E0B; }
        .dot-green { background-color: #10B981; }

        .terminal-title {
            color: #64748B;
            font-size: 0.85rem;
            font-family: 'JetBrains Mono', monospace;
        }

        .terminal-body {
            padding: 24px;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.95rem;
            color: #E2E8F0;
            min-height: 280px;
        }

        .terminal-line {
            margin-bottom: 10px;
            white-space: pre-wrap;
        }

        .prompt-user { color: var(--terminal-user); }
        .prompt-loc { color: var(--text-muted); }
        .prompt-sign { color: var(--accent-color); }
        
        .output-success { color: #10B981; }
        .output-info { color: #38BDF8; }

        /* --- Interactive Categories --- */
        .categories-nav {
            max-width: 1200px;
            margin: 40px auto 20px;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 16px;
        }

        .btn-console {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 18px 24px;
            border-radius: 8px;
            cursor: pointer;
            text-align: left;
            display: flex;
            align-items: center;
            gap: 14px;
            font-size: 1rem;
            font-weight: 500;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05);
        }

        .btn-console:hover {
            border-color: var(--accent-color);
            background-color: rgba(255, 255, 255, 0.02);
        }

        .btn-console.active {
            border-color: var(--accent-color);
            background-color: var(--accent-glow);
            box-shadow: inset 0 0 12px var(--accent-glow);
        }

        .btn-icon {
            font-size: 1.25rem;
        }

        /* --- Content Layout --- */
        .content-section {
            max-width: 1200px;
            margin: 0 auto 60px;
            padding: 0 20px;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 24px;
            opacity: 1;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .card {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 28px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
        }

        .card-header-group {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 16px;
        }

        .card h3 {
            color: var(--text-main);
            font-size: 1.2rem;
        }

        .card .tag {
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.75rem;
            background-color: rgba(255, 255, 255, 0.05);
            padding: 4px 8px;
            border-radius: 4px;
            border: 1px solid var(--border-color);
            color: var(--text-muted);
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 20px;
        }

        .metric-list {
            list-style: none;
        }

        .metric-item {
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 8px;
            color: var(--text-main);
        }

        .metric-item::before {
            content: "→";
            color: var(--accent-color);
        }

        /* --- Fixed Floating Action Button --- */
        #logic-toggle-btn {
            position: fixed;
            bottom: 32px;
            right: 32px;
            background-color: var(--bg-secondary);
            border: 1px solid var(--accent-color);
            color: var(--accent-color);
            width: 56px;
            height: 56px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            box-shadow: 0 10px 25px -5px rgba(0,0,0,0.3), 0 0 15px var(--accent-glow);
        }

        #logic-toggle-btn:hover {
            transform: scale(1.05);
        }

        /* --- Footer --- */
        footer {
            background-color: var(--bg-secondary);
            border-top: 1px solid var(--border-color);
            padding: 40px 20px;
            margin-top: 80px;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            text-align: center;
        }

        .footer-links {
            display: flex;
            gap: 32px;
        }

        .footer-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-links a:hover {
            color: var(--accent-color);
        }

        .copyright {
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        /* --- Responsive Viewport Modifications --- */
        @media (max-width: 768px) {
            header { padding: 20px; }
            .categories-nav { grid-template-columns: 1fr; }
            .grid-container { grid-template-columns: 1fr; }
            #logic-toggle-btn { bottom: 20px; right: 20px; width: 48px; height: 48px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-container">
            <h1 class="logo">AAQIL JAFFER<span>.</span></h1>
            <div class="subtitle">Systems Architecture // Cybersecurity Diagnostics // Software Engineering</div>
        </div>
    </header>

    <main class="hero">
        <div class="terminal-container">
            <div class="terminal-header">
                <div class="terminal-buttons">
                    <div class="dot dot-red"></div>
                    <div class="dot dot-yellow"></div>
                    <div class="dot dot-green"></div>
                </div>
                <div class="terminal-title">core_engine_diagnostic.sh</div>
                <div></div>
            </div>
            <div class="terminal-body" id="terminal-output">
                <div class="terminal-line"><span class="prompt-user">visitor</span><span class="prompt-loc">@jaffer-node</span><span class="prompt-sign">:$</span> ./initialize_portfolio</div>
                <div class="terminal-line output-info">[SYSTEM] Initializing neutral logical verification engine...</div>
                <div class="terminal-line output-success">[SUCCESS] Environment loaded status: 100% integral.</div>
                <div class="terminal-line">[METRICS] Host active: Metro State Core Network node.</div>
                <div class="terminal-line"><span class="prompt-user">visitor</span><span class="prompt-loc">@jaffer-node</span><span class="prompt-sign">:$</span> <span id="typing-effect"></span></div>
            </div>
        </div>
    </main>

    <nav class="categories-nav">
        <button class="btn-console active" onclick="showCategory('cloud')" id="btn-cloud">
            <span class="btn-icon">🌐</span>
            <span>Cloud & Software</span>
        </button>
        <button class="btn-console" onclick="showCategory('security')" id="btn-security">
            <span class="btn-icon">🛡️</span>
            <span>Cybersecurity</span>
        </button>
        <button class="btn-console" onclick="showCategory('hardware')" id="btn-hardware">
            <span class="btn-icon">⚙️</span>
            <span>Hardware Systems</span>
        </button>
        <button class="btn-console" onclick="showCategory('logic')" id="btn-logic">
            <span class="btn-icon">🧠</span>
            <span>Logical Frameworks</span>
        </button>
    </nav>

    <section class="content-section">
        <div class="grid-container" id="dynamic-grid-target">
            </div>
    </section>

    <button id="logic-toggle-btn" onclick="toggleSystemTheme()" title="Toggle System Theme">🌓</button>

    <footer>
        <div class="footer-container">
            <div class="footer-links">
                <a href="https://github.com" target="_blank">
                    <span>🗂️</span> GitHub Repository
                </a>
                <a href="#" onclick="alert('System Notice: Integration point active.'); return false;">
                    <span>⚡</span> Vercel Status
                </a>
            </div>
            <p class="copyright">© 2026 Aaqil Jaffer | Built with structural logic and deployed via Vercel.</p>
        </div>
    </footer>

    <script>
        // Content Data Repositories Matched to Technical Footprint
        const categoryData = {
            cloud: [
                {
                    title: "Cloud Ecosystem Engineering",
                    tag: "Infrastructure",
                    desc: "Architecting cloud-native solutions across disparate ecosystems ensuring scalability and low-latency access patterns.",
                    metrics: ["AWS Deployment Architectures", "Azure Security Frameworks", "GCP Service Alignments"]
                },
                {
                    title: "Object-Oriented Concurrency",
                    tag: "Backend",
                    desc: "Developing robust backend services managing multi-threaded computational streams and race condition mitigation.",
                    metrics: ["Java Concurrency Engine Design", "Python Automation Protocols", "High-Throughput Rest APIs"]
                },
                {
                    title: "Relational Modeling",
                    tag: "Persistence",
                    desc: "Structuring schema frameworks to assure transactional atomicity, strict consistency, and query optimization.",
                    metrics: ["SQL Relational Architecture", "Query Optimization Vectors", "Schema Integrity Protocols"]
                }
            ],
            security: [
                {
                    title: "Threat Landscape Assessment",
                    tag: "Risk Diagnostics",
                    desc: "Systematic auditing of target attack vectors to lower surface vulnerability and align with standard frameworks.",
                    metrics: ["Active Risk Mitigation Modeling", "Vulnerability Surface Isolation", "NIST Compliance Reviews"]
                },
                {
                    title: "Network Inspection Frameworks",
                    tag: "Packet Analysis",
                    desc: "Deep packet observation and data stream carving to identify malicious network behaviors or anomalies.",
                    metrics: ["Wireshark Payload Deep Dives", "Packetbeat Log Telemetry", "Real-Time Traffic Parsing"]
                },
                {
                    title: "Passive & Active Network Discovery",
                    tag: "Auditing",
                    desc: "Mapping internal network topologies and parsing response codes to diagnose structural vulnerabilities.",
                    metrics: ["Nmap Port State Evaluation", "Kibana SIEM Analysis Layers", "Network Topology Mapping"]
                }
            ],
            hardware: [
                {
                    title: "FPGA Architecture Engineering",
                    tag: "VHDL Design",
                    desc: "Synthesizing precise digital logical engines implemented explicitly via hardware description frameworks.",
                    metrics: ["VHDL Structural Modeling", "XC7A100T Hardware Engineering", "Multi-Mode Gameplay Engines"]
                },
                {
                    title: "Sub-Tier Supply Chain Audits",
                    tag: "NIST SP 800-161",
                    desc: "Evaluating multi-layered supplier networks to trace hardware provenance and intercept logical corruption.",
                    metrics: ["Chain of Custody Verifications", "Sub-Tier Dependency Assessments", "Vulnerability Surface Indexing"]
                },
                {
                    title: "Advanced Component Security",
                    tag: "Hardware Trust",
                    desc: "Evaluating potential exploitation vectors across specialized, high-density physical modular layouts.",
                    metrics: ["2.5D Chiplet Boundary Analysis", "3D Interconnect Exploitation Checks", "Silicon Provenance Logic"]
                }
            ],
            logic: [
                {
                    title: "Axiomatic Break Resolution",
                    tag: "Münchhausen Trilemma",
                    desc: "Isolating systemic logical structural loops through structural regression and absolute axiomatic bounds.",
                    metrics: ["Infinite Regress Interception", "Circularity Diagnostic Models", "Dogmatic Axiomatic Definitions"]
                },
                {
                    title: "Integritism Core Architecture",
                    tag: "Systemic Truth",
                    desc: "Modeling abstract processing systems on immutable logical frameworks to limit data divergence.",
                    metrics: ["Data-to-Truth Synthesis Matrix", "Structural Logic Verifications", "Integritism Framework Mapping"]
                },
                {
                    title: "Framework Auditing Engine",
                    tag: "Metacognition",
                    desc: "Deploying structural observation mechanisms to identify cognitive biases or systemic alignment faults.",
                    metrics: ["Sensory Metaphor Conversion", "Cognitive Mechanics Isolations", "Dr. Kanojia Framework Mapping"]
                }
            ]
        };

        // UI View Updating State Engine
        function showCategory(categoryKey) {
            const gridTarget = document.getElementById('dynamic-grid-target');
            
            // Re-apply active class markers across navigation nodes
            document.querySelectorAll('.btn-console').forEach(btn => btn.classList.remove('active'));
            const selectedButton = document.getElementById(`btn-${categoryKey}`);
            if (selectedButton) selectedButton.classList.add('active');

            // Construct new dynamic node grid layout mapping the underlying array
            const dataSet = categoryData[categoryKey] || [];
            let generatedHtml = '';

            dataSet.forEach(item => {
                let metricsHtml = '';
                item.metrics.forEach(metric => {
                    metricsHtml += `<li class="metric-item">${metric}</li>`;
                });

                generatedHtml += `
                    <div class="card" style="animation: fadeIn 0.4s ease forwards;">
                        <div class="card-header-group">
                            <h3>${item.title}</h3>
                            <span class="tag">${item.tag}</span>
                        </div>
                        <p>${item.desc}</p>
                        <ul class="metric-list">
                            ${metricsHtml}
                        </ul>
                    </div>
                `;
            });

            gridTarget.innerHTML = generatedHtml;
            updateTerminalLog(categoryKey);
        }

        // Contextual Terminal Logging Engine
        function updateTerminalLog(categoryKey) {
            const textMap = {
                cloud: "cat cloud_architecture_manifest.json --query modules",
                security: "nmap -sV -T4 internal_audit_subnet.net && packetbeat -run",
                hardware: "ghdl -a --std=08 fpga_xc7a100t_core.vhdl",
                logic: "verify --system=integritism --resolution=trilemma"
            };
            
            const targetString = textMap[categoryKey] || "";
            const textContainer = document.getElementById('typing-effect');
            if (textContainer) {
                textContainer.textContent = targetString;
            }
        }

        // Theme Switcher Logic Engine (Dark/Light Custom Property Swapping)
        function toggleSystemTheme() {
            const rootElement = document.documentElement;
            const activeTheme = rootElement.getAttribute('data-theme');
            const targetTheme = (activeTheme === 'dark') ? 'light' : 'dark';
            rootElement.setAttribute('data-theme', targetTheme);
        }

        // DOM Domination Initialization Hook
        document.addEventListener('DOMContentLoaded', () => {
            showCategory('cloud');
        });
    </script>
</body>
</html>
