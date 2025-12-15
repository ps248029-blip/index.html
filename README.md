<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>高城玲奈 Official Web Site | STARDALIA ENTERTAINMENT</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Noto Sans JP', 'Yu Gothic', 'YuGothic', sans-serif;
            background: #f5f5f5;
            color: #333;
        }

        /* ヘッダー */
        .header {
            background: #1a2f42;
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-box {
            background: #2d4a63;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
        }

        .logo-text {
            color: white;
            font-size: 12px;
            letter-spacing: 1px;
        }

        .nav {
            display: flex;
            gap: 40px;
        }

        .nav a {
            color: white;
            text-decoration: none;
            font-size: 14px;
        }

        /* 画像1: トップセクション（2枚の写真） */
        .top-section {
            background: white;
            padding: 40px;
        }

        .top-content {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .photo-box {
            background: #e8e8e8;
            border-radius: 8px;
            overflow: hidden;
        }

        .photo-placeholder {
            width: 100%;
            aspect-ratio: 3/4;
            background: linear-gradient(135deg, #e0e0e0, #f5f5f5);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #999;
            font-size: 14px;
        }

        .photo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .name-section {
            text-align: center;
            margin-top: 30px;
            grid-column: 1 / -1;
        }

        .name-jp {
            font-size: 48px;
            font-weight: 300;
            letter-spacing: 8px;
            margin-bottom: 10px;
        }

        .name-en {
            font-size: 18px;
            letter-spacing: 3px;
            color: #666;
            border-bottom: 1px solid #333;
            display: inline-block;
            padding-bottom: 5px;
        }

        .contact-info {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 30px;
            font-size: 14px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .social-icon {
            width: 30px;
            height: 30px;
            background: #333;
            border-radius: 3px;
        }

        /* 画像2: プロフィールセクション */
        .profile-section {
            background: white;
            padding: 60px 40px;
            margin-top: 2px;
        }

        .profile-content {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 350px 1fr;
            gap: 50px;
            align-items: start;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            letter-spacing: 4px;
            margin-bottom: 10px;
        }

        .section-subtitle {
            text-align: center;
            font-size: 14px;
            letter-spacing: 2px;
            color: #666;
            border-bottom: 1px solid #333;
            display: inline-block;
            padding-bottom: 5px;
            margin-bottom: 40px;
        }

        .profile-header {
            grid-column: 1 / -1;
            text-align: center;
        }

        .profile-table {
            width: 100%;
            border-collapse: collapse;
        }

        .profile-table tr {
            border-bottom: 1px solid #e0e0e0;
        }

        .profile-table td {
            padding: 15px 10px;
        }

        .profile-table td:first-child {
            width: 150px;
            font-weight: 600;
        }

        /* 画像3: Historyセクション */
        .history-section {
            background-image: url('image-history-bg.jpg');
            background-size: cover;
            background-position: center;
            padding: 60px 40px;
            margin-top: 2px;
            position: relative;
        }

        .history-overlay {
            background: rgba(255, 255, 255, 0.85);
            padding: 40px;
            max-width: 1000px;
            margin: 0 auto;
            border-radius: 10px;
        }

        .history-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-top: 30px;
        }

        .history-category h3 {
            font-size: 18px;
            margin-bottom: 15px;
            color: #1a2f42;
        }

        .history-item {
            margin-bottom: 8px;
            font-size: 14px;
            line-height: 1.8;
        }

        /* 画像4: Fanclubセクション */
        .fanclub-section {
            background-image: url('image-fanclub-bg.jpg');
            background-size: cover;
            background-position: center;
            padding: 80px 40px;
            margin-top: 2px;
            text-align: center;
            position: relative;
        }

        .fanclub-overlay {
            background: rgba(255, 255, 255, 0.9);
            padding: 60px;
            max-width: 800px;
            margin: 0 auto;
            border-radius: 10px;
        }

        .pixel-character {
            width: 150px;
            height: 200px;
            margin: 30px auto;
            background: white;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .pixel-character img {
            width: 100%;
            height: 100%;
            object-fit: contain;
            image-rendering: pixelated;
        }

        .fanclub-links {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .fanclub-links a {
            color: #333;
            text-decoration: none;
            font-size: 14px;
            border-bottom: 1px solid #333;
            padding-bottom: 2px;
        }

        /* フッター */
        .footer {
            background: #1a2f42;
            color: white;
            text-align: center;
            padding: 30px;
            font-size: 12px;
            margin-top: 2px;
        }

        .footer-links {
            margin-bottom: 15px;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 13px;
        }

        @media (max-width: 768px) {
            .top-content,
            .profile-content,
            .history-content {
                grid-template-columns: 1fr;
            }

            .nav {
                gap: 20px;
            }

            .name-jp {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    <!-- ヘッダー -->
    <header class="header">
        <div class="logo-area">
            <div class="logo-box">★</div>
            <div class="logo-text">STARDALIA<br>ENTERTAINMENT</div>
        </div>
        <nav class="nav">
            <a href="#profile">Profile</a>
            <a href="#history">History</a>
            <a href="#fanclub">Fanclub</a>
        </nav>
    </header>

    <!-- 画像1エリア: トップ2枚写真 -->
    <section class="top-section">
        <div class="top-content">
            <div class="photo-box">
                <img src="image1.jpg" alt="高城玲奈 正面写真">
            </div>
            <div class="photo-box">
                <img src="image2.jpg" alt="高城玲奈 横顔写真">
            </div>
            
            <div class="name-section">
                <h1 class="name-jp">高城 玲奈</h1>
                <p class="name-en">Rena Takashiro</p>
                
                <div class="contact-info">
                    <span>📧 rena.takashiro@stardalia.jp</span>
                    <span>📧 info@stardalia.jp</span>
                    <div class="social-icons">
                        <div class="social-icon"></div>
                        <div class="social-icon"></div>
                    </div>
                    <a href="#" style="color: #333; text-decoration: none;">メールでご連絡ください</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 画像2エリア: プロフィール -->
    <section id="profile" class="profile-section">
        <div class="profile-content">
            <div class="profile-header">
                <h2 class="section-title">高城 玲奈</h2>
                <p class="section-subtitle">Rena Takashiro</p>
            </div>
            
            <div class="photo-box">
                <img src="image3.jpg" alt="高城玲奈 プロフィール写真">
            </div>
            
            <div>
                <table class="profile-table">
                    <tr>
                        <td>Age</td>
                        <td>23歳</td>
                    </tr>
                    <tr>
                        <td>Birthday</td>
                        <td>2002年10月9日</td>
                    </tr>
                    <tr>
                        <td>Native Place</td>
                        <td>神奈川県横浜市</td>
                    </tr>
                    <tr>
                        <td>Height</td>
                        <td>162cm</td>
                    </tr>
                    <tr>
                        <td>Blood</td>
                        <td>A型</td>
                    </tr>
                    <tr>
                        <td>Speciality</td>
                        <td>ピアノ</td>
                    </tr>
                </table>
            </div>
        </div>
    </section>

    <!-- 画像3エリア: History -->
    <section id="history" class="history-section">
        <div class="history-overlay">
            <div style="text-align: center;">
                <h2 class="section-title" style="color: #ff69b4; font-family: cursive;">history</h2>
            </div>
            
            <div class="history-content">
                <div>
                    <div class="history-category">
                        <h3>映画</h3>
                        <div class="history-item">『夏空に沿けて』(2019年)</div>
                        <div class="history-item">『風のなりか』(2021年)</div>
                        <div class="history-item">『心音-しんおん-』(2023年)</div>
                        <div class="history-item">『月とアトリエ』(2024年)</div>
                        <div class="history-item">『星降る夜に、もう一度』(2025年)</div>
                    </div>
                    
                    <div class="history-category" style="margin-top: 30px;">
                        <h3>ドラマ</h3>
                        <div class="history-item">『静寂の街』(2022年／NHK)</div>
                        <div class="history-item">『恋の残響』(2023年／TBS)</div>
                        <div class="history-item">『AFTERGLOW』(2023年／Netflix)</div>
                        <div class="history-item">『シンデレラ・ブルー』(2025年／Netflix)</div>
                    </div>
                </div>
                
                <div>
                    <div class="history-category">
                        <h3>受賞歴</h3>
                        <div class="history-item">第45回シルバースクリーン映画祭 最優秀助演女優賞</div>
                        <div class="history-item">（『風のなりか』／2021年）</div>
                        <div class="history-item" style="margin-top: 10px;">第10回クリスタルドラマアワード主演女優賞</div>
                        <div class="history-item">（『静寂の街』／2022年）</div>
                        <div class="history-item" style="margin-top: 10px;">日本フィルムアーツ大賞 最優秀主演女優賞</div>
                        <div class="history-item">（『月とアトリエ』／2024年）</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 画像4エリア: Fanclub -->
    <section id="fanclub" class="fanclub-section">
        <div class="fanclub-overlay">
            <h2 class="section-title">高城玲奈 Official Web Site</h2>
            <h3 style="font-size: 24px; margin-top: 20px;">高城玲奈 Official Fanclub</h3>
            
            <div class="pixel-character">
                <img src="image4.jpg" alt="高城玲奈 ピクセルアート">
            </div>
            
            <p style="margin-top: 20px;">女優・アーティストとして活動中。<br>最新情報や出演情報はこちらの公式サイトから見ることができます。</p>
            
            <div class="fanclub-links">
                <a href="#">サイトについて</a>
                <a href="#">利用規約</a>
            </div>
        </div>
    </section>

    <!-- フッター -->
    <footer class="footer">
        <div class="footer-links">
            <a href="#">サイトについて</a>
            <a href="#">利用規約</a>
        </div>
        <p>© Stardalia Entertainment Promotion</p>
    </footer>
</body>
</html>
