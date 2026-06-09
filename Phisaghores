<!DOCTYPE html>
<html dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>فیثاغورس کامل | محمد امین دشتبان</title>
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --deep: #020b18;
            --navy: #061426;
            --teal: #00c8b4;
            --gold: #f5c842;
            --coral: #ff6b6b;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            background: var(--deep);
            font-family: 'Vazirmatn', system-ui, sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }

        body::before {
            content: '';
            position: fixed;
            inset: 0;
            background:
                radial-gradient(ellipse 80% 60% at 20% 10%, rgba(0,200,180,0.07) 0%, transparent 60%),
                radial-gradient(ellipse 60% 80% at 80% 90%, rgba(245,200,66,0.06) 0%, transparent 60%);
            z-index: 0;
            pointer-events: none;
        }

        .stars {
            position: fixed;
            inset: 0;
            z-index: 0;
            pointer-events: none;
            overflow: hidden;
        }
        .star {
            position: absolute;
            border-radius: 50%;
            background: white;
            animation: twinkle var(--dur) ease-in-out infinite alternate;
            opacity: 0;
        }
        @keyframes twinkle {
            0% { opacity: 0; transform: scale(0.8); }
            100% { opacity: var(--op); transform: scale(1.2); }
        }

        .card {
            position: relative;
            z-index: 1;
            max-width: 580px;
            width: 100%;
            background: linear-gradient(160deg, rgba(255,255,255,0.055) 0%, rgba(0,200,180,0.04) 100%);
            border: 1px solid rgba(0,200,180,0.22);
            border-radius: 32px;
            padding: 32px 28px 24px;
            box-shadow: 0 30px 80px rgba(0,0,0,0.7), 0 0 60px rgba(0,200,180,0.08);
            backdrop-filter: blur(20px);
            animation: cardIn 0.7s cubic-bezier(.22,1,.36,1) both;
        }

        @keyframes cardIn {
            from { opacity:0; transform: translateY(30px) scale(0.97); }
            to   { opacity:1; transform: translateY(0) scale(1); }
        }

        .card::before {
            content: '';
            position: absolute;
            top: -1px; right: -1px;
            width: 120px; height: 120px;
            background: linear-gradient(135deg, var(--teal) 0%, transparent 60%);
            border-radius: 0 32px 0 0;
            opacity: 0.12;
            pointer-events: none;
        }

        .header {
            text-align: center;
            margin-bottom: 22px;
            animation: fadeUp 0.6s 0.1s both;
        }
        @keyframes fadeUp {
            from { opacity:0; transform:translateY(12px); }
            to   { opacity:1; transform:translateY(0); }
        }

        .title {
            font-size: 2rem;
            font-weight: 900;
            background: linear-gradient(90deg, var(--teal), var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle-name {
            margin-top: 6px;
            font-size: 0.85rem;
            color: rgba(245,200,66,0.75);
        }

        .badge-row {
            display: flex;
            justify-content: center;
            gap: 8px;
            margin-top: 10px;
            flex-wrap: wrap;
        }
        .badge {
            background: rgba(0,200,180,0.12);
            border: 1px solid rgba(0,200,180,0.35);
            color: var(--teal);
            border-radius: 20px;
            padding: 4px 14px;
            font-size: 0.7rem;
            font-weight: 700;
        }

        .formula-box {
            background: rgba(0,0,0,0.4);
            border: 1px solid rgba(0,200,180,0.18);
            border-radius: 20px;
            padding: 14px 18px;
            text-align: center;
            margin: 18px 0;
        }
        .formula-text {
            font-size: 1.6rem;
            font-weight: 900;
            color: var(--gold);
            direction: ltr;
        }
        .formula-desc {
            color: rgba(0,200,180,0.7);
            font-size: 0.75rem;
            margin-top: 5px;
        }

        .canvas-wrap {
            background: rgba(0,0,0,0.35);
            border: 1px solid rgba(255,255,255,0.07);
            border-radius: 20px;
            padding: 14px;
            margin: 0 0 18px;
            text-align: center;
            min-height: 250px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        canvas {
            border-radius: 14px;
            width: 100%;
            max-width: 300px;
            height: auto;
            background: #071020;
            display: block;
            margin: 0 auto;
        }

        .input-group {
            background: rgba(255,255,255,0.03);
            border: 1px solid rgba(255,255,255,0.07);
            border-radius: 20px;
            padding: 16px;
            margin-bottom: 16px;
        }
        .input-row {
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 10px 0;
            flex-wrap: wrap;
        }
        .input-row label {
            width: 76px;
            font-weight: 700;
            color: var(--gold);
            font-size: 0.92rem;
            flex-shrink: 0;
        }
        .input-row input {
            flex: 1;
            min-width: 150px;
            background: rgba(255,255,255,0.07);
            border: 1px solid rgba(0,200,180,0.2);
            padding: 11px 14px;
            border-radius: 12px;
            font-size: 0.9rem;
            text-align: center;
            font-weight: 500;
            color: #fff;
            font-family: 'Vazirmatn', monospace;
        }
        .input-row input:focus {
            outline: none;
            border-color: var(--teal);
            background: rgba(0,200,180,0.07);
        }
        .input-row .unit {
            font-size: 0.72rem;
            color: rgba(255,255,255,0.3);
            width: 50px;
            text-align: center;
        }
        .info-text {
            font-size: 0.7rem;
            color: rgba(0,200,180,0.6);
            text-align: center;
            margin-top: 10px;
        }

        .calc-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 16px;
            background: linear-gradient(135deg, var(--teal), #009e8c);
            color: var(--deep);
            font-family: 'Vazirmatn', sans-serif;
            font-weight: 900;
            font-size: 1.05rem;
            cursor: pointer;
            margin-bottom: 16px;
        }
        .calc-btn:hover {
            background: linear-gradient(135deg, #00e0c8, #00b8a0);
        }
        .calc-btn:active {
            transform: scale(0.97);
        }

        .result-box {
            border-radius: 16px;
            padding: 16px 18px;
            min-height: 60px;
            font-size: 0.95rem;
            font-weight: 700;
            text-align: center;
            border: 1px solid rgba(245,200,66,0.2);
            background: rgba(245,200,66,0.05);
            color: rgba(245,200,66,0.85);
        }
        .result-box.success {
            border-color: rgba(0,200,180,0.4);
            background: rgba(0,200,180,0.07);
            color: var(--teal);
        }
        .result-box.error {
            border-color: rgba(255,107,107,0.4);
            background: rgba(255,107,107,0.07);
            color: var(--coral);
        }
        .result-value {
            font-size: 1.5rem;
            font-weight: 900;
            color: var(--gold);
            display: block;
            margin: 4px 0;
        }

        footer {
            margin-top: 20px;
            text-align: center;
            border-top: 1px solid rgba(255,255,255,0.06);
            padding-top: 14px;
        }
        .dev-name { font-weight: 700; color: var(--gold); font-size: 0.82rem; }
        .teacher-name { color: rgba(255,107,107,0.75); font-size: 0.78rem; }

        @keyframes pulse-ring {
            0% { box-shadow: 0 0 0 0 rgba(0,200,180,0.2); }
            70% { box-shadow: 0 0 0 10px rgba(0,200,180,0); }
            100% { box-shadow: 0 0 0 0 rgba(0,200,180,0); }
        }
        .canvas-wrap.pulse { animation: pulse-ring 0.6s ease-out; }
    </style>
</head>
<body>

<div class="stars" id="stars"></div>

<div class="card">
    <div class="header">
        <div class="title">📐 فیثاغورس هوشمند</div>
        <div class="subtitle-name">✦ محمد امین دشتبان ✦</div>
        <div class="badge-row">
            <span class="badge">a² + b² = c²</span>
            <span class="badge">پشتیبانی از اعشار، کسر و رادیکال</span>
        </div>
    </div>

    <div class="formula-box">
        <div class="formula-text">a² + b² = c²</div>
        <div class="formula-desc">a و b = ضلع‌های قائمه | c = وتر</div>
    </div>

    <div class="canvas-wrap" id="canvasWrap">
        <canvas id="triangleCanvas" width="300" height="220"></canvas>
    </div>

    <div class="input-group">
        <div class="input-row">
            <label>📐 ضلع a :</label>
            <input type="text" id="sideA" placeholder="مثال: 3, 1.5, 3/4, √2" value="3">
            <span class="unit">واحد</span>
        </div>
        <div class="input-row">
            <label>📐 ضلع b :</label>
            <input type="text" id="sideB" placeholder="مثال: 4, 2.5, 2/3, √3" value="4">
            <span class="unit">واحد</span>
        </div>
        <div class="input-row">
            <label>🔺 وتر c :</label>
            <input type="text" id="sideC" placeholder="مثال: 5, 3.2, 1/2, √5" value="">
            <span class="unit">واحد</span>
        </div>
        <div class="info-text">💡 پشتیبانی از: اعشار (1.5) | کسر (3/4) | رادیکال (√2 یا sqrt(2))</div>
    </div>

    <button class="calc-btn" id="calcBtn">
        <span>🧮</span>
        محاسبه کن
    </button>

    <div class="result-box" id="resultArea">نتیجه اینجا نشان داده می‌شود</div>

    <footer>
        <div class="dev-name">👨‍💻 محمد امین دشتبان</div>
        <div class="teacher-name">📚 دبیر: آقای نجف‌پور</div>
    </footer>
</div>

<script>
    // ستاره‌ها
    const starsEl = document.getElementById('stars');
    for (let i = 0; i < 80; i++) {
        const s = document.createElement('div');
        s.className = 'star';
        const size = Math.random() * 2.2 + 0.5;
        s.style.cssText = `
            width:${size}px; height:${size}px;
            top:${Math.random()*100}%;
            left:${Math.random()*100}%;
            --dur:${(Math.random()*3+2).toFixed(1)}s;
            --op:${(Math.random()*0.5+0.15).toFixed(2)};
            animation-delay:${(Math.random()*4).toFixed(1)}s;
        `;
        starsEl.appendChild(s);
    }

    // تابع تبدیل ورودی به عدد
    function parseInputValue(str) {
        if (!str || str.trim() === '') return NaN;
        let input = str.trim().replace(/\s/g, '');
        input = input.replace(/√/g, 'Math.sqrt');
        
        const sqrtMatch = input.match(/sqrt\(([^)]+)\)/i);
        if (sqrtMatch) {
            try {
                const innerValue = parseInputValue(sqrtMatch[1]);
                if (!isNaN(innerValue) && innerValue >= 0) {
                    return Math.sqrt(innerValue);
                }
            } catch(e) {}
        }
        
        if (input.includes('/')) {
            const parts = input.split('/');
            if (parts.length === 2) {
                const numerator = parseFloat(parts[0]);
                const denominator = parseFloat(parts[1]);
                if (!isNaN(numerator) && !isNaN(denominator) && denominator !== 0) {
                    return numerator / denominator;
                }
            }
        }
        
        const num = parseFloat(input);
        if (!isNaN(num)) return num;
        return NaN;
    }

    function fmt(n) { 
        if (isNaN(n)) return '?';
        return Math.round(n * 100) / 100; 
    }
    
    function fmtPrecise(n) {
        if (isNaN(n)) return '?';
        return Math.round(n * 1000000) / 1000000;
    }

    // کانواس
    const canvas = document.getElementById('triangleCanvas');
    const ctx = canvas.getContext('2d');

    function drawTriangle(a, b, c) {
        const w = canvas.clientWidth || 300;
        const h = canvas.clientHeight || 220;
        
        canvas.width = w;
        canvas.height = h;
        
        ctx.clearRect(0, 0, w, h);

        // گرید
        ctx.strokeStyle = 'rgba(0,200,180,0.08)';
        ctx.lineWidth = 0.5;
        for (let x = 0; x < w; x += 25) { 
            ctx.beginPath(); 
            ctx.moveTo(x,0); 
            ctx.lineTo(x,h); 
            ctx.stroke(); 
        }
        for (let y = 0; y < h; y += 25) { 
            ctx.beginPath(); 
            ctx.moveTo(0,y); 
            ctx.lineTo(w,y); 
            ctx.stroke(); 
        }

        // بررسی اعتبار
        if (isNaN(a) || isNaN(b) || isNaN(c) || a <= 0 || b <= 0 || c <= 0) {
            ctx.fillStyle = 'rgba(255,255,255,0.4)';
            ctx.font = '14px Vazirmatn';
            ctx.textAlign = 'center';
            ctx.fillText('مقادیر معتبر وارد کنید', w/2, h/2);
            return;
        }

        // محاسبه موقعیت مثلث
        const margin = 45;
        const maxX = Math.max(b, a * (b/a));
        const scale = Math.min((w - margin * 1.5) / maxX, (h - margin * 1.5) / Math.max(a, b));
        
        const ox = margin;
        const oy = h - margin;
        const bx = ox + b * scale;
        const ay = oy - a * scale;

        // پر کردن مثلث
        const grad = ctx.createLinearGradient(ox, ay, bx, oy);
        grad.addColorStop(0, 'rgba(0,200,180,0.25)');
        grad.addColorStop(1, 'rgba(245,200,66,0.1)');
        ctx.beginPath();
        ctx.moveTo(ox, oy); 
        ctx.lineTo(bx, oy); 
        ctx.lineTo(ox, ay);
        ctx.closePath();
        ctx.fillStyle = grad;
        ctx.fill();

        // خطوط اضلاع قائمه
        ctx.strokeStyle = '#00c8b4';
        ctx.lineWidth = 2.5;
        ctx.stroke();

        // خط وتر
        ctx.beginPath(); 
        ctx.moveTo(bx, oy); 
        ctx.lineTo(ox, ay);
        ctx.strokeStyle = '#f5c842';
        ctx.lineWidth = 3;
        ctx.stroke();

        // علامت قائمه
        const sq = 12;
        ctx.fillStyle = 'rgba(245,200,66,0.85)';
        ctx.fillRect(ox + 3, oy - sq - 3, sq, sq);
        ctx.strokeStyle = '#f5c842';
        ctx.lineWidth = 1.5;
        ctx.strokeRect(ox + 3, oy - sq - 3, sq, sq);

        // برچسب‌ها
        ctx.font = 'bold 14px Vazirmatn';
        ctx.fillStyle = '#00e8d0';
        ctx.textAlign = 'right';
        ctx.fillText(`a = ${fmt(a)}`, ox - 10, (oy + ay) / 2);

        ctx.fillStyle = '#7dd8ff';
        ctx.textAlign = 'center';
        ctx.fillText(`b = ${fmt(b)}`, (ox + bx) / 2, oy + 18);

        ctx.fillStyle = '#f5c842';
        ctx.textAlign = 'left';
        ctx.fillText(`c = ${fmt(c)}`, bx + 10, (oy + ay) / 2 - 5);
    }

    function setResult(el, msg, type) {
        el.className = `result-box ${type}`;
        el.innerHTML = msg;
    }

    function compute() {
        const a = parseInputValue(document.getElementById('sideA').value);
        const b = parseInputValue(document.getElementById('sideB').value);
        const c = parseInputValue(document.getElementById('sideC').value);
        
        const res = document.getElementById('resultArea');
        const isValid = n => !isNaN(n) && n > 0;
        const count = [a, b, c].filter(isValid).length;
        
        if (count < 2) {
            setResult(res, '⚠️ لطفاً دو مقدار از اضلاع را وارد کن!', 'error');
            drawTriangle(NaN, NaN, NaN);
            return;
        }
        if (count > 2) {
            setResult(res, '⚠️ فقط دو مقدار وارد کن — سومی را خالی بذار!', 'error');
            drawTriangle(NaN, NaN, NaN);
            return;
        }
        
        let result, label;
        
        if (isValid(a) && isValid(b)) {
            result = Math.sqrt(a*a + b*b);
            label = 'وتر (c)';
            document.getElementById('sideC').value = fmtPrecise(result);
            drawTriangle(a, b, result);
        } 
        else if (isValid(a) && isValid(c)) {
            if (c <= a) { 
                setResult(res, '⚠️ وتر باید بزرگتر از ضلع a باشد!', 'error'); 
                drawTriangle(NaN, NaN, NaN); 
                return; 
            }
            result = Math.sqrt(c*c - a*a);
            label = 'ضلع b';
            document.getElementById('sideB').value = fmtPrecise(result);
            drawTriangle(a, result, c);
        } 
        else {
            if (c <= b) { 
                setResult(res, '⚠️ وتر باید بزرگتر از ضلع b باشد!', 'error'); 
                drawTriangle(NaN, NaN, NaN); 
                return; 
            }
            result = Math.sqrt(c*c - b*b);
            label = 'ضلع a';
            document.getElementById('sideA').value = fmtPrecise(result);
            drawTriangle(result, b, c);
        }
        
        res.className = 'result-box success';
        res.innerHTML = `✅ <strong>${label}</strong> محاسبه شد<br><span class="result-value">${fmtPrecise(result)} واحد</span>`;
        
        const wrap = document.getElementById('canvasWrap');
        wrap.classList.remove('pulse');
        void wrap.offsetWidth;
        wrap.classList.add('pulse');
    }
    
    document.getElementById('calcBtn').addEventListener('click', compute);
    document.addEventListener('keydown', e => { if (e.key === 'Enter') compute(); });
    
    // مثلث پیش‌فرض
    drawTriangle(3, 4, 5);
</script>
</body>
</html>
