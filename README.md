# instagram-growth-tracker
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CreatorScale - Instagram 10K Growth & Monetization Tracker</title>
    <style>
        :root {
            --primary: #962fbf;
            --secondary: #4f5bd5;
            --gradient: linear-gradient(45deg, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
            --dark: #121212;
            --card-bg: #1e1e1e;
            --text: #ffffff;
            --muted: #aaaaaa;
            --success: #00fa9a;
            --accent-blue: #00d2ff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: var(--dark); color: var(--text); padding-bottom: 60px; }
        
        header {
            background: rgba(18, 18, 18, 0.8);
            backdrop-filter: blur(10px);
            padding: 20px;
            text-align: center;
            border-bottom: 1px solid #333;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        header h1 { font-size: 1.5rem; background: var(--gradient); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }

        .container { max-width: 800px; margin: 30px auto; padding: 0 20px; }
        
        .card {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 24px;
            margin-bottom: 24px;
            border: 1px solid #2a2a2a;
            box-shadow: 0 4px 15px rgba(0,0,0,0.5);
        }

        /* Executive Badge Styling */
        .executive-badge {
            border: 1px solid #3d3d3d;
            background: linear-gradient(135deg, #1e1e1e 0%, #252525 100%);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }
        .exec-info h3 { color: var(--accent-blue); font-size: 1.1rem; margin-bottom: 4px; }
        .exec-info p { margin: 0; font-size: 0.85rem; color: var(--muted); }
        .exec-contact a {
            color: #fff;
            background: #2a2a2a;
            padding: 8px 16px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: bold;
            border: 1px solid #444;
            display: inline-block;
            transition: background 0.2s;
        }
        .exec-contact a:hover { background: #3a3a3a; }

        h2 { font-size: 1.25rem; margin-bottom: 15px; color: #fff; display: flex; align-items: center; gap: 10px; }
        p { color: var(--muted); font-size: 0.95rem; line-height: 1.5; margin-bottom: 15px; }

        .input-group { display: flex; gap: 10px; margin-bottom: 20px; }
        input[type="number"] {
            flex: 1; padding: 12px; border-radius: 8px; border: 1px solid #444;
            background: #252525; color: #fff; font-size: 1rem; outline: none;
        }
        button {
            background: var(--gradient); color: #fff; border: none; padding: 12px 24px;
            border-radius: 8px; font-weight: bold; cursor: pointer; transition: transform 0.2s;
        }
        button:hover { transform: scale(1.02); }

        .progress-container { background: #333; height: 12px; border-radius: 6px; overflow: hidden; margin-top: 15px; }
        .progress-bar { background: var(--gradient); width: 0%; height: 100%; transition: width 0.5s ease-in-out; }

        .checklist-item { display: flex; align-items: flex-start; gap: 12px; margin-bottom: 12px; padding-bottom: 12px; border-bottom: 1px solid #2a2a2a; }
        .checklist-item input[type="checkbox"] { width: 18px; height: 18px; accent-color: #d6249f; cursor: pointer; margin-top: 3px; }
        .checklist-item label { font-size: 0.95rem; cursor: pointer; }
        .checklist-item span { display: block; font-size: 0.8rem; color: var(--muted); margin-top: 2px; }

        footer { text-align: center; margin-top: 40px; font-size: 0.8rem; color: var(--muted); line-height: 1.6; }
        footer a { color: #4f5bd5; text-decoration: none; margin: 0 10px; }
    </style>
</head>
<body>

    <header>
        <h1>🚀 CreatorScale</h1>
    </header>

    <div class="container">
        
        <!-- Executive Ownership Card -->
        <div class="card executive-badge">
            <div class="exec-info">
                <h3>👑 Executive Administration</h3>
                <p>Owner & CEO: <strong>KWIZERA Gad</strong></p>
                <p>Corporate Verification ID: Active Integration</p>
            </div>
            <div class="exec-contact">
                <a href="tel:0792927748">📞 Call HQ: 0792927748</a>
            </div>
        </div>

        <!-- Live Follower Milestone Tracker -->
        <div class="card">
            <h2>📈 10K Follower Roadmap Tracker</h2>
            <p>Enter your current follower count to generate your organic viral checklist adjustments dynamically.</p>
            <div class="input-group">
                <input type="number" id="currentFollowers" placeholder="e.g., 1250" min="0" max="10000">
                <button onclick="calculateProgress()">Update Status</button>
            </div>
            <div id="statsOutput" style="display: none;">
                <p>Progress to 10K: <strong id="percentageText" style="color: var(--success)">0%</strong></p>
                <div class="progress-container">
                    <div class="progress-bar" id="progressBar"></div>
                </div>
                <p style="margin-top: 10px; font-size: 0.85rem;" id="remainingText"></p>
            </div>
        </div>

        <!-- Legal Monetization Safety Audit -->
        <div class="card">
            <h2>⚖️ Legal & Policy Eligibility Pre-Check</h2>
            <p>Instagram checks your structural configurations before allowing native payouts. Confirm compliance below:</p>
            
            <div class="checklist-item">
                <input type="checkbox" id="rule1">
                <div>
                    <label for="rule1">Professional Account Enabled</label>
                    <span>Account type is manually set to "Creator" or "Business" inside Instagram Settings.</span>
                </div>
            </div>

            <div class="checklist-item">
                <input type="checkbox" id="rule2">
                <div>
                    <label for="rule2">Original & Transformative Assets Only</label>
                    <span>No unedited re-uploads from TikTok or Pinterest. Video metadata belongs entirely to you.</span>
                </div>
            </div>

            <div class="checklist-item">
                <input type="checkbox" id="rule3">
                <div>
                    <label for="rule3">Commercial Track Verification</label>
                    <span>Only original audio tracks or audios licensed strictly for business use are utilized in Reels.</span>
                </div>
            </div>

            <div class="checklist-item">
                <input type="checkbox" id="rule4">
                <div>
                    <label for="rule4">Clean Account Status (Zero Strikes)</label>
                    <span>No active Intellectual Property claims or Community Guideline flags under Account Status.</span>
                </div>
            </div>
        </div>

        <!-- Secure API Login Access Point -->
        <div class="card" style="text-align: center;">
            <h2>🔗 Connect Your Creator Account Securely</h2>
            <p>Ready to automate your monetization data pulls? When you deploy, configure Meta App OAuth securely here.</p>
            <button style="background: #252525; border: 1px solid #444;" onclick="alert('OAuth Platform: Managed by Executive Director KWIZERA Gad. Connect endpoints via production server scripts.')">
                🔒 Connect with Instagram API
            </button>
        </div>

        <footer>
            <p>© 2026 CreatorScale. All Rights Reserved.</p>
            <p>Authority Control: <strong>KWIZERA Gad (Owner & CEO)</strong> | Helpline: <strong>0792927748</strong></p>
            <p style="margin-top: 10px;">
                <a href="privacy.html">Privacy Policy</a> | 
                <a href="#terms">Terms of Service</a>
            </p>
        </footer>
    </div>

    <script>
        function calculateProgress() {
            const current = parseInt(document.getElementById('currentFollowers').value);
            const target = 10000;
            
            if (isNaN(current) || current < 0) {
                alert("Please enter a valid positive number.");
                return;
            }

            const safeCurrent = Math.min(current, target);
            const percentage = ((safeCurrent / target) * 100).toFixed(1);
            const remaining = target - safeCurrent;

            document.getElementById('statsOutput').style.display = 'block';
            document.getElementById('progressBar').style.width = percentage + '%';
            document.getElementById('percentageText').innerText = percentage + '%';

            if (remaining > 0) {
                document.getElementById('remainingText').innerText = `You need ${remaining.toLocaleString()} more followers to safely request native live badges and brand marketplace features under compliance guidelines.`;
            } else {
                document.getElementById('remainingText').innerText = "🎉 Milestone achieved! Ensure your geographic region is listed within Meta's active payment payout lists.";
            }
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Privacy Policy - CreatorScale</title>
    <style>body { font-family: sans-serif; padding: 40px; line-height: 1.6; max-width: 700px; margin: 0 auto; background: #fafafa; color: #333; }</style>
</head>
<body>
    <h1>Privacy Policy</h1>
    <p><strong>Effective Date: September 22, 2026</strong></p>
    <p>This web dashboard tracks operational metrics on the client-side browser context. It does not store user data remotely without explicit platform authentication.</p>
    
    <h2>Data Protection Officer & Administration</h2>
    <p>This application operates under the direct executive supervision of:</p>
    <ul>
        <li><strong>Owner & CEO:</strong> KWIZERA Gad</li>
        <li><strong>Direct Contact Helpline:</strong> 0792927748</li>
    </ul>

    <h2>Compliance Framework</h2>
    <p>This policy satisfies global terms concerning basic user dashboard configurations, running completely independent of destructive automation practices.</p>
</body>
</html>
