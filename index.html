<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub API Link Converter</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom scrollbar for better aesthetics */
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #1f2937; }
        ::-webkit-scrollbar-thumb { background: #4b5563; border-radius: 4px; }
    </style>
</head>
<body class="bg-gray-900 text-gray-100 min-h-screen flex items-center justify-center p-4 antialiased">

    <div class="w-full max-w-md bg-gray-800 rounded-2xl shadow-xl border border-gray-700 p-6 sm:p-8">
        <!-- Header -->
        <div class="mb-6 text-center">
            <div class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-blue-900/50 text-blue-400 mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
                </svg>
            </div>
            <h1 class="text-2xl font-bold text-white tracking-tight">API Link Converter</h1>
            <p class="text-sm text-gray-400 mt-2">Convert GitHub workflow links to API dispatch URLs</p>
        </div>

        <!-- Input Section -->
        <div class="space-y-4">
            <div>
                <label for="inputUrl" class="block text-sm font-medium text-gray-300 mb-1">GitHub Workflow URL</label>
                <input type="text" id="inputUrl" placeholder="https://github.com/.../.github/workflows/file.yml" 
                    class="w-full px-4 py-3 bg-gray-900 border border-gray-700 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-white text-sm outline-none transition-all placeholder-gray-600"
                    autocomplete="off">
                <p id="errorText" class="text-red-400 text-xs mt-2 hidden">Invalid URL format. Make sure it points to a .github/workflows/.yml file.</p>
            </div>

            <button onclick="convertUrl()" 
                class="w-full bg-blue-600 hover:bg-blue-500 text-white font-medium py-3 px-4 rounded-lg transition-colors focus:ring-4 focus:ring-blue-900 focus:outline-none flex items-center justify-center">
                <span>Convert Link</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                </svg>
            </button>
        </div>

        <!-- Output Section (Hidden by default) -->
        <div id="resultBox" class="mt-6 hidden">
            <label class="block text-sm font-medium text-gray-300 mb-1">API Dispatch URL</label>
            <div class="relative">
                <input type="text" id="outputUrl" readonly 
                    class="w-full px-4 py-3 pr-24 bg-gray-900 border border-gray-700 rounded-lg text-green-400 text-sm outline-none">
                <button id="copyBtn" onclick="copyToClipboard()" 
                    class="absolute right-1 top-1 bottom-1 bg-gray-700 hover:bg-gray-600 text-white text-xs font-medium px-4 rounded-md transition-colors flex items-center">
                    Copy
                </button>
            </div>
        </div>
    </div>

    <script>
        function convertUrl() {
            const input = document.getElementById('inputUrl').value.trim();
            const resultBox = document.getElementById('resultBox');
            const outputUrl = document.getElementById('outputUrl');
            const errorText = document.getElementById('errorText');

            // Regex banaya gaya hai owner, repo aur filename extract karne ke liye
            const regex = /^https:\/\/github\.com\/([^\/]+)\/([^\/]+)\/blob\/[^\/]+\/\.github\/workflows\/([^\/]+\.yml)$/;
            const match = input.match(regex);

            if (match) {
                const owner = match[1];
                const repo = match[2];
                const file = match[3];
                
                // Naya API URL format generate karna
                const apiUrl = `https://api.github.com/repos/${owner}/${repo}/actions/workflows/${file}/dispatches`;

                outputUrl.value = apiUrl;
                resultBox.classList.remove('hidden');
                errorText.classList.add('hidden');
            } else {
                errorText.classList.remove('hidden');
                resultBox.classList.add('hidden');
            }
        }

        function copyToClipboard() {
            const outputUrl = document.getElementById('outputUrl');
            const copyBtn = document.getElementById('copyBtn');

            outputUrl.select();
            outputUrl.setSelectionRange(0, 99999); // Mobile devices ke liye
            navigator.clipboard.writeText(outputUrl.value).then(() => {
                copyBtn.innerText = 'Copied!';
                copyBtn.classList.replace('bg-gray-700', 'bg-green-600');
                copyBtn.classList.replace('hover:bg-gray-600', 'hover:bg-green-500');
                
                setTimeout(() => {
                    copyBtn.innerText = 'Copy';
                    copyBtn.classList.replace('bg-green-600', 'bg-gray-700');
                    copyBtn.classList.replace('hover:bg-green-500', 'hover:bg-gray-600');
                }, 2000);
            });
        }
    </script>
</body>
</html>
