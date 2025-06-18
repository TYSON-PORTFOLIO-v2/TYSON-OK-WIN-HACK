<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TYSON MODS - Live Ping</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0c1d30 0%, #0a1523 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            color: #fff;
        }
        
        .container {
            width: 100%;
            max-width: 400px;
            background: linear-gradient(145deg, #0d2135 0%, #0b1829 100%);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid #1a3a5f;
            position: relative;
        }
        
        .header {
            padding: 25px 20px 15px;
            text-align: center;
            background: linear-gradient(to right, #0a2a4a, #0c1d30);
            position: relative;
        }
        
        .header h1 {
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(to right, #4facfe, #00f2fe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }
        
        .header p {
            color: #5d8db9;
            font-size: 14px;
            letter-spacing: 1px;
        }
        
        .logo-img {
            height: 60px;
            margin-bottom: 10px;
        }
        
        .content {
            padding: 20px;
        }
        
        .country-info {
            display: flex;
            justify-content: space-between;
            background: rgba(10, 40, 70, 0.4);
            padding: 12px 15px;
            border-radius: 10px;
            margin-bottom: 20px;
            border: 1px solid #1a3a5f;
        }
        
        .country-info p {
            font-size: 16px;
        }
        
        .country-info span {
            color: #00d09c;
            font-weight: 600;
        }
        
        .win-notification {
            background: linear-gradient(to right, #0d2e4d, #0a213a);
            padding: 15px;
            border-radius: 12px;
            text-align: center;
            margin-bottom: 20px;
            border: 1px solid #1e456e;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .win-notification p {
            font-size: 18px;
        }
        
        .win-amount {
            color: #00d09c;
            font-weight: 700;
            font-size: 22px;
            letter-spacing: 1px;
            display: inline-block;
            transition: transform 0.3s ease;
        }
        
        hr {
            border: none;
            height: 1px;
            background: linear-gradient(to right, transparent, #1a3a5f, transparent);
            margin: 25px 0;
        }
        
        .version {
            text-align: center;
            font-weight: 600;
            font-size: 18px;
            margin-bottom: 25px;
            color: #4facfe;
            letter-spacing: 1px;
        }
        
        .server-info {
            background: rgba(10, 40, 70, 0.4);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 25px;
            border: 1px solid #1a3a5f;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        td {
            padding: 8px 0;
            font-size: 16px;
        }
        
        td:first-child {
            color: #8da5c0;
            width: 60%;
        }
        
        .active {
            color: #00d09c;
            font-weight: 600;
        }
        
        .result-container {
            background: rgba(10, 40, 70, 0.4);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 25px;
            text-align: center;
            border: 1px solid #1a3a5f;
        }
        
        .result-text {
            font-size: 16px;
            margin-bottom: 15px;
            color: #8da5c0;
        }
        
        .success-rate {
            font-size: 42px;
            font-weight: 800;
            background: linear-gradient(to bottom, #4facfe, #00f2fe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 5px 0;
        }
        
        .success-label {
            color: #8da5c0;
            font-size: 16px;
            letter-spacing: 1px;
        }
        
        .stats {
            display: flex;
            justify-content: space-between;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .stat-box {
            flex: 1;
            background: rgba(10, 40, 70, 0.4);
            border-radius: 10px;
            padding: 15px 10px;
            text-align: center;
            border: 1px solid #1a3a5f;
            position: relative;
            overflow: hidden;
        }
        
        .stat-number {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 5px;
            color: #00f2fe;
        }
        
        .stat-label {
            font-size: 14px;
            color: #8da5c0;
        }
        
        /* New Register Button */
        .register-btn {
            display: block;
            width: 100%;
            padding: 18px;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            border: none;
            border-radius: 12px;
            color: white;
            font-size: 22px;
            font-weight: 700;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(254, 180, 123, 0.4);
            position: relative;
            overflow: hidden;
            margin-bottom: 15px;
            text-decoration: none;
            text-align: center;
        }
        
        .register-btn span {
            display: block;
            font-size: 16px;
            font-weight: 500;
            margin-top: 5px;
            letter-spacing: 0.5px;
        }
        
        .register-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(254, 180, 123, 0.6);
        }
        
        .register-btn:active {
            transform: translateY(1px);
        }
        
        .register-pulse {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            animation: pulse 2s infinite;
            opacity: 0;
            border-radius: 12px;
        }
        
        .telegram-btn {
            display: block;
            width: 100%;
            padding: 18px;
            background: linear-gradient(to right, #0088cc, #00aced);
            border: none;
            border-radius: 12px;
            color: white;
            font-size: 22px;
            font-weight: 700;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 136, 204, 0.4);
            position: relative;
            overflow: hidden;
            text-decoration: none;
            text-align: center;
        }
        
        .telegram-btn span {
            display: block;
            font-size: 16px;
            font-weight: 500;
            margin-top: 5px;
            letter-spacing: 0.5px;
        }
        
        .telegram-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 136, 204, 0.6);
        }
        
        .telegram-btn:active {
            transform: translateY(1px);
        }
        
        .pulse {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            animation: pulse 2s infinite;
            opacity: 0;
            border-radius: 12px;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
                opacity: 0.5;
            }
            100% {
                transform: scale(1.5);
                opacity: 0;
            }
        }
        
        .footer {
            text-align: center;
            padding: 15px;
            color: #5d8db9;
            font-size: 12px;
            border-top: 1px solid #1a3a5f;
        }
        
        .period-input-container {
            background: rgba(10, 40, 70, 0.4);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #1a3a5f;
        }
        
        .period-input-container h3 {
            text-align: center;
            margin-bottom: 15px;
            color: #00f2fe;
            font-size: 18px;
        }
        
        .input-group {
            display: flex;
            gap: 10px;
        }
        
        #periodInput {
            flex: 1;
            padding: 12px 15px;
            border-radius: 8px;
            border: 1px solid #1a3a5f;
            background: rgba(10, 30, 50, 0.6);
            color: white;
            font-size: 16px;
            text-align: center;
        }
        
        #periodInput::placeholder {
            color: #5d8db9;
        }
        
        #calculateBtn {
            padding: 12px 20px;
            border-radius: 8px;
            border: none;
            background: linear-gradient(to right, #00d09c, #00b388);
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        #calculateBtn:hover {
            background: linear-gradient(to right, #00b388, #009672);
            transform: translateY(-2px);
        }
        
        .result-display {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
            padding: 15px;
            border-radius: 8px;
            background: rgba(10, 30, 50, 0.6);
            border: 1px solid #1a3a5f;
        }
        
        .result-item {
            text-align: center;
            flex: 1;
        }
        
        .result-value {
            font-size: 22px;
            font-weight: 700;
            margin-top: 5px;
            transition: transform 0.3s ease;
        }
        
        .big-result {
            color: #ff6b6b;
        }
        
        .small-result {
            color: #4facfe;
        }
        
        .result-label {
            font-size: 14px;
            color: #8da5c0;
        }
        
        .last-digits {
            color: #00f2fe;
            font-weight: 700;
        }
        
        .live-ping-container {
            background: rgba(10, 40, 70, 0.4);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #1a3a5f;
            text-align: center;
            position: relative;
        }
        
        .live-ping-header {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .live-indicator {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .live-dot {
            width: 10px;
            height: 10px;
            background-color: #ff4d4d;
            border-radius: 50%;
            animation: pulse-dot 1.5s infinite;
        }
        
        @keyframes pulse-dot {
            0% {
                transform: scale(1);
                opacity: 1;
            }
            50% {
                transform: scale(1.2);
                opacity: 0.7;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }
        
        .live-text {
            color: #ff4d4d;
            font-weight: 600;
            font-size: 18px;
        }
        
        .ping-display {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            background: rgba(10, 30, 50, 0.6);
            border-radius: 8px;
            border: 1px solid #1a3a5f;
        }
        
        .ping-value {
            font-size: 32px;
            font-weight: 700;
            background: linear-gradient(to right, #00f2fe, #4facfe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            min-width: 100px;
        }
        
        .ping-status {
            text-align: right;
            font-size: 14px;
        }
        
        .ping-status-text {
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .ping-status.excellent {
            color: #00d09c;
        }
        
        .ping-status.good {
            color: #4facfe;
        }
        
        .ping-status.fair {
            color: #ffcc00;
        }
        
        .ping-status.poor {
            color: #ff6b6b;
        }
        
        .ping-graph {
            height: 80px;
            margin-top: 15px;
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            background: rgba(0, 0, 0, 0.2);
            border: 1px solid #1a3a5f;
        }
        
        .graph-grid {
            position: absolute;
            width: 100%;
            height: 100%;
            background: 
                linear-gradient(to right, rgba(26, 58, 95, 0.3) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(26, 58, 95, 0.3) 1px, transparent 1px);
            background-size: 20px 20px;
        }
        
        .graph-line {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            stroke: #00f2fe;
            stroke-width: 2;
            fill: none;
        }
        
        .ping-history {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
            font-size: 12px;
            color: #8da5c0;
        }

        /* Win notification animation */
        @keyframes win-pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .win-notification {
            animation: win-pulse 1.5s ease-in-out infinite;
        }
        
        /* Counter animation */
        @keyframes counter-up {
            0% { transform: translateY(5px); opacity: 0; }
            100% { transform: translateY(0); opacity: 1; }
        }
        
        .counter-up {
            animation: counter-up 0.5s ease-out;
        }
        
        .update-indicator {
            position: absolute;
            top: 5px;
            right: 5px;
            background: rgba(0, 210, 156, 0.2);
            color: #00d09c;
            font-size: 10px;
            padding: 2px 5px;
            border-radius: 10px;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0% { opacity: 0.5; }
            50% { opacity: 1; }
            100% { opacity: 0.5; }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img src="https://via.placeholder.com/60x60/0d2135/00f2fe?text=TM" alt="TYSON MODS logo" class="logo-img">
            <h1>TYSON MODS</h1>
            <p>Real-time Network Performance Monitor</p>
        </div>
        
        <div class="content">
            <div class="country-info">
                <p>Country : <span>India</span></p>
                <p>Online Users : <span id="onlineUsers">3169</span></p>
            </div>
            
            <div class="win-notification">
                <p>User <span id="winningUser">665****796</span> Win <span class="win-amount" id="winAmount">₹5026</span></p>
            </div>
            
            <div class="live-ping-container">
                <div class="live-ping-header">
                    <div class="live-indicator">
                        <div class="live-dot"></div>
                        <div class="live-text">LIVE</div>
                    </div>
                </div>
                
                <div class="ping-display">
                    <div class="ping-value" id="pingValue">25ms</div>
                    <div class="ping-status excellent" id="pingStatus">
                        <div class="ping-status-text">Excellent</div>
                        <div>Connection</div>
                    </div>
                </div>
                
                <div class="ping-graph">
                    <div class="graph-grid"></div>
                    <svg class="graph-line" id="pingGraph"></svg>
                </div>
                
                <div class="ping-history">
                    <div>Last Ping: <span id="lastPing">25ms</span></div>
                    <div>Min: <span id="minPing">22ms</span></div>
                    <div>Max: <span id="maxPing">38ms</span></div>
                </div>
            </div>
            
            <div class="period-input-container">
                <h3>Period Number Analysis</h3>
                <div class="input-group">
                    <input type="number" id="periodInput" placeholder="Enter last 3 digits" min="0" max="999" maxlength="3">
                    <button id="calculateBtn">Calculate</button>
                </div>
                
                <div class="result-display">
                    <div class="result-item">
                        <div class="result-label">Big/Small</div>
                        <div class="result-value" id="bigSmallResult">-</div>
                    </div>
                    <div class="result-item">
                        <div class="result-label">Last 3 Digits</div>
                        <div class="result-value" id="lastDigits">-</div>
                    </div>
                </div>
            </div>
            
            <hr>
            
            <div class="version">TYSON MODS<br>V2.1.4</div>
            
            <div class="server-info">
                <table>
                    <tr>
                        <td>Server :</td>
                        <td class="active">Active</td>
                    </tr>
                    <tr>
                        <td>Ping:</td>
                        <td id="serverPing">25ms</td>
                    </tr>
                    <tr>
                        <td>CONTACT :</td>
                        <td>@TYSON_OWNER</td>
                    </tr>
                </table>
            </div>
            
            <div class="result-container">
                <p class="result-text">Result :(-) ~ 100%</p>
                <div class="success-rate">98.7%</div>
                <div class="success-label">Success Rate</div>
            </div>
            
            <div class="stats">
                <div class="stat-box">
                    <div class="update-indicator">LIVE</div>
                    <div class="stat-number" id="todayWins">207</div>
                    <div class="stat-label">Today's Wins</div>
                </div>
                <div class="stat-box">
                    <div class="update-indicator">LIVE</div>
                    <div class="stat-number" id="totalUsers">16.2K</div>
                    <div class="stat-label">Total Users</div>
                </div>
            </div>
            
            <!-- New Register Button -->
            <a href="https://www.okwin.game//#/register?invitationCode=565455654920" target="_blank" class="register-btn" id="registerBtn">
                REGISTER NOW
                <span>Create New ID to Win</span>
                <div class="register-pulse"></div>
            </a>
        
            <a href="https://t.me/TYSON_OK_WIN_HACK" target="_blank" class="telegram-btn" id="telegramBtn">
                START
                <span>JOIN TELEGRAM</span>
                <div class="pulse"></div>
            </a>
        </div>
        
        <div class="footer">
            © 2023 TYSON MODS | All Rights Reserved
        </div>
    </div>

    <script>
        // Initialize variables
        let onlineUsers = 3169;
        let totalUsers = 16200;
        let todayWins = 207;
        
        const winAmountElement = document.getElementById('winAmount');
        const onlineUsersElement = document.getElementById('onlineUsers');
        const totalUsersElement = document.getElementById('totalUsers');
        const todayWinsElement = document.getElementById('todayWins');
        const winningUserElement = document.getElementById('winningUser');
        
        // Update online users in real-time
        function updateOnlineUsers() {
            // Simulate user fluctuation
            const change = Math.floor(Math.random() * 11) - 5; // -5 to +5
            onlineUsers = Math.max(3000, onlineUsers + change);
            onlineUsersElement.textContent = onlineUsers.toLocaleString();
        }
        
        // Generate random 4-digit win amount
        function generateWinAmount() {
            return Math.floor(1000 + Math.random() * 9000);
        }
        
        // Generate random masked user ID
        function generateWinningUser() {
            const prefix = Math.floor(100 + Math.random() * 900);
            const suffix = Math.floor(100 + Math.random() * 900);
            return `${prefix}****${suffix}`;
        }
        
        // Update win notification
        function updateWinNotification() {
            const amount = generateWinAmount();
            const user = generateWinningUser();
            
            winAmountElement.textContent = `₹${amount}`;
            winningUserElement.textContent = user;
            
            // Animate the win amount
            winAmountElement.style.transform = 'scale(1.1)';
            setTimeout(() => {
                winAmountElement.style.transform = 'scale(1)';
            }, 300);
        }
        
        // Update Today's Wins and Total Users every minute
        function updateMinuteStats() {
            // Add random wins (5-15)
            const newWins = Math.floor(Math.random() * 11) + 5;
            todayWins += newWins;
            
            // Add random users (50-150)
            const newUsers = Math.floor(Math.random() * 101) + 50;
            totalUsers += newUsers;
            
            // Update DOM with animation
            todayWinsElement.textContent = todayWins;
            todayWinsElement.classList.add('counter-up');
            
            totalUsersElement.textContent = totalUsers > 10000 
                ? (totalUsers/1000).toFixed(1) + 'K' 
                : totalUsers.toLocaleString();
            totalUsersElement.classList.add('counter-up');
            
            // Remove animation class after animation completes
            setTimeout(() => {
                todayWinsElement.classList.remove('counter-up');
                totalUsersElement.classList.remove('counter-up');
            }, 500);
        }
        
        // Period calculation functionality
        document.getElementById('calculateBtn').addEventListener('click', function() {
            const input = document.getElementById('periodInput').value;
            
            if (!input || input.length !== 3 || isNaN(input)) {
                alert('Please enter a valid 3-digit number');
                return;
            }
            
            const digits = parseInt(input);
            
            // Update the last digits display
            document.getElementById('lastDigits').textContent = input;
            document.getElementById('lastDigits').classList.add('last-digits');
            
            // Calculate Big/Small
            const result = digits >= 500 ? 'BIG' : 'SMALL';
            const resultElement = document.getElementById('bigSmallResult');
            
            resultElement.textContent = result;
            resultElement.className = 'result-value';
            
            if (result === 'BIG') {
                resultElement.classList.add('big-result');
            } else {
                resultElement.classList.add('small-result');
            }
            
            // Add animation effect
            resultElement.style.transform = 'scale(1.2)';
            setTimeout(() => {
                resultElement.style.transform = 'scale(1)';
            }, 300);
        });
        
        // Input validation to ensure only 3 digits
        document.getElementById('periodInput').addEventListener('input', function() {
            if (this.value.length > 3) {
                this.value = this.value.slice(0, 3);
            }
        });
        
        // Live ping functionality
        const pingValue = document.getElementById('pingValue');
        const serverPing = document.getElementById('serverPing');
        const pingStatus = document.getElementById('pingStatus');
        const lastPing = document.getElementById('lastPing');
        const minPing = document.getElementById('minPing');
        const maxPing = document.getElementById('maxPing');
        const pingGraph = document.getElementById('pingGraph');
        
        let pingHistory = [25, 26, 24, 28, 25, 23, 27, 25, 26, 25];
        let minPingValue = 22;
        let maxPingValue = 38;
        
        // Initialize graph
        updateGraph();
        
        function updatePing() {
            // Simulate ping change
            const change = (Math.random() - 0.5) * 6;
            let newPing = pingHistory[pingHistory.length - 1] + change;
            
            // Keep ping within reasonable bounds
            newPing = Math.max(15, Math.min(60, Math.round(newPing)));
            
            // Update history
            pingHistory.push(newPing);
            if (pingHistory.length > 10) {
                pingHistory.shift();
            }
            
            // Update min/max
            minPingValue = Math.min(minPingValue, newPing);
            maxPingValue = Math.max(maxPingValue, newPing);
            
            // Update display
            pingValue.textContent = `${newPing}ms`;
            serverPing.textContent = `${newPing}ms`;
            lastPing.textContent = `${newPing}ms`;
            minPing.textContent = `${minPingValue}ms`;
            maxPing.textContent = `${maxPingValue}ms`;
            
            // Update status
            pingStatus.className = 'ping-status ';
            if (newPing < 30) {
                pingStatus.classList.add('excellent');
                pingStatus.querySelector('.ping-status-text').textContent = 'Excellent';
            } else if (newPing < 40) {
                pingStatus.classList.add('good');
                pingStatus.querySelector('.ping-status-text').textContent = 'Good';
            } else if (newPing < 50) {
                pingStatus.classList.add('fair');
                pingStatus.querySelector('.ping-status-text').textContent = 'Fair';
            } else {
                pingStatus.classList.add('poor');
                pingStatus.querySelector('.ping-status-text').textContent = 'Poor';
            }
            
            // Update graph
            updateGraph();
        }
        
        function updateGraph() {
            const svgNS = "http://www.w3.org/2000/svg";
            pingGraph.innerHTML = '';
            
            const width = pingGraph.clientWidth;
            const height = pingGraph.clientHeight;
            const maxPingInHistory = Math.max(...pingHistory);
            const minPingInHistory = Math.min(...pingHistory);
            const range = Math.max(20, maxPingInHistory - minPingInHistory);
            
            const points = [];
            for (let i = 0; i < pingHistory.length; i++) {
                const x = (i / (pingHistory.length - 1)) * width;
                const y = height - ((pingHistory[i] - minPingInHistory) / range) * height * 0.8;
                points.push(`${x},${y}`);
            }
            
            const polyline = document.createElementNS(svgNS, 'polyline');
            polyline.setAttribute('points', points.join(' '));
            polyline.setAttribute('class', 'graph-line');
            pingGraph.appendChild(polyline);
        }
        
        // Set up intervals for dynamic updates
        setInterval(updateOnlineUsers, 3000); // Update online users every 3 seconds
        setInterval(updateWinNotification, 8000); // Update win notification every 8 seconds
        setInterval(updatePing, 2000); // Update ping every 2 seconds
        setInterval(updateMinuteStats, 60000); // Update minute stats every 60 seconds
        
        // Initial updates
        updateOnlineUsers();
        updateWinNotification();
        updatePing();
        updateMinuteStats(); // Initialize the minute stats
        
        // Update graph on resize
        window.addEventListener('resize', updateGraph);
    </script>
</body>
</html>
