[index.html.html](https://github.com/user-attachments/files/29285823/index.html.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>圈圈小屋 · dyh的小圈圈</title>
    <!-- 引用圆润优雅的字体 -->
    @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&display=swap');
    <style>
        /* --- 全局样式初始化 --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html {
            scroll-behavior: smooth; /* 全局平滑滚动 */
        }
        body {
            font-family: 'Nunito', 'PingFang SC', 'Microsoft YaHei', sans-serif;
            background-color: #fefbf6;
            color: #4a3125;
            line-height: 1.6;
        }
        a {
            text-decoration: none;
            color: inherit;
        }

        /* --- 1. 导航栏 --- */
        nav {
            position: sticky;
            top: 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 5%;
            background-color: rgba(255, 249, 239, 0.92);
            backdrop-filter: blur(8px);
            box-shadow: 0 2px 15px rgba(255, 193, 7, 0.1);
            z-index: 100;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            color: #e8a838;
            letter-spacing: 2px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }
        .nav-links a {
            font-size: 1.1rem;
            font-weight: 600;
            color: #5a4033;
            transition: color 0.3s ease;
        }
        .nav-links a:hover {
            color: #f3b33d;
        }

        /* --- 2. Banner 区域 --- */
        #dyh-banner {
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: linear-gradient(145deg, #fff4e0 0%, #ffeec9 100%);
            padding: 0 5%;
            position: relative;
        }
        #dyh-banner h1 {
            font-size: 3.8rem;
            color: #4a3125;
            margin-bottom: 1rem;
            letter-spacing: 4px;
        }
        #dyh-banner h1 span {
            color: #f3b33d;
        }
        #dyh-banner p {
            font-size: 1.6rem;
            color: #b8884c;
            font-weight: 600;
            letter-spacing: 6px;
            margin-top: 10px;
        }
        #dyh-banner p i {
            font-style: normal;
            background-color: #f3b33d;
            color: #fff;
            padding: 0 10px;
            border-radius: 20px;
            font-weight: 800;
        }

        /* --- 3. 三大产品板块 --- */
        #products {
            padding: 4rem 5%;
            background-color: #ffffff;
        }
        #products h2 {
            text-align: center;
            font-size: 2.2rem;
            color: #4a3125;
            margin-bottom: 0.5rem;
        }
        #products .subtitle {
            text-align: center;
            color: #b8884c;
            font-size: 1rem;
            margin-bottom: 3rem;
        }
        .product-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2.5rem;
        }
        .product-card {
            background: #fefbf6;
            border-radius: 25px;
            padding: 2rem 1.5rem;
            width: 300px;
            box-shadow: 0 8px 25px rgba(243, 179, 61, 0.12);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
            border: 1px solid #fff3e0;
        }
        .product-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 18px 35px rgba(243, 179, 61, 0.2);
            border-color: #f3b33d;
        }
        /* 更新：替换为真实图片占位符 */
        .card-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 15px;
            margin-bottom: 1.2rem;
            background-color: #f9f3e8; /* 图片加载失败时的底色 */
        }
        .product-card h3 {
            font-size: 1.6rem;
            color: #4a3125;
            margin-bottom: 0.5rem;
            letter-spacing: 1px;
        }
        .product-card h3 span {
            color: #f3b33d;
        }
        .product-card p {
            color: #7a6253;
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
        }
        /* 更新：按钮改为 a 标签，支持跳转链接 */
        .buy-btn {
            display: inline-block;
            background: #f3b33d;
            color: #4a3125;
            padding: 0.5rem 1.8rem;
            border-radius: 30px;
            font-weight: 700;
            transition: background 0.3s, color 0.3s, transform 0.2s;
            cursor: pointer;
            border: none;
            font-family: inherit;
        }
        .buy-btn:hover {
            background: #e8a838;
            color: white;
            transform: scale(1.05);
        }

        /* --- 4. 底部区域 --- */
        #contact {
            background-color: #4a3125;
            color: #fefbf6;
            padding: 3.5rem 5% 1.5rem;
            text-align: center;
        }
        .footer-content p {
            margin: 0.5rem 0;
            opacity: 0.9;
            font-size: 1rem;
        }
        .footer-btn {
            background: #f3b33d;
            color: #4a3125;
            border: none;
            padding: 0.8rem 2.5rem;
            font-size: 1.1rem;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 800;
            margin: 1.5rem 0 2.5rem;
            transition: transform 0.2s, background 0.3s;
            box-shadow: 0 4px 15px rgba(243, 179, 61, 0.3);
        }
        .footer-btn:hover {
            transform: scale(1.05);
            background: #fad67e;
        }
        .copyright {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 1.5rem;
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* --- 5. 弹窗 (Modal) --- */
        .modal {
            display: none; 
            position: fixed;
            z-index: 999;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(74, 49, 37, 0.6);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background: #fefbf6;
            padding: 2.5rem 3rem;
            border-radius: 25px;
            text-align: center;
            max-width: 420px;
            width: 90%;
            position: relative;
            border: 2px solid #f3b33d;
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
        }
        .modal-content h2 {
            color: #4a3125;
            margin-bottom: 0.8rem;
        }
        .modal-content .emoji-big {
            font-size: 3rem;
            display: block;
            margin-bottom: 1rem;
        }
        .modal-content p {
            color: #7a6253;
            font-size: 1rem;
        }
        .close-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2rem;
            cursor: pointer;
            color: #b8884c;
            transition: color 0.3s, transform 0.3s;
        }
        .close-btn:hover {
            color: #f3b33d;
            transform: rotate(90deg);
        }

        /* --- 6. 新增：回到顶部按钮 --- */
        #back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: #f3b33d;
            color: #4a3125;
            border-radius: 50%;
            display: none; /* 默认隐藏 */
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: bold;
            box-shadow: 0 4px 15px rgba(243, 179, 61, 0.4);
            cursor: pointer;
            transition: opacity 0.3s, transform 0.3s;
            z-index: 1000;
            border: none;
        }
        #back-to-top:hover {
            transform: translateY(-5px);
            background-color: #e8a838;
        }

        /* --- 响应式适配 --- */
        @media (max-width: 768px) {
            .logo { font-size: 1.4rem; }
            .nav-links { gap: 1rem; }
            .nav-links a { font-size: 0.9rem; }
            #dyh-banner h1 { font-size: 2.4rem; }
            #dyh-banner p { font-size: 1.2rem; }
            .product-card { width: 100%; max-width: 360px; }
            #back-to-top { width: 45px; height: 45px; font-size: 1.4rem; bottom: 20px; right: 20px; }
        }
    </style>
</head>
<body>

    <!-- 1. 导航栏 -->
    <nav>
        <div class="logo">⭕ 圈圈小屋</div>
        <ul class="nav-links">
            <li><a href="#dyh-banner">首页</a></li>
            <li><a href="#products">圈圈好物</a></li>
            <li><a href="#contact">联系我们</a></li>
        </ul>
    </nav>

    <!-- 2. Banner 区域 -->
    <section id="dyh-banner">
        <h1>dyh 的 <span>小圈圈</span></h1>
        <p>探索 · <i>生活的小确幸</i></p>
    </section>

    <!-- 3. 三大板块卡片 -->
    <section id="products">
        <h2>🌻 圈圈生活指南</h2>
        <p class="subtitle">涵盖衣、食、行，打造属于你的精致日常</p>
        <div class="product-grid">
            
            <!-- 板块一：圈圈衣服 -->
            <div class="product-card">
                <!-- 真实图片占位符（替换 src 中的链接即可换成您的商品图） -->
                <img src="clothes.jpg" alt="圈圈衣服" class="card-img" loading="lazy">
                <h3>圈圈<span>衣服</span></h3>
                <p>主打亲肤天然棉麻，简约不简单的日常穿搭，每一件都包裹着暖暖的舒适感。</p>
                <!-- 增加跳转链接 -->
                <a href="https://www.example.com/clothes" target="_blank" class="buy-btn">探索穿搭 →</a>
            </div>

            <!-- 板块二：圈圈饮食 -->
            <div class="product-card">
                <img src="food.jpg" alt="圈圈饮食" class="card-img" loading="lazy">
                <h3>圈圈<span>饮食</span></h3>
                <p>甄选时令鲜食与粗粮谷物，低卡轻负担，用心烹饪，只为治愈每一天的味蕾。</p>
                <a href="https://www.example.com/food" target="_blank" class="buy-btn">探索食谱 →</a>
            </div>

            <!-- 板块三：圈圈运动 -->
            <div class="product-card">
                <img src="run.jpg" alt="圈圈运动" class="card-img" loading="lazy">
                <h3>圈圈<span>运动</span></h3>
                <p>从瑜伽垫到轻量化运动装备，陪伴你在每一个清晨挥洒汗水，收获健康活力。</p>
                <a href="https://www.example.com/sports" target="_blank" class="buy-btn">探索装备 →</a>
            </div>

        </div>
    </section>

    <!-- 4. 底部及联系方式 -->
    <footer id="contact">
        <div class="footer-content">
            <p style="font-size: 1.2rem; font-weight: bold;">圈圈小屋 · 客服中心</p>
            <p>📞 客服电话：17706718559</p>
            <p>📍 项家13 号 · 圈圈恶犬园</p>
            <p>📧 邮箱：561331620@qq.com</p>
            <button class="footer-btn" id="contactBtn">✨ 联系我们 ✨</button>
            <div class="copyright">
                &copy; 2026 圈圈小屋 | dyh的小圈圈 温暖出品
            </div>
        </div>
    </footer>

    <!-- 5. 弹窗结构 -->
    <div id="contactModal" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <span class="emoji-big">💌</span>
            <h2>圈圈收到了！</h2>
            <p>感谢您的关注！<br>我们将在 <strong>1小时内</strong> 加急回复，期待与您在圈圈相遇~</p>
        </div>
    </div>

    <!-- 6. 回到顶部按钮 (新增 HTML) -->
    <button id="back-to-top" title="回到顶部">↑</button>

    <!-- 7. JS 交互逻辑 -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // --- 弹窗交互 ---
            const modal = document.getElementById('contactModal');
            const contactBtn = document.getElementById('contactBtn');
            const closeBtn = document.querySelector('.close-btn');

            contactBtn.addEventListener('click', function() {
                modal.style.display = 'flex';
            });

            closeBtn.addEventListener('click', function() {
                modal.style.display = 'none';
            });

            window.addEventListener('click', function(event) {
                if (event.target === modal) {
                    modal.style.display = 'none';
                }
            });

            // --- 回到顶部交互 (新增 JS) ---
            const backToTopBtn = document.getElementById('back-to-top');

            // 监听滚动事件：滚动超过 300px 显示按钮
            window.addEventListener('scroll', function() {
                if (window.scrollY > 300) {
                    backToTopBtn.style.display = 'flex';
                } else {
                    backToTopBtn.style.display = 'none';
                }
            });

            // 点击按钮平滑回到顶部
            backToTopBtn.addEventListener('click', function() {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
