<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>🔄 Sprite Align Pro</title>
    <style>
        /* ==========================================================
           Sprite Align Pro - UI/UX by DeepSeek (ثابت 100%)
           ========================================================== */
        :root {
            --bg-primary: #0b1220;
            --bg-secondary: #151f32;
            --bg-card: rgba(255,255,255,0.04);
            --border-color: rgba(255,255,255,0.06);
            --text-primary: #eef2ff;
            --text-secondary: #b9c4f0;
            --text-muted: #8d9bd0;
            --accent-blue: #3b82f6;
            --accent-yellow: #facc15;
            --accent-green: #22c55e;
            --accent-purple: #a78bfa;
            --shadow: 0 20px 50px rgba(0,0,0,0.5);
            --radius: 24px;
            --radius-sm: 12px;
            --transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        body {
            background: var(--bg-primary);
            color: var(--text-primary);
            min-height: 100vh;
            padding: 20px;
        }
        .container {
            max-width: 1500px;
            margin: 0 auto;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 28px;
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(16px);
            border-radius: 60px;
            border: 1px solid var(--border-color);
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 12px;
        }
        .logo {
            font-size: 26px;
            font-weight: 800;
            background: linear-gradient(135deg, var(--accent-blue), var(--accent-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .logo i {
            -webkit-text-fill-color: initial;
            color: var(--accent-blue);
        }
        .logo span {
            font-size: 14px;
            background: var(--accent-purple);
            padding: 2px 12px;
            border-radius: 40px;
            color: white;
            -webkit-text-fill-color: white;
            font-weight: 600;
        }
        .header-actions {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }
        .btn {
            padding: 10px 24px;
            border: none;
            border-radius: 50px;
            font-weight: 700;
            cursor: pointer;
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 13px;
            background: rgba(255,255,255,0.06);
            color: var(--text-secondary);
            border: 1px solid rgba(255,255,255,0.06);
        }
        .btn:hover {
            background: rgba(255,255,255,0.12);
            transform: translateY(-2px);
        }
        .btn-primary {
            background: linear-gradient(135deg, var(--accent-blue), var(--accent-purple));
            color: white;
            border: none;
            box-shadow: 0 8px 25px rgba(59, 130, 246, 0.3);
        }
        .btn-primary:hover {
            box-shadow: 0 12px 35px rgba(59, 130, 246, 0.5);
        }
        .btn-success {
            background: var(--accent-green);
            color: white;
            border: none;
        }
        .btn-yellow {
            background: var(--accent-yellow);
            color: #0b1220;
            border: none;
        }
        .btn-ghost {
            background: rgba(167, 139, 250, 0.15);
            border: 1px solid var(--accent-purple);
            color: var(--accent-purple);
        }
        .btn-ghost:hover {
            background: rgba(167, 139, 250, 0.25);
        }
        .btn-danger {
            background: #ef4444;
            color: white;
            border: none;
        }
        .btn-sm {
            padding: 6px 14px;
            font-size: 14px;
        }
        .main-grid {
            display: grid;
            grid-template-columns: 1fr 320px;
            gap: 25px;
        }
        @media (max-width: 1100px) {
            .main-grid {
                grid-template-columns: 1fr;
            }
        }
        .card {
            background: var(--bg-card);
            backdrop-filter: blur(16px);
            border-radius: var(--radius);
            padding: 24px;
            border: 1px solid var(--border-color);
            box-shadow: var(--shadow);
        }
        .card-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 16px;
            color: var(--text-secondary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .card-title i {
            color: var(--accent-purple);
        }
        .drop-zone {
            border: 2px dashed rgba(167, 139, 250, 0.3);
            border-radius: var(--radius-sm);
            padding: 30px 20px;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            background: rgba(167, 139, 250, 0.03);
            min-height: 140px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        .drop-zone:hover {
            border-color: var(--accent-purple);
            background: rgba(167, 139, 250, 0.07);
        }
        .drop-zone i {
            font-size: 40px;
            color: var(--text-muted);
            margin-bottom: 8px;
        }
        .drop-zone p {
            color: var(--text-muted);
            font-size: 14px;
        }
        .drop-zone input {
            display: none;
        }
        .drop-zone .warning {
            color: var(--accent-yellow);
            font-size: 12px;
            margin-top: 8px;
            background: rgba(250, 204, 21, 0.1);
            padding: 4px 12px;
            border-radius: 20px;
            border: 1px solid rgba(250, 204, 21, 0.2);
        }
        .frames-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 12px;
            margin-top: 16px;
            max-height: 400px;
            overflow-y: auto;
            padding: 4px;
        }
        .frame-thumb {
            background: var(--bg-secondary);
            border-radius: var(--radius-sm);
            padding: 8px;
            border: 2px solid transparent;
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
        }
        .frame-thumb:hover {
            border-color: var(--accent-purple);
        }
        .frame-thumb.active {
            border-color: var(--accent-blue);
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.2);
        }
        .frame-thumb canvas {
            width: 100%;
            aspect-ratio: 1/1;
            border-radius: 6px;
            background: #0a0f18;
            image-rendering: pixelated;
        }
        .frame-thumb .frame-label {
            font-size: 11px;
            color: var(--text-muted);
            margin-top: 4px;
        }
        .viewer-container {
            position: relative;
            background: #0a0f18;
            border-radius: var(--radius-sm);
            overflow: hidden;
            aspect-ratio: 1/1;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--border-color);
        }
        .viewer-container canvas {
            width: 100%;
            height: 100%;
            image-rendering: pixelated;
            image-rendering: crisp-edges;
        }
        .alignment-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }
        .alignment-line {
            position: absolute;
            pointer-events: none;
            opacity: 0.7;
        }
        .alignment-line.vertical {
            width: 1px;
            height: 100%;
            left: 50%;
            top: 0;
            background: var(--accent-blue);
            box-shadow: 0 0 8px rgba(59, 130, 246, 0.3);
        }
        .alignment-line.horizontal {
            width: 100%;
            height: 1px;
            top: 50%;
            left: 0;
            background: var(--accent-yellow);
            box-shadow: 0 0 8px rgba(250, 204, 21, 0.3);
        }
        .alignment-line.baseline {
            width: 100%;
            height: 1px;
            top: 75%;
            left: 0;
            background: var(--accent-green);
            box-shadow: 0 0 8px rgba(34, 197, 94, 0.3);
            border-top: 2px dashed var(--accent-green);
        }
        .controls-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
            margin: 16px 0;
        }
        .controls-grid .btn {
            justify-content: center;
            padding: 14px;
            font-size: 18px;
        }
        .slider-group {
            margin: 12px 0;
        }
        .slider-group label {
            display: flex;
            justify-content: space-between;
            font-size: 13px;
            color: var(--text-muted);
            margin-bottom: 4px;
        }
        .slider-group input[type="range"] {
            width: 100%;
            height: 4px;
            -webkit-appearance: none;
            background: #2a3150;
            border-radius: 10px;
            outline: none;
        }
        .slider-group input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background: var(--accent-blue);
            cursor: pointer;
        }
        .ghost-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 12px 0;
        }
        .ghost-controls .btn {
            font-size: 12px;
            padding: 6px 14px;
        }
        .status-bar {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 8px;
            padding: 12px 16px;
            background: var(--bg-secondary);
            border-radius: var(--radius-sm);
            margin-top: 16px;
            font-size: 13px;
            color: var(--text-muted);
        }
        .status-bar strong {
            color: var(--text-primary);
        }
        .toast {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--bg-secondary);
            color: white;
            padding: 14px 24px;
            border-radius: var(--radius-sm);
            border: 1px solid var(--accent-purple);
            box-shadow: var(--shadow);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 9999;
            font-size: 14px;
            pointer-events: none;
        }
        .toast.show {
            opacity: 1;
            pointer-events: auto;
        }

        /* ===== Animation Preview ===== */
        .preview-section {
            background: var(--bg-card);
            border-radius: var(--radius);
            padding: 20px;
            border: 1px solid var(--border-color);
            margin-top: 20px;
        }
        .section-header {
            font-size: 16px;
            font-weight: 600;
            color: var(--text-secondary);
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .section-header i {
            color: var(--accent-purple);
        }
        .preview-container {
            position: relative;
            background: #0a0f18;
            border-radius: var(--radius-sm);
            overflow: hidden;
            aspect-ratio: 1/1;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--border-color);
        }
        .preview-container canvas {
            width: 100%;
            height: 100%;
            image-rendering: pixelated;
            image-rendering: crisp-edges;
        }
        .preview-controls {
            position: absolute;
            bottom: 16px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 8px;
            background: rgba(0,0,0,0.7);
            backdrop-filter: blur(8px);
            padding: 8px 16px;
            border-radius: 40px;
            border: 1px solid rgba(255,255,255,0.06);
        }
        .preview-controls .btn {
            padding: 6px 14px;
            font-size: 16px;
            min-width: 36px;
            justify-content: center;
            background: transparent;
            border: none;
            color: var(--text-secondary);
            border-radius: 30px;
            transition: var(--transition);
        }
        .preview-controls .btn:hover {
            background: rgba(255,255,255,0.06);
            color: white;
        }
        .preview-controls .btn-primary {
            background: var(--accent-blue);
            color: white;
        }
        .preview-controls .btn-primary:hover {
            background: var(--accent-purple);
        }
        .preview-tools {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 16px;
            margin-top: 16px;
        }
        .tool-group {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        .tool-group label {
            font-size: 12px;
            color: var(--text-muted);
            font-weight: 500;
        }
        .tool-group input[type="range"] {
            width: 100%;
            height: 4px;
            -webkit-appearance: none;
            background: #2a3150;
            border-radius: 10px;
            outline: none;
        }
        .tool-group input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 14px;
            height: 14px;
            border-radius: 50%;
            background: var(--accent-blue);
            cursor: pointer;
        }

        /* ===== Timeline ===== */
        .timeline-section {
            margin-top: 20px;
            background: var(--bg-card);
            border-radius: var(--radius);
            padding: 20px;
            border: 1px solid var(--border-color);
        }
        .timeline-section .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 12px;
            font-size: 15px;
            color: var(--text-secondary);
        }
        .timeline-section .section-header i {
            color: var(--accent-purple);
        }
        .timeline-info {
            font-size: 13px;
            color: var(--text-muted);
            background: var(--bg-secondary);
            padding: 2px 12px;
            border-radius: 40px;
        }
        .timeline-container {
            position: relative;
            background: var(--bg-secondary);
            border-radius: var(--radius-sm);
            padding: 12px 8px;
            overflow-x: auto;
            overflow-y: hidden;
            border: 1px solid var(--border-color);
            min-height: 70px;
            display: flex;
            align-items: center;
        }
        .timeline-track {
            display: flex;
            gap: 6px;
            padding: 4px 8px;
            min-width: 100%;
            justify-content: center;
            align-items: center;
        }
        .timeline-frame {
            width: 44px;
            height: 44px;
            min-width: 44px;
            border-radius: 8px;
            border: 2px solid transparent;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 11px;
            font-weight: 600;
            color: var(--text-muted);
            background: var(--bg-primary);
            overflow: hidden;
            position: relative;
        }
        .timeline-frame canvas {
            width: 100%;
            height: 100%;
            image-rendering: pixelated;
            image-rendering: crisp-edges;
        }
        .timeline-frame .frame-number {
            position: absolute;
            bottom: 2px;
            right: 4px;
            font-size: 9px;
            color: rgba(255,255,255,0.3);
            background: rgba(0,0,0,0.5);
            padding: 0 4px;
            border-radius: 4px;
        }
        .timeline-frame:hover {
            border-color: var(--text-muted);
            transform: scale(1.05);
        }
        .timeline-frame.active {
            border-color: var(--accent-blue);
            box-shadow: 0 0 16px rgba(59, 130, 246, 0.3);
            transform: scale(1.08);
        }
        .timeline-frame.has-offset {
            border-color: var(--accent-yellow);
        }
        .timeline-frame.has-offset.active {
            border-color: var(--accent-purple);
            box-shadow: 0 0 16px rgba(167, 139, 250, 0.3);
        }
        .timeline-marker {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            color: var(--accent-blue);
            font-size: 18px;
            text-shadow: 0 0 12px rgba(59, 130, 246, 0.4);
            transition: left 0.3s ease;
            pointer-events: none;
            z-index: 10;
        }
        .timeline-controls {
            display: flex;
            gap: 8px;
            margin-top: 12px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .timeline-controls .btn {
            padding: 6px 16px;
            font-size: 14px;
            background: var(--bg-secondary);
            color: var(--text-secondary);
            border: 1px solid var(--border-color);
            border-radius: 30px;
            transition: var(--transition);
            cursor: pointer;
        }
        .timeline-controls .btn:hover {
            background: var(--accent-blue);
            color: white;
            border-color: var(--accent-blue);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
        }
        .timeline-container::-webkit-scrollbar {
            height: 4px;
        }
        .timeline-container::-webkit-scrollbar-track {
            background: var(--bg-primary);
        }
        .timeline-container::-webkit-scrollbar-thumb {
            background: var(--accent-purple);
            border-radius: 10px;
        }
        ::-webkit-scrollbar {
            width: 4px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg-primary);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--accent-purple);
            border-radius: 10px;
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
                align-items: stretch;
                text-align: center;
                border-radius: 30px;
                padding: 16px;
            }
            .header-actions {
                justify-content: center;
            }
            .controls-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .frames-grid {
                grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            }
            .main-grid {
                gap: 16px;
            }
            .card {
                padding: 16px;
            }
            .btn {
                font-size: 12px;
                padding: 8px 16px;
            }
            .preview-tools {
                grid-template-columns: 1fr 1fr;
            }
            .preview-controls {
                padding: 6px 12px;
                gap: 4px;
                bottom: 10px;
            }
            .preview-controls .btn {
                padding: 4px 10px;
                font-size: 14px;
                min-width: 30px;
            }
            .timeline-frame {
                width: 34px;
                height: 34px;
                min-width: 34px;
                font-size: 9px;
            }
            .timeline-frame .frame-number {
                font-size: 7px;
                bottom: 1px;
                right: 2px;
            }
            .timeline-marker {
                font-size: 14px;
                top: -8px;
            }
        }

        @media (max-width: 400px) {
            .timeline-frame {
                width: 28px;
                height: 28px;
                min-width: 28px;
            }
            .timeline-frame .frame-number {
                font-size: 6px;
                bottom: 0;
                right: 1px;
                padding: 0 2px;
            }
            .timeline-marker {
                font-size: 12px;
                top: -6px;
            }
            .preview-controls .btn {
                padding: 2px 8px;
                font-size: 12px;
                min-width: 24px;
            }
            .btn {
                font-size: 11px;
                padding: 6px 12px;
            }
            .status-bar {
                font-size: 11px;
                flex-direction: column;
                align-items: center;
                gap: 4px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo"><i>🔄</i> Sprite Align <span>Pro</span></div>
            <div class="header-actions">
                <button class="btn btn-primary" id="exportBtn">📤 تصدير</button>
                <button class="btn btn-yellow" id="resetAllBtn">↺ إعادة الكل</button>
            </div>
        </header>

        <div class="main-grid">
            <!-- العمود الأيسر -->
            <div class="card">
                <div class="card-title"><i>🎯</i> المعاينة</div>
                <div class="drop-zone" id="dropZone">
                    <i>📤</i>
                    <p>اسحب PNG هنا أو اضغط للاختيار</p>
                    <div class="warning">⚠️ ارفع صور PNG بخلفية شفافة فقط</div>
                    <input type="file" id="fileInput" accept="image/png" multiple />
                </div>
                <div class="viewer-container" id="viewerContainer">
                    <canvas id="viewerCanvas"></canvas>
                    <div class="alignment-overlay" id="alignmentOverlay">
                        <div class="alignment-line vertical" id="lineV"></div>
                        <div class="alignment-line horizontal" id="lineH"></div>
                        <div class="alignment-line baseline" id="lineB"></div>
                    </div>
                </div>
                <div class="status-bar">
                    <span>📐 الإطار: <strong id="frameCounter">0 / 0</strong></span>
                    <span>📏 الحجم: <strong id="sizeInfo">0x0</strong></span>
                    <span>🔄 <strong id="offsetInfo">X:0 Y:0</strong></span>
                </div>
            </div>

            <!-- العمود الأيمن -->
            <div class="card">
                <div class="card-title"><i>🛠️</i> الأدوات</div>
                <div class="controls-grid">
                    <button class="btn btn-secondary" id="moveUp">⬆</button>
                    <button class="btn btn-secondary" id="moveLeft">⬅</button>
                    <button class="btn btn-secondary" id="moveRight">➡</button>
                    <button class="btn btn-secondary" id="moveDown">⬇</button>
                </div>
                <div class="card-title" style="margin-top:12px;"><i>👻</i> Ghost Frames</div>
                <div class="ghost-controls">
                    <button class="btn btn-ghost" id="ghostPrev">👻 السابق</button>
                    <button class="btn btn-ghost" id="ghostNext">👻 التالي</button>
                    <button class="btn btn-ghost" id="ghostAll">👻 الكل</button>
                    <button class="btn btn-danger" id="clearGhosts">✖ إزالة</button>
                </div>
                <div class="slider-group">
                    <label><span>شفافية Ghost</span><span id="ghostOpacityLabel">30%</span></label>
                    <input type="range" id="ghostOpacity" min="0" max="100" value="30" />
                </div>
                <div class="card-title" style="margin-top:12px;"><i>📋</i> الإطارات</div>
                <div class="frames-grid" id="framesGrid"></div>
                <button class="btn btn-primary" id="resetFrameBtn" style="width:100%;margin-top:12px;">↺ إعادة ضبط الإطار</button>
                <div style="display: flex; gap: 8px; margin-top: 12px;">
                    <button class="btn btn-secondary" id="lockHeightBtn" style="flex:1;">🔒 قفل الارتفاع</button>
                    <button class="btn btn-secondary" id="autoHeightBtn" style="flex:1;">📏 ضبط الارتفاع</button>
                </div>
            </div>
        </div>

        <!-- Animation Preview -->
        <div class="preview-section">
            <div class="section-header"><i>🎬</i> Animation Preview</div>
            <div class="preview-container">
                <canvas id="previewCanvas"></canvas>
                <div class="preview-controls">
                    <button class="btn btn-secondary" id="prevFrameBtn">⏮</button>
                    <button class="btn btn-primary" id="playBtn">▶</button>
                    <button class="btn btn-secondary" id="pauseBtn">⏸</button>
                    <button class="btn btn-secondary" id="stopBtn">⏹</button>
                    <button class="btn btn-secondary" id="nextFrameBtn">⏭</button>
                </div>
            </div>
            <div class="preview-tools">
                <div class="tool-group">
                    <label>FPS</label>
                    <input type="range" id="fpsSlider" min="2" max="20" value="12" />
                    <span id="fpsValue">12</span>
                </div>
                <div class="tool-group">
                    <label>Loop</label>
                    <input type="checkbox" id="loopToggle" checked />
                </div>
                <div class="tool-group">
                    <label>Zoom</label>
                    <input type="range" id="zoomSlider" min="25" max="200" value="100" />
                    <span id="zoomValue">100%</span>
                </div>
            </div>
        </div>

        <!-- Timeline -->
        <div class="timeline-section">
            <div class="section-header">
                <i>🎞️</i> Timeline
                <span class="timeline-info" id="timelineInfo">الإطار 0 / 0</span>
            </div>
            <div class="timeline-container" id="timelineContainer">
                <div class="timeline-track" id="timelineTrack"></div>
                <div class="timeline-marker" id="timelineMarker">▲</div>
            </div>
            <div class="timeline-controls">
                <button class="btn btn-sm btn-secondary" id="timelineFirst">⏮⏮</button>
                <button class="btn btn-sm btn-secondary" id="timelinePrev">⏮</button>
                <button class="btn btn-sm btn-secondary" id="timelineNext">⏭</button>
                <button class="btn btn-sm btn-secondary" id="timelineLast">⏭⏭</button>
            </div>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <script>
        /* ==========================================================
           Sprite Align Pro - Core Engine v1.1
           جميع الأجزاء مدمجة (ChatGPT) + 30 لون مختلف لـ Ghost Frames
           + مسافة 3px بين الإطارات + قفل الارتفاع
           ========================================================== */

        // ================================
        // ألوان Ghost Frames (30 لون مختلف)
        // ================================
        const ghostColors = [
            "rgba(255,0,0,0.25)", "rgba(255,69,0,0.25)", "rgba(255,165,0,0.25)",
            "rgba(255,215,0,0.25)", "rgba(255,255,0,0.25)", "rgba(173,255,47,0.25)",
            "rgba(0,255,0,0.25)", "rgba(0,255,127,0.25)", "rgba(0,255,255,0.25)",
            "rgba(0,191,255,0.25)", "rgba(0,0,255,0.25)", "rgba(75,0,130,0.25)",
            "rgba(128,0,128,0.25)", "rgba(255,0,255,0.25)", "rgba(255,20,147,0.25)",
            "rgba(255,105,180,0.25)", "rgba(255,182,193,0.25)", "rgba(255,99,71,0.25)",
            "rgba(255,140,0,0.25)", "rgba(154,205,50,0.25)", "rgba(60,179,113,0.25)",
            "rgba(46,139,87,0.25)", "rgba(0,206,209,0.25)", "rgba(70,130,180,0.25)",
            "rgba(100,149,237,0.25)", "rgba(138,43,226,0.25)", "rgba(186,85,211,0.25)",
            "rgba(218,112,214,0.25)", "rgba(255,182,193,0.25)", "rgba(255,228,196,0.25)"
        ];

        // ================================
        // عناصر الواجهة
        // ================================
        const dropZone = document.getElementById("dropZone");
        const fileInput = document.getElementById("fileInput");

        const viewerCanvas = document.getElementById("viewerCanvas");
        const viewerCtx = viewerCanvas.getContext("2d");

        const previewCanvas = document.getElementById("previewCanvas");
        const previewCtx = previewCanvas.getContext("2d");

        const framesGrid = document.getElementById("framesGrid");
        const timelineTrack = document.getElementById("timelineTrack");
        const timelineMarker = document.getElementById("timelineMarker");

        const frameCounter = document.getElementById("frameCounter");
        const sizeInfo = document.getElementById("sizeInfo");
        const offsetInfo = document.getElementById("offsetInfo");
        const timelineInfo = document.getElementById("timelineInfo");

        const fpsSlider = document.getElementById("fpsSlider");
        const fpsValue = document.getElementById("fpsValue");

        const zoomSlider = document.getElementById("zoomSlider");
        const zoomValue = document.getElementById("zoomValue");

        const ghostOpacity = document.getElementById("ghostOpacity");
        const ghostOpacityLabel = document.getElementById("ghostOpacityLabel");

        // ================================
        // أزرار التحريك
        // ================================
        const moveUp = document.getElementById("moveUp");
        const moveDown = document.getElementById("moveDown");
        const moveLeft = document.getElementById("moveLeft");
        const moveRight = document.getElementById("moveRight");

        // ================================
        // Ghost
        // ================================
        const ghostPrev = document.getElementById("ghostPrev");
        const ghostNext = document.getElementById("ghostNext");
        const ghostAll = document.getElementById("ghostAll");
        const clearGhosts = document.getElementById("clearGhosts");

        // ================================
        // Preview
        // ================================
        const playBtn = document.getElementById("playBtn");
        const pauseBtn = document.getElementById("pauseBtn");
        const stopBtn = document.getElementById("stopBtn");
        const prevFrameBtn = document.getElementById("prevFrameBtn");
        const nextFrameBtn = document.getElementById("nextFrameBtn");

        // ================================
        // Timeline
        // ================================
        const timelineFirst = document.getElementById("timelineFirst");
        const timelinePrev = document.getElementById("timelinePrev");
        const timelineNext = document.getElementById("timelineNext");
        const timelineLast = document.getElementById("timelineLast");

        // ================================
        // أزرار عامة
        // ================================
        const exportBtn = document.getElementById("exportBtn");
        const resetFrameBtn = document.getElementById("resetFrameBtn");
        const resetAllBtn = document.getElementById("resetAllBtn");
        const lockHeightBtn = document.getElementById("lockHeightBtn");
        const autoHeightBtn = document.getElementById("autoHeightBtn");

        // ================================
        // البيانات
        // ================================
        const MAX_FRAMES = 30;

        let frames = [];
        let currentFrame = 0;

        let zoom = 1;
        let onionEnabled = true;
        let onionOpacity = 0.3;

        let playing = false;
        let previewRAF = null;
        let lastTime = 0;

        let lockHeight = false;
        let fixedHeight = 0;

        // ================================
        // Toast
        // ================================

        function showToast(message) {
            const toast = document.getElementById("toast");
            if (!toast) return;
            toast.textContent = message;
            toast.classList.add("show");
            clearTimeout(showToast.timer);
            showToast.timer = setTimeout(() => {
                toast.classList.remove("show");
            }, 2200);
        }

        // ================================
        // تحديث المعلومات
        // ================================

        function updateStatus() {
            frameCounter.textContent = (frames.length ? currentFrame + 1 : 0) + " / " + frames.length;

            if (frames[currentFrame]) {
                sizeInfo.textContent =
                    frames[currentFrame].image.width +
                    " × " +
                    frames[currentFrame].image.height;

                offsetInfo.textContent =
                    "X: " + frames[currentFrame].x +
                    " | Y: " + frames[currentFrame].y;
            } else {
                sizeInfo.textContent = "-";
                offsetInfo.textContent = "-";
            }

            timelineInfo.textContent =
                "الإطار " + (frames.length ? currentFrame + 1 : 0) + " / " + frames.length;
        }

        // ================================
        // إضافة صورة واحدة
        // ================================

        function addFrame(file) {
            if (frames.length >= MAX_FRAMES) {
                showToast("❌ الحد الأقصى 30 إطار");
                return;
            }

            if (!file.type.startsWith("image")) return;

            const reader = new FileReader();

            reader.onload = function(e) {
                const img = new Image();

                img.onload = function() {
                    frames.push({
                        image: img,
                        src: e.target.result,
                        x: 0,
                        y: 0
                    });

                    currentFrame = frames.length - 1;

                    renderViewer();
                    renderFramesGrid();
                    renderTimeline();
                    updateStatus();

                    showToast("✅ تمت إضافة إطار");
                };

                img.src = e.target.result;
            };

            reader.readAsDataURL(file);
        }

        // ================================
        // اختيار الملفات
        // ================================

        fileInput.addEventListener("change", function() {
            [...this.files].forEach(addFrame);
            this.value = "";
        });

        // ================================
        // Drag & Drop
        // ================================

        dropZone.addEventListener("dragover", function(e) {
            e.preventDefault();
            dropZone.style.borderColor = "#3b82f6";
        });

        dropZone.addEventListener("dragleave", function() {
            dropZone.style.borderColor = "";
        });

        dropZone.addEventListener("drop", function(e) {
            e.preventDefault();
            dropZone.style.borderColor = "";
            [...e.dataTransfer.files].forEach(addFrame);
        });

        dropZone.addEventListener("click", function() {
            fileInput.click();
        });

        // ================================
        // رسم الإطار
        // ================================

        function drawFrameOnViewer(frame, alpha) {
            const img = frame.image;

            viewerCtx.save();
            viewerCtx.globalAlpha = alpha;

            const scale = Math.min(
                viewerCanvas.width / img.width,
                viewerCanvas.height / img.height
            ) * zoom;

            const w = img.width * scale;
            const h = img.height * scale;

            const x = (viewerCanvas.width - w) / 2 + frame.x;
            const y = (viewerCanvas.height - h) / 2 + frame.y;

            viewerCtx.imageSmoothingEnabled = false;
            viewerCtx.drawImage(img, x, y, w, h);

            viewerCtx.restore();
        }

        // ================================
        // رسم Ghost Frame بلون مختلف
        // ================================

        function drawGhostFrame(frame, alpha, color) {
            const img = frame.image;

            viewerCtx.save();
            viewerCtx.globalAlpha = alpha;

            const scale = Math.min(
                viewerCanvas.width / img.width,
                viewerCanvas.height / img.height
            ) * zoom;

            const w = img.width * scale;
            const h = img.height * scale;

            const x = (viewerCanvas.width - w) / 2 + frame.x;
            const y = (viewerCanvas.height - h) / 2 + frame.y;

            viewerCtx.fillStyle = color;
            viewerCtx.fillRect(x, y, w, h);

            viewerCtx.imageSmoothingEnabled = false;
            viewerCtx.drawImage(img, x, y, w, h);

            viewerCtx.restore();
        }

        // ================================
        // رسم المعاينة
        // ================================

        function renderViewer() {
            viewerCtx.clearRect(
                0,
                0,
                viewerCanvas.width,
                viewerCanvas.height
            );

            if (!frames.length) return;

            if (onionEnabled) {
                for (let i = 1; i <= Math.min(15, currentFrame); i++) {
                    const colorIndex = (i - 1) % 30;
                    const alphaMultiplier = 1 - (i / 30);
                    const finalAlpha = onionOpacity * Math.max(0.1, alphaMultiplier);
                    drawGhostFrame(frames[currentFrame - i], finalAlpha, ghostColors[colorIndex]);
                }

                for (let i = 1; i <= Math.min(15, frames.length - currentFrame - 1); i++) {
                    const colorIndex = (i - 1 + 15) % 30;
                    const alphaMultiplier = 1 - (i / 30);
                    const finalAlpha = onionOpacity * Math.max(0.1, alphaMultiplier);
                    drawGhostFrame(frames[currentFrame + i], finalAlpha, ghostColors[colorIndex]);
                }
            }

            drawFrameOnViewer(frames[currentFrame], 1);
        }

        // ================================
        // عرض الإطارات
        // ================================

        function renderFramesGrid() {
            framesGrid.innerHTML = "";

            frames.forEach(function(frame, index) {
                const div = document.createElement("div");
                div.className = "frame-thumb";
                if (index === currentFrame) div.classList.add("active");

                const canvas = document.createElement("canvas");
                canvas.width = 80;
                canvas.height = 80;

                const c = canvas.getContext("2d");
                c.imageSmoothingEnabled = false;
                c.drawImage(frame.image, 0, 0, 80, 80);

                const label = document.createElement("div");
                label.className = "frame-label";
                label.innerText = index + 1;

                div.appendChild(canvas);
                div.appendChild(label);

                div.onclick = function() {
                    currentFrame = index;
                    renderViewer();
                    renderFramesGrid();
                    renderTimeline();
                    updateStatus();
                };

                framesGrid.appendChild(div);
            });
        }

        // ================================
        // Timeline
        // ================================

        function renderTimeline() {
            timelineTrack.innerHTML = "";

            frames.forEach(function(frame, index) {
                const div = document.createElement("div");
                div.className = "timeline-frame";
                if (index === currentFrame) div.classList.add("active");
                if (frame.x !== 0 || frame.y !== 0) div.classList.add("has-offset");

                const canvas = document.createElement("canvas");
                canvas.width = 40;
                canvas.height = 40;

                const c = canvas.getContext("2d");
                c.imageSmoothingEnabled = false;
                c.drawImage(frame.image, 0, 0, 40, 40);

                div.appendChild(canvas);

                div.onclick = function() {
                    currentFrame = index;
                    renderViewer();
                    renderFramesGrid();
                    renderTimeline();
                    updateStatus();
                };

                timelineTrack.appendChild(div);
            });

            updateTimelineMarker();
            updateStatus();
        }

        function updateTimelineMarker() {
            if (!frames.length) return;
            const percent = (currentFrame / (frames.length - 1)) * 100;
            timelineMarker.style.left = percent + "%";
        }

        // ================================
        // تحريك الإطار
        // ================================

        function moveCurrentFrame(dx, dy) {
            if (!frames.length) return;
            const frame = frames[currentFrame];
            frame.x += dx;
            frame.y += dy;

            renderViewer();
            renderTimeline();
            updateStatus();
        }

        // ================================
        // أزرار التحريك
        // ================================

        moveUp.onclick = function() { moveCurrentFrame(0, -1); };
        moveDown.onclick = function() { moveCurrentFrame(0, 1); };
        moveLeft.onclick = function() { moveCurrentFrame(-1, 0); };
        moveRight.onclick = function() { moveCurrentFrame(1, 0); };

        // ================================
        // لوحة المفاتيح
        // ================================

        document.addEventListener("keydown", function(e) {
            if (!frames.length) return;

            let step = e.shiftKey ? 5 : 1;

            switch (e.key) {
                case "ArrowUp":
                    e.preventDefault();
                    moveCurrentFrame(0, -step);
                    break;

                case "ArrowDown":
                    e.preventDefault();
                    moveCurrentFrame(0, step);
                    break;

                case "ArrowLeft":
                    e.preventDefault();
                    moveCurrentFrame(-step, 0);
                    break;

                case "ArrowRight":
                    e.preventDefault();
                    moveCurrentFrame(step, 0);
                    break;

                case " ":
                    e.preventDefault();
                    if (playing) {
                        stopAnimation();
                    } else {
                        playAnimation();
                    }
                    break;
            }
        });

        // ================================
        // إعادة ضبط الإطار
        // ================================

        resetFrameBtn.onclick = function() {
            if (!frames.length) return;
            frames[currentFrame].x = 0;
            frames[currentFrame].y = 0;

            renderViewer();
            renderTimeline();
            updateStatus();

            showToast("↺ تمت إعادة ضبط الإطار");
        };

        resetAllBtn.onclick = function() {
            frames.forEach(function(f) {
                f.x = 0;
                f.y = 0;
            });

            renderViewer();
            renderTimeline();
            updateStatus();

            showToast("↺ تمت إعادة ضبط جميع الإطارات");
        };

        // ================================
        // Ghost / Onion
        // ================================

        ghostOpacity.oninput = function() {
            onionOpacity = this.value / 100;
            ghostOpacityLabel.textContent = this.value + "%";
            renderViewer();
        };

        ghostPrev.onclick = function() {
            onionEnabled = !onionEnabled;
            renderViewer();
            showToast(
                onionEnabled ?
                "👻 Onion Skinning ON" :
                "👻 Onion Skinning OFF"
            );
        };

        // ================================
        // Animation Preview
        // ================================

        function renderPreview() {
            previewCtx.clearRect(
                0,
                0,
                previewCanvas.width,
                previewCanvas.height
            );

            if (!frames.length) return;

            const frame = frames[currentFrame];
            const img = frame.image;

            const scale = Math.min(
                previewCanvas.width / img.width,
                previewCanvas.height / img.height
            ) * zoom;

            const w = img.width * scale;
            const h = img.height * scale;

            const x = (previewCanvas.width - w) / 2 + frame.x;
            const y = (previewCanvas.height - h) / 2 + frame.y;

            previewCtx.imageSmoothingEnabled = false;
            previewCtx.drawImage(img, x, y, w, h);
        }

        function playAnimation() {
            if (playing || !frames.length) return;

            playing = true;
            lastTime = 0;

            function loop(t) {
                if (!playing) return;

                const fps = Number(fpsSlider.value);

                if (t - lastTime > 1000 / fps) {
                    currentFrame++;

                    if (currentFrame >= frames.length) {
                        if (document.getElementById("loopToggle").checked) {
                            currentFrame = 0;
                        } else {
                            currentFrame = frames.length - 1;
                            playing = false;
                            return;
                        }
                    }

                    renderViewer();
                    renderPreview();
                    renderFramesGrid();
                    renderTimeline();
                    updateStatus();

                    lastTime = t;
                }

                previewRAF = requestAnimationFrame(loop);
            }

            previewRAF = requestAnimationFrame(loop);
        }

        function stopAnimation() {
            playing = false;
            if (previewRAF) {
                cancelAnimationFrame(previewRAF);
                previewRAF = null;
            }
        }

        playBtn.onclick = function() {
            if (playing) {
                stopAnimation();
            } else {
                playAnimation();
            }
        };

        pauseBtn.onclick = stopAnimation;

        stopBtn.onclick = function() {
            stopAnimation();
            currentFrame = 0;
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        prevFrameBtn.onclick = function() {
            if (!frames.length) return;
            currentFrame = Math.max(0, currentFrame - 1);
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        nextFrameBtn.onclick = function() {
            if (!frames.length) return;
            currentFrame = Math.min(frames.length - 1, currentFrame + 1);
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        // ================================
        // FPS
        // ================================

        fpsSlider.oninput = function() {
            fpsValue.innerText = this.value;
        };

        // ================================
        // Zoom
        // ================================

        zoomSlider.oninput = function() {
            zoom = this.value / 100;
            zoomValue.innerText = this.value + "%";
            renderViewer();
            renderPreview();
        };

        // ================================
        // Timeline Buttons
        // ================================

        timelineFirst.onclick = function() {
            if (!frames.length) return;
            currentFrame = 0;
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        timelineLast.onclick = function() {
            if (!frames.length) return;
            currentFrame = frames.length - 1;
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        timelinePrev.onclick = function() {
            if (!frames.length) return;
            currentFrame = Math.max(0, currentFrame - 1);
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        timelineNext.onclick = function() {
            if (!frames.length) return;
            currentFrame = Math.min(frames.length - 1, currentFrame + 1);
            renderViewer();
            renderPreview();
            renderFramesGrid();
            renderTimeline();
            updateStatus();
        };

        // ================================
        // قفل الارتفاع
        // ================================

        lockHeightBtn.onclick = function() {
            lockHeight = !lockHeight;
            this.classList.toggle("active");
            showToast(lockHeight ? "🔒 تم قفل الارتفاع" : "🔓 تم فتح الارتفاع");
        };

        // ================================
        // ضبط الارتفاع التلقائي
        // ================================

        autoHeightBtn.onclick = function() {
            if (!frames.length) {
                showToast("❌ لا توجد إطارات");
                return;
            }

            let totalHeight = 0;
            frames.forEach(function(frame) {
                totalHeight += frame.image.height + Math.abs(frame.y) * 2;
            });
            fixedHeight = Math.round(totalHeight / frames.length) + 3;

            showToast("📏 تم ضبط الارتفاع إلى: " + fixedHeight + "px");
        };

        // ================================
        // Export Sprite Sheet مع مسافة 3px
        // ================================

        exportBtn.onclick = function() {
            if (!frames.length) {
                showToast("❌ لا توجد إطارات للتصدير");
                return;
            }

            let maxWidth = 0;
            let maxHeight = 0;

            frames.forEach(function(frame) {
                maxWidth = Math.max(
                    maxWidth,
                    frame.image.width + Math.abs(frame.x) * 2
                );
                maxHeight = Math.max(
                    maxHeight,
                    frame.image.height + Math.abs(frame.y) * 2
                );
            });

            const spacing = 3;
            const frameWidth = maxWidth + spacing;
            const frameHeight = maxHeight + spacing;

            const cols = 6;
            const rows = Math.ceil(frames.length / cols);

            const finalHeight = lockHeight ? fixedHeight : frameHeight;

            const sheet = document.createElement("canvas");
            sheet.width = cols * frameWidth;
            sheet.height = rows * finalHeight;

            const ctx = sheet.getContext("2d");
            ctx.imageSmoothingEnabled = false;
            ctx.clearRect(0, 0, sheet.width, sheet.height);

            frames.forEach(function(frame, index) {
                const col = index % cols;
                const row = Math.floor(index / cols);

                const cellX = col * frameWidth + spacing / 2;
                const cellY = row * finalHeight + spacing / 2;

                const offsetX = (frameWidth - spacing - frame.image.width) / 2 + frame.x;
                const offsetY = (finalHeight - spacing - frame.image.height) / 2 + frame.y;

                ctx.drawImage(
                    frame.image,
                    cellX + offsetX,
                    cellY + offsetY
                );
            });

            const link = document.createElement("a");
            link.download = "SpriteSheet_Aligned.png";
            link.href = sheet.toDataURL("image/png");
            link.click();

            showToast("✅ تم إنشاء Sprite Sheet مع مسافة 3px");
        };

        // ================================
        // Resize
        // ================================

        window.addEventListener("resize", function() {
            renderViewer();
            renderPreview();
        });

        // ================================
        // بدء التشغيل
        // ================================

        viewerCanvas.width = 700;
        viewerCanvas.height = 700;

        previewCanvas.width = 700;
        previewCanvas.height = 700;

        renderViewer();
        renderPreview();
        updateStatus();

        showToast("🎉 Sprite Align Pro v1.1 جاهز!");
    </script>
</body>
</html>
