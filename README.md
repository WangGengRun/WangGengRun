<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>打字机风格 · GitHub 个人主页</title>
    <!-- 引入谷歌字体，让打字机风格更复古 -->
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600;700&family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (免费图标库，用于社交图标) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;   /* GitHub 暗色主题背景 */
            font-family: 'Inter', 'Fira Code', monospace, system-ui;
            color: #e6edf3;
            line-height: 1.5;
            padding: 2rem 1rem;
            display: flex;
            justify-content: center;
            min-height: 100vh;
        }

        /* 主容器 —— 模拟类似 README 卡片但保留可读性 */
        .container {
            max-width: 960px;
            width: 100%;
            background: #0d1117;
            border-radius: 24px;
            padding: 1.8rem 2rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.5);
            border: 1px solid #30363d;
        }

        /* 打字机核心区块 */
        .typewriter-section {
            margin-bottom: 2.5rem;
            border-left: 4px solid #58a6ff;
            padding-left: 1.2rem;
            background: #161b22;
            border-radius: 0 16px 16px 0;
            padding: 1.2rem 1.5rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.3);
        }

        /* 动态打字容器 */
        .typewriter {
            font-family: 'Fira Code', 'Courier New', monospace;
            font-size: 1.3rem;
            font-weight: 500;
            color: #f0f6fc;
            white-space: pre-wrap;
            word-break: break-word;
            line-height: 1.6;
        }

        /* 闪烁光标 (模拟打字机) */
        .cursor-blink {
            display: inline-block;
            width: 10px;
            height: 1.3rem;
            background-color: #58a6ff;
            vertical-align: middle;
            margin-left: 4px;
            animation: blink 1s step-end infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* 控制台风格的装饰线 */
        .console-line {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.85rem;
            color: #8b949e;
            margin-top: 12px;
            font-family: monospace;
        }

        .prompt {
            color: #3fb950;
        }

        /* 卡片样式通用 */
        .card {
            background: #161b22;
            border-radius: 20px;
            padding: 1.2rem 1.5rem;
            margin-top: 2rem;
            border: 1px solid #30363d;
            transition: all 0.2s;
        }

        .card h2 {
            font-size: 1.6rem;
            font-weight: 600;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 12px;
            border-bottom: 2px dashed #30363d;
            padding-bottom: 0.5rem;
        }

        .badge-list {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 1.2rem 0;
        }

        .tech-icon {
            background: #21262d;
            border-radius: 40px;
            padding: 6px 14px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            font-family: 'Fira Code', monospace;
            transition: 0.2s;
        }

        .tech-icon i, .tech-icon img {
            font-size: 1.2rem;
        }

        /* 社交链接 */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 24px;
            margin: 20px 0 10px;
        }
        .social-btn {
            background: #21262d;
            padding: 8px 16px;
            border-radius: 40px;
            text-decoration: none;
            color: #c9d1d9;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: 0.2s;
            border: 1px solid #30363d;
        }
        .social-btn:hover {
            background: #30363d;
            color: #ffffff;
            transform: translateY(-2px);
        }

        /* 统计占位 & 数据卡片 */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-between;
        }
        .stat-card {
            flex: 1;
            background: #0d1117;
            border-radius: 16px;
            padding: 1rem;
            text-align: center;
            border: 1px solid #30363d;
        }

        /* 项目列表 */
        .project-item {
            margin-bottom: 1rem;
            padding-bottom: 0.8rem;
            border-bottom: 1px solid #30363d;
        }
        .project-title {
            font-weight: bold;
            font-size: 1.1rem;
        }
        .project-title a {
            color: #58a6ff;
            text-decoration: none;
        }
        .project-desc {
            color: #b1bac4;
            font-size: 0.9rem;
            margin-top: 5px;
        }

        footer {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.8rem;
            color: #6e7681;
            border-top: 1px solid #21262d;
            padding-top: 1.5rem;
        }

        @media (max-width: 680px) {
            .container {
                padding: 1rem;
            }
            .typewriter {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <!-- 动态打字机区域 -->
    <div class="typewriter-section">
        <div class="typewriter" id="typewriter"></div>
        <div class="console-line">
            <span class="prompt">➜</span> <span id="cursorLine">~ 欢迎光临我的代码宇宙</span>
        </div>
    </div>

    <!-- 以下是正常展示区域，但是也会配合渐入动画（无打字但视觉增强） -->
    <div class="social-links" id="social-area">
        <a href="#" class="social-btn" target="_blank"><i class="fab fa-github"></i> GitHub</a>
        <a href="#" class="social-btn" target="_blank"><i class="fab fa-twitter"></i> Twitter</a>
        <a href="#" class="social-btn" target="_blank"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="#" class="social-btn" target="_blank"><i class="fas fa-envelope"></i> 邮箱</a>
    </div>

    <!-- 关于我卡片，稍后部分也会有渐变出现 -->
    <div class="card" id="about-card">
        <h2><i class="fas fa-terminal"></i> 关于我<span style="font-size:0.8rem;">&nbsp;~ $ whoami</span></h2>
        <p>✨ 全栈开发者 & 开源爱好者 · 热衷于构建优雅的交互与高性能应用。<br>
        🔭 目前专注于 <strong>React · Node.js · TypeScript · AI 应用</strong><br>
        🌱 2025 年目标：深入 Rust 与边缘计算，贡献更多开源工具。<br>
        ⚡ 趣味向：代码洁癖 | 复古机械键盘控 | 咖啡因驱动 ☕<br>
        💬 任何关于前端工程化、全栈设计的问题，欢迎与我交流。
        </p>
        <div class="badge-list" id="tech-badges">
            <span class="tech-icon"><i class="fab fa-js"></i> JavaScript/TS</span>
            <span class="tech-icon"><i class="fab fa-react"></i> React</span>
            <span class="tech-icon"><i class="fab fa-node-js"></i> Node.js</span>
            <span class="tech-icon"><i class="fab fa-python"></i> Python</span>
            <span class="tech-icon"><i class="fas fa-database"></i> PostgreSQL</span>
            <span class="tech-icon"><i class="fab fa-docker"></i> Docker</span>
            <span class="tech-icon"><i class="fas fa-code-branch"></i> Git/GitHub Actions</span>
        </div>
    </div>

    <!-- GitHub 统计占位(展示漂亮的静态仿 stats 卡，但实际可以用真实API) 但是为了打印机风格统一，保留动态加载的文字小彩蛋-->
    <div class="card" id="stats-card">
        <h2><i class="fas fa-chart-line"></i> GitHub 脉搏</h2>
        <div class="stats-row">
            <div class="stat-card">
                <i class="fas fa-code-branch" style="font-size: 2rem; color:#2f81f7;"></i>
                <h3 id="repo-count">--</h3>
                <p>公共仓库</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-star" style="font-size: 2rem; color:#e3b341;"></i>
                <h3 id="star-count">--</h3>
                <p>累计 Stars</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-user-friends" style="font-size: 2rem; color:#57ab5a;"></i>
                <h3 id="follow-count">--</h3>
                <p>追随者</p>
            </div>
        </div>
        <p style="margin-top: 16px; font-family: monospace; text-align: center;">⚡ 这些数据会随着 GitHub 动态更新，就像打印机输出实时状态~</p>
        <div style="margin-top: 12px; background: #0d1117; border-radius: 12px; padding: 12px;">
            <img id="github-stats-img" src="https://github-readme-stats.vercel.app/api?username=你的GitHub用户名&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=79c0ff&text_color=c9d1d9" alt="GitHub Stats" width="100%" style="border-radius: 12px; max-width: 100%;">
        </div>
    </div>

    <!-- 精选项目 带有打字机纪念 -->
    <div class="card" id="projects-card">
        <h2><i class="fas fa-laptop-code"></i> 匠心项目 · 打印出品</h2>
        <div class="project-item">
            <div class="project-title">📟 <a href="#">TypeWriter Portfolio</a> <span style="font-size:0.7rem;">[正在热映]</span></div>
            <div class="project-desc">采用打字机效果的个人主页——灵感源自老式电报与终端模拟，生动展示开发者旅程。</div>
        </div>
        <div class="project-item">
            <div class="project-title">🧠 <a href="#">AI Content Studio</a></div>
            <div class="project-desc">基于大语言模型的辅助创作平台，支持实时文档生成 & 智能摘要，日活用户 5k+。</div>
        </div>
        <div class="project-item">
            <div class="project-title">🚀 <a href="#">next-saas-starter</a></div>
            <div class="project-desc">现代全栈脚手架 (Next.js + Tailwind + Prisma) ，内置认证、支付集成。已收获 380+ stars.</div>
        </div>
        <div class="project-item">
            <div class="project-title">🎨 <a href="#">terminal-chat-ui</a></div>
            <div class="project-desc">极客风格命令行聊天界面，WebSocket 实时通信，仿终端的体验。</div>
        </div>
    </div>

    <!-- 最新动态/文章区块 模拟博客列表-->
    <div class="card" id="blog-card">
        <h2><i class="fas fa-newspaper"></i> 最近·墨迹未干</h2>
        <ul style="list-style: none; margin-top: 8px;">
            <li style="margin-bottom: 12px;">📄 <strong>《从零实现终端打字机动画：CSS+JS 复古浪漫》</strong> —— 深度剖析逐字输出原理 → <span style="color:#58a6ff;">阅读全文</span></li>
            <li style="margin-bottom: 12px;">📄 <strong>《2025 全栈架构演进：Serverless 真的适合你吗？》</strong> —— 实践经验总结 → <span style="color:#58a6ff;">即刻翻阅</span></li>
            <li style="margin-bottom: 12px;">📄 <strong>《GitHub Profile 个性化完全指南》</strong> —— 让你的主页会“说话” → <span style="color:#58a6ff;">浏览详情</span></li>
        </ul>
    </div>
    <footer>
        <i class="fas fa-terminal"></i> 访客计数: <span id="visitor-count">正在统计...</span> &nbsp;&nbsp;|&nbsp;&nbsp;
        <i class="fas fa-crown"></i> 打印机模式 · 每个字符皆匠心
    </footer>
</div>

<script>
    // ********************************************
    // 打字机效果核心: 一行一行、一个字一个字输出
    // ********************************************
    // 要打印的完整文本 (支持多行，保留空格和标点，这里使用模拟个人介绍)
    const fullText = `>_ Hello, 世界！ 👋 我是 [你的名字] ，一名将创意编译成代码的开发者。\n>_ 欢迎来到我的 GitHub 维度 —— 这里每行代码就像打印机墨迹，\n>_ 缓缓渗出逻辑与热情。当前系统在线，准备就绪。\n>_ 可用命令: 探索项目 · 切磋技术 · 共同构建更好网络 🌍`;

    let index = 0;
    const typewriterElement = document.getElementById('typewriter');
    // 光标动态效果容器 (我们将在同一行内动态追加html，包含光标)
    // 优雅处理:
    function updateTyping() {
        if (index < fullText.length) {
            // 逐个字符添加，保留换行符转换为 <br>
            let currentChar = fullText[index];
            if (currentChar === '\n') {
                typewriterElement.innerHTML += '<br>';
            } else {
                typewriterElement.innerHTML += currentChar;
            }
            index++;
            setTimeout(updateTyping, 50); // 每个字符间隔 50ms，模拟打字机节奏
        } else {
            // 打字结束，在末尾加一个静态闪烁光标(增强效果)
            const cursorSpan = document.createElement('span');
            cursorSpan.className = 'cursor-blink';
            typewriterElement.appendChild(cursorSpan);
            // 同时改变下面命令行区域显示为ready
            document.getElementById('cursorLine').innerHTML = '~ 系统就绪，继续滚动精彩 ✨';
        }
    }

    // 开始打印机欢迎语 (页面加载启动)
    window.addEventListener('DOMContentLoaded', () => {
        // 清空占位
        typewriterElement.innerHTML = '';
        updateTyping();

        // 以下是一些动态加载GitHub数据(真实或模拟？为了演示效果，使用fetch获取真实用户数据但需要填入真实用户名)
        // 请把 "你的GitHub用户名" 替换成真正的用户名，否则API返回默认演示
        // 获取真实数据改进体验
        const ghUsername = '你的GitHub用户名';   // 👈 重要！ 将这里修改为自己的 GitHub 用户名
        // 注意 如果用户名是中文或者特殊 保持原样
        if (ghUsername !== '你的GitHub用户名') {
            fetch(`https://api.github.com/users/${ghUsername}`)
                .then(res => res.json())
                .then(data => {
                    if (data && !data.message) {
                        document.getElementById('repo-count').innerText = data.public_repos ?? '--';
                        document.getElementById('follow-count').innerText = data.followers ?? '--';
                    } else {
                        document.getElementById('repo-count').innerText = '?';
                        document.getElementById('follow-count').innerText = '?';
                    }
                })
                .catch(() => {
                    document.getElementById('repo-count').innerText = 'err';
                    document.getElementById('follow-count').innerText = 'err';
                });
            // 模拟 stars 总数(可用另外接口较复杂, 展示趣味近似或者用readme-stats近似)
            // 这里简单用个动态预估或者展示动态风格,为了演示，我们使用有趣的估计：获取用户仓库然后累加star需要跨域或者小心。简化优雅一点：通过另一个服务
            // 为了不复杂，手动展示一个模拟渐变值 -> 也可以通过读取html中的img异步获取，但为了美观给出一个占位动态更新
            fetch(`https://api.github.com/users/${ghUsername}/repos?per_page=100`)
                .then(res => res.json())
                .then(repos => {
                    if (Array.isArray(repos) && !repos.message) {
                        let totalStars = repos.reduce((acc, repo) => acc + (repo.stargazers_count || 0), 0);
                        document.getElementById('star-count').innerText = totalStars;
                    } else {
                        document.getElementById('star-count').innerText = '❤️';
                    }
                }).catch(() => document.getElementById('star-count').innerText = '★');
        } else {
            // 占位演示数据 (如果未修改用户名)
            document.getElementById('repo-count').innerText = '24';
            document.getElementById('star-count').innerText = '387';
            document.getElementById('follow-count').innerText = '142';
            // 同时也更新图片中的username占位图片url为演示用户，让视觉友好但提示修改
            const statsImg = document.getElementById('github-stats-img');
            if (statsImg) {
                statsImg.src = 'https://github-readme-stats.vercel.app/api?username=octocat&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117';
            }
        }

        // 访客计数器: 使用免费的计数器API (示例使用countapi? 简单点演示, 可用本地localstorage假装趣味)
        // 实际正式可更换为 https://visitor-badge.glitch.me/ 之类, 下面展示模拟动态更新，让访客看到真实+1感觉
        let visitCount = localStorage.getItem('visit_demo_count');
        if (!visitCount) {
            visitCount = 1280; // 初始展示
        } else {
            visitCount = Number(visitCount) + 1;
        }
        localStorage.setItem('visit_demo_count', visitCount);
        document.getElementById('visitor-count').innerText = visitCount + ' 次墨水印记';
    });

    // 更多细节: 让项目链接都加上真实链接可自定义（点击社交按钮替换为自己真实链接, 这里为了方便编辑, 默认等待用户自己替换href）
    // 修改社交链接: 挑选自定义编辑示例，让用户直接修改以下DOM属性
    const socialLinks = document.querySelectorAll('.social-btn');
    if (socialLinks.length) {
        // 可以根据需要修改，也可以在控制台提示，这里简单映射让用户修改
        // 因为无法知道用户的真实地址，这里提示用title属性展示占位
        socialLinks[0].href = "https://github.com/你的GitHub用户名";   // 改成自己的github
        socialLinks[1].href = "https://twitter.com/你的用户名";
        socialLinks[2].href = "https://linkedin.com/in/你的linkedin";
        socialLinks[3].href = "mailto:yourname@example.com";
    }

    // 可选: 对项目区域<a>的链接更新占位
    const projectLinks = document.querySelectorAll('.project-title a');
    if (projectLinks.length) {
        projectLinks[0].href = "https://github.com/你的用户名/typewriter-profile";
        projectLinks[1].href = "https://github.com/你的用户名/ai-content-studio";
        projectLinks[2].href = "https://github.com/你的用户名/next-saas-starter";
        projectLinks[3].href = "https://github.com/你的用户名/terminal-chat-ui";
    }
    // 博文区域链接占位
    const blogLinks = document.querySelectorAll('#blog-card li span');
    // 简单为每个文章增加点击友好提醒
    for (let i = 0; i < blogLinks.length; i++) {
        if(blogLinks[i].innerText.includes('阅读全文')||blogLinks[i].innerText.includes('即刻翻阅')||blogLinks[i].innerText.includes('浏览详情')) {
            blogLinks[i].style.cursor = 'pointer';
            blogLinks[i].style.textDecoration = 'underline';
            blogLinks[i].addEventListener('click', () => {
                alert('📖 文章详细链接待配置，请将实际博客链接替换到此处 ✨');
            });
        }
    }

    // 头像可选：给typewriter区显示动效logo，无伤大雅
    // 替换统计图标的用户名动态
    const currentUsername = '你的GitHub用户名';
    if(currentUsername !== '你的GitHub用户名') {
        const statsImg = document.getElementById('github-stats-img');
        if(statsImg) {
            statsImg.src = `https://github-readme-stats.vercel.app/api?username=${currentUsername}&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=79c0ff&text_color=c9d1d9`;
        }
    }
</script>
</body>
</html>
