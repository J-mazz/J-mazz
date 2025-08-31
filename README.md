 👋 Hi, I’m @J-mazz

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>/dev/urandom</title>
    <link href="https://fonts.googleapis.com/css2?family=VT323&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'VT323', monospace;
            background-color: #0d1117;
            color: #c9d1d9;
            overflow: hidden;
            cursor: none;
        }
        #urandom-output {
            white-space: pre-wrap;
            word-break: break-all;
            line-height: 1.2;
            font-size: 1.1rem;
            color: #58a6ff; /* A slightly brighter blue for the random characters */
        }
        .terminal-window {
            border: 1px solid #30363d;
            border-radius: 6px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.4);
        }
        .terminal-header {
            background-color: #161b22;
            border-bottom: 1px solid #30363d;
            height: 28px;
        }
    </style>
</head>
<body class="flex items-center justify-center h-screen m-0 p-4">

    <div class="terminal-window w-full max-w-4xl h-[80vh] flex flex-col">
        <!-- Terminal Header -->
        <div class="terminal-header flex items-center px-4">
            <div class="flex space-x-2">
                <div class="w-3 h-3 bg-red-500 rounded-full"></div>
                <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
                <div class="w-3 h-3 bg-green-500 rounded-full"></div>
            </div>
            <div class="flex-grow text-center text-sm text-gray-400">
                bash &mdash; /dev/urandom
            </div>
        </div>

        <!-- Terminal Body -->
        <div id="terminal" class="p-4 overflow-hidden flex-grow bg-[#0d1117] rounded-b-md">
            <div id="urandom-output"></div>
        </div>
    </div>

    <script>
        const output = document.getElementById('urandom-output');
        const terminal = document.getElementById('terminal');

        // Function to generate a chunk of random characters
        function generateRandomChars(length) {
            let result = '';
            const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()-=_+[]{}|;:,.<>/?`~';
            const charactersLength = characters.length;
            for (let i = 0; i < length; i++) {
                result += characters.charAt(Math.floor(Math.random() * charactersLength));
            }
            return result;
        }

        // Function to fill the screen with random characters
        function fillScreen() {
            // Estimate the number of characters needed to fill the container
            const charWidth = 8; // Approximate width of a character in pixels
            const charHeight = 16; // Approximate height of a character in pixels
            const containerWidth = terminal.clientWidth;
            const containerHeight = terminal.clientHeight;
            const charsPerLine = Math.floor(containerWidth / charWidth);
            const lines = Math.floor(containerHeight / charHeight);
            const totalChars = charsPerLine * lines * 1.5; // Fill a bit more to be safe

            output.textContent = generateRandomChars(totalChars);
        }

        // Initial fill
        fillScreen();

        // Continuously update a part of the screen to create a dynamic effect
        setInterval(() => {
            const currentContent = output.textContent;
            const newChars = generateRandomChars(250); // Add a smaller chunk for performance
            const startIndex = Math.floor(Math.random() * (currentContent.length - newChars.length));
            
            // Replace a random chunk of text
            if (startIndex >= 0) {
                 output.textContent = currentContent.substring(0, startIndex) + newChars + currentContent.substring(startIndex + newChars.length);
            }
           
        }, 50); // Update every 50ms for a smooth animation

        // Adjust on window resize
        window.addEventListener('resize', fillScreen);
    </script>
</body>
</html>


   


