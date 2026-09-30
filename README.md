<!DOCTYPE html>
<html lang="th" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Learning - Interactive Master Web Platform</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0fdf4',
                            100: '#dcfce7',
                            500: '#22c55e',
                            600: '#16a34a',
                            700: '#15803d',
                            900: '#14532d',
                        }
                    }
                }
            }
        }
    </script>
    <!-- Chart.js CDN -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700;800&display=swap');
        body {
            font-family: 'Sarabun', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 340px;
            }
        }
        /* Custom Scrollbar for Chat */
        .chat-scroll::-webkit-scrollbar {
            width: 5px;
        }
        .chat-scroll::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
        .dark .chat-scroll::-webkit-scrollbar-thumb {
            background: #475569;
        }
    </style>
</head>
<body class="bg-slate-50 dark:bg-slate-950 text-slate-800 dark:text-slate-100 font-sans antialiased selection:bg-emerald-500 selection:text-white transition-colors duration-200">

    <header class="sticky top-0 z-40 bg-slate-900/95 dark:bg-slate-900/90 backdrop-blur-md text-white shadow-lg border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center h-auto md:h-16 py-3 md:py-0 gap-3 md:gap-0">
            <div class="flex items-center space-x-3">
                <span class="bg-emerald-500 text-slate-950 px-2.5 py-1 rounded-xl font-black text-sm tracking-wider shadow-sm">SL</span>
                <div>
                    <div class="flex items-center gap-2">
                        <h1 class="text-base font-bold leading-tight">Smart Learning</h1>
                        <span class="text-[10px] bg-indigo-600/80 text-indigo-100 px-2 py-0.5 rounded-full font-medium">v2.5 Live</span>
                    </div>
                    <p class="text-xs text-slate-400">Master Action Plan & Interactive Platform</p>
                </div>
            </div>

            <!-- User Gamification Snapshot & Theme Toggle -->
            <div class="flex items-center gap-3">
                <!-- Gamification Points Pill -->
                <div class="flex items-center bg-slate-800/90 dark:bg-slate-800 border border-slate-700 rounded-full px-3 py-1 gap-2 text-xs">
                    <span class="text-amber-400">⚡ <span id="user-points" class="font-bold">450</span> XP</span>
                    <span class="text-slate-500">|</span>
                    <span class="text-emerald-400 font-medium" id="user-level">Lv.3 Smart Learner</span>
                </div>

                <!-- Navigation Tabs -->
                <nav class="hidden lg:flex items-center gap-1 text-xs font-medium text-slate-300">
                    <button onclick="scrollToSection('summary')" class="px-2.5 py-1.5 rounded-md hover:bg-slate-800 hover:text-white transition">ภาพรวม</button>
                    <button onclick="scrollToSection('roadmap')" class="px-2.5 py-1.5 rounded-md hover:bg-slate-800 hover:text-white transition">แผนงาน</button>
                    <button onclick="scrollToSection('student-tracker')" class="px-2.5 py-1.5 rounded-md hover:bg-slate-800 hover:text-white transition">ติดตามงานกลุ่ม</button>
                    <button onclick="scrollToSection('gamification')" class="px-2.5 py-1.5 rounded-md hover:bg-slate-800 hover:text-white transition">ภารกิจ & ตรา</button>
                    <button onclick="scrollToSection('kpis')" class="px-2.5 py-1.5 rounded-md hover:bg-slate-800 hover:text-white transition">แดชบอร์ด KPIs</button>
                    <button onclick="scrollToSection('calculator')" class="px-2.5 py-1.5 rounded-md bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-bold transition">คำนวณเวลาครู</button>
                </nav>

                <!-- Dark Mode Toggle Button -->
                <button id="theme-toggle" onclick="toggleDarkMode()" aria-label="Toggle Dark Mode" class="p-2 rounded-xl bg-slate-800 hover:bg-slate-70
