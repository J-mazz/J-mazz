<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>/dev/urandom</title>
    <link href="https://fonts.googleapis.comcom/css2?family=VT323&display=swap" rel="stylesheet">
</head>
<body style="font-family: 'VT323', monospace; background-color: #0d1117; color: #c9d1d9; overflow: hidden; cursor: none; display: flex; align-items: center; justify-content: center; height: 100vh; margin: 0; padding: 1rem;">

    <div style="width: 100%; max-width: 56rem; height: 80vh; display: flex; flex-direction: column; border: 1px solid #30363d; border-radius: 6px; box-shadow: 0 8px 24px rgba(0,0,0,0.4);">
        <!-- Terminal Header -->
        <div style="background-color: #161b22; border-bottom: 1px solid #30363d; height: 28px; display: flex; align-items: center; padding-left: 1rem; padding-right: 1rem;">
            <div style="display: flex; gap: 0.5rem;">
                <div style="width: 0.75rem; height: 0.75rem; background-color: #ef4444; border-radius: 9999px;"></div>
                <div style="width: 0.75rem; height: 0.75rem; background-color: #f59e0b; border-radius: 9999px;"></div>
                <div style="width: 0.75rem; height: 0.75rem; background-color: #10b981; border-radius: 9999px;"></div>
            </div>
            <div style="flex-grow: 1; text-align: center; font-size: 0.875rem; color: #9ca3af;">
                bash &mdash; /dev/urandom
            </div>
        </div>

        <!-- Terminal Body -->
        <div id="terminal" style="padding: 1rem; overflow: hidden; flex-grow: 1; background-color: #0d1117; border-bottom-left-radius: 6px; border-bottom-right-radius: 6px;">
            <div id="urandom-output" style="white-space: pre-wrap; word-break: break-all; line-height: 1.2; font-size: 1.1rem; color: #58a6ff;"></div>
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

            if (totalChars > 0) {
                output.textContent = generateRandomChars(totalChars);
            }
        }

        // Initial fill
        fillScreen();

        // Continuously update a part of the screen to create a dynamic effect
        setInterval(() => {
            const currentContent = output.textContent;
            const newChars = generateRandomChars(250); // Add a smaller chunk for performance
            const startIndex = Math.floor(Math.random() * (currentContent.length - newChars.length));
            
            // Replace a random chunk of text
            if (startIndex >= 0 && currentContent.length > newChars.length) {
                 output.textContent = currentContent.substring(0, startIndex) + newChars + currentContent.substring(startIndex + newChars.length);
            }
           
        }, 50); // Update every 50ms for a smooth animation

        // Adjust on window resize
        window.addEventListener('resize', fillScreen);
    </script>
</body>
</html>

