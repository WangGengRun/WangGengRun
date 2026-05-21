# Hello World!

<div align="center">
<!-- 浅蓝色多行终端打字机组件（顺序打印，全留存，不循环） -->
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 130" width="500" height="130">
    <style>
      .terminal-text {
        font-family: 'Fira Code', 'Courier New', monospace;
        font-size: 18px;
        fill: #87CEEB;
        white-space: pre;
      }
      .line1 { animation: type1 1.5s steps(30) forwards; }
      .line2 { opacity: 0; animation: type2 1.5s steps(30) 1.5s forwards; }
      .line3 { opacity: 0; animation: type3 1s steps(20) 3.0s forwards; }
      .line4 { opacity: 0; animation: type4 2s steps(40) 4.0s forwards; }
      
      @keyframes type1 { from { width: 0; } to { width: 500px; } }
      @keyframes type2 { from { opacity: 1; width: 0; } to { opacity: 1; width: 500px; } }
      @keyframes type3 { from { opacity: 1; width: 0; } to { opacity: 1; width: 500px; } }
      @keyframes type4 { from { opacity: 1; width: 0; } to { opacity: 1; width: 500px; } }
    </style>
    <g class="terminal-text">
      <!-- 这里的 clip-path 模拟了打字机的光标推进和保留效果 -->
      <svg x="20" y="25" width="500" height="25" class="line1">
        <text x="0" y="18">> I'm GodspRun.</text>
      </svg>
      <svg x="20" y="50" width="500" height="25" class="line2">
        <text x="0" y="18">> A Software Development Engineer.</text>
      </svg>
      <svg x="20" y="75" width="500" height="25" class="line3">
        <text x="0" y="18">> An Anime Enthusiast.</text>
      </svg>
      <svg x="20" y="100" width="500" height="25" class="line4">
        <text x="0" y="18">> Keep Learning, Keep Progressing.</text>
      </svg>
    </g>
  </svg>
  <p align="center">
    <strong>👋 你好，我是GodspRun，一名程序员，也是一名动漫爱好者。</strong> <br />
  </p>

</div>

