<svg width="600" height="320" xmlns="http://www.w3.org/2000/svg">
    <!-- 
      /dev/urandom animation for GitHub Profile README
      Author: Gemini
      This SVG uses CSS animation to create a pseudo-random character stream effect.
    -->
    <defs>
        <style>
            @import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
            .terminal-text {
                font-family: 'VT323', monospace;
                font-size: 18px;
                fill: #58a6ff;
                /* Animation to flicker text layers */
                animation-name: flicker;
                animation-duration: 2s;
                animation-iteration-count: infinite;
                opacity: 0; /* Start hidden */
            }
            /* Stagger the animation for each text layer */
            .text-1 { animation-delay: 0s; }
            .text-2 { animation-delay: 0.5s; }
            .text-3 { animation-delay: 1s; }
            .text-4 { animation-delay: 1.5s; }
            
            @keyframes flicker {
                0% { opacity: 0; }
                25% { opacity: 1; }
                50% { opacity: 0; }
                100% { opacity: 0; }
            }
        </style>
    </defs>

    <!-- Terminal Window -->
    <rect x="1" y="1" width="598" height="318" rx="6" stroke="#30363d" fill="#0d1117" stroke-width="1"/>
    
    <!-- Terminal Header -->
    <rect x="1" y="1" width="598" height="30" rx="6" ry="6" fill="#161b22" stroke="#30363d" stroke-width="1"/>
    <circle cx="20" cy="16" r="6" fill="#ef4444"/>
    <circle cx="40" cy="16" r="6" fill="#f59e0b"/>
    <circle cx="60" cy="16" r="6" fill="#10b981"/>
    <text x="300" y="21" fill="#9ca3af" font-family="sans-serif" font-size="12" text-anchor="middle">
        bash &mdash; /dev/urandom
    </text>

    <!-- Random Text Layers (positioned on top of each other) -->
    <!-- We create multiple layers and fade them in and out to simulate a changing screen -->
    <text x="15" y="55" class="terminal-text text-1">
        <tspan x="15" dy="1.2em">iH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)c</tspan>
        <tspan x="15" dy="1.2em">a@R8!qZ$gW*vF^lB7yC^e@jS)tXp%nVb^sU&amp;mI^e@jK)wD(oI#b8@L</tspan>
        <tspan x="15" dy="1.2em">z^tY)cQd9!kR(wI^e@pQd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t</tspan>
        <tspan x="15" dy="1.2em">Y)cQd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5</tspan>
        <tspan x="15" dy="1.2em">sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)cQd9!kR(wI^e@pQz^tY)c</tspan>
        <tspan x="15" dy="1.2em">wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQ</tspan>
        <tspan x="15" dy="1.2em">pS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!j</tspan>
        <tspan x="15" dy="1.2em">Xp%nVb^sU&amp;mI^e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5</tspan>
        <tspan x="15" dy="1.2em">kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Q</tspan>
    </text>

    <text x="15" y="55" class="terminal-text text-2">
        <tspan x="15" dy="1.2em">pQz^tY)cQd9!kR(wI^e@pQd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X</tspan>
        <tspan x="15" dy="1.2em">fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)cQd9!kR</tspan>
        <tspan x="15" dy="1.2em">b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)c</tspan>
        <tspan x="15" dy="1.2em">jS)tXp%nVb^sU&amp;mI^e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u</tspan>
        <tspan x="15" dy="1.2em">sU&amp;mI^e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9</tspan>
        <tspan x="15" dy="1.2em">e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(</tspan>
        <tspan x="15" dy="1.2em">ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!j</tspan>
        <tspan x="15" dy="1.2em">lB7yC^e@jS)tXp%nVb^sU&amp;mI^e@jK)wD(oI#b8@L$fs(X^t!jo*</tspan>
        <tspan x="15" dy="1.2em">I^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!</tspan>
    </text>

    <text x="15" y="55" class="terminal-text text-3">
        <tspan x="15" dy="1.2em">V&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*Zp</tspan>
        <tspan x="15" dy="1.2em">g@Qd9!kR(wI^e@pQz^tY)cQd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(</tspan>
        <tspan x="15" dy="1.2em">b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)c</tspan>
        <tspan x="15" dy="1.2em">eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;</tspan>
        <tspan x="15" dy="1.2em">X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$f</tspan>
        <tspan x="15" dy="1.2em">fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)cQd9!kR</tspan>
        <tspan x="15" dy="1.2em">e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI</tspan>
        <tspan x="15" dy="1.2em">mI^e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR</tspan>
        <tspan x="15" dy="1.2em">D(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^</tspan>
    </text>

     <text x="15" y="55" class="terminal-text text-4">
        <tspan x="15" dy="1.2em">t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(</tspan>
        <tspan x="15" dy="1.2em">R(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!</tspan>
        <tspan x="15" dy="1.2em">nVb^sU&amp;mI^e@jK)wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@</tspan>
        <tspan x="15" dy="1.2em">tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz</tspan>
        <tspan x="15" dy="1.2em">yCg@Qd9!kR(wI^e@pQz^tY)cQd9!kR(wI^e@pQz^tY)ciH#b8@L$fs</tspan>
        <tspan x="15" dy="1.2em">L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)cQd9!</tspan>
        <tspan x="15" dy="1.2em">wD(oI#b8@L$fs(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^t</tspan>
        <tspan x="15" dy="1.2em">u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$fs(X^t!jo*ZpS%sV&amp;</tspan>
        <tspan x="15" dy="1.2em">s(X^t!jo*ZpS%sV&amp;u^eB5yCg@Qd9!kR(wI^e@pQz^tY)ciH#b8@L$</tspan>
    </text>
</svg>
