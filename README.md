# Smart-learning-
<!DOCTYPE html>
<html lang="th" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduTransform Matrix | Smart Learning Architecture</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Sarabun', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            700: '#0369a1',
                            900: '#0c4a6e',
                        }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-900 dark:text-slate-100 transition-colors duration-300 font-sans antialiased">

    <!-- Top Navigation Bar -->
    <nav class="sticky top-0 z-50 backdrop-blur-md bg-white/80 dark:bg-slate-900/80 border-b border-slate-200 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center space-x-3">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-sky-500 to-indigo-600 flex items-center justify-center text-white font-bold text-xl shadow-md">
                        E
                    </div>
                    <div>
                        <span class="font-bold text-lg tracking-tight text-slate-900 dark:text-white">EduTransform</span>
                        <span class="text-xs bg-sky-100 dark:bg-sky-950 text-sky-600 dark:text-sky-400 font-semibold px-2 py-0.5 rounded-full ml-1">Matrix v2.6</span>
                    </div>
                </div>
                
                <div class="hidden md:flex items-center space-x-6 text-sm font-medium">
                    <a href="#overview" class="hover:text-sky-500 transition-colors">ภาพรวมระบบ</a>
                    <a href="#solutions" class="hover:text-sky-500 transition-colors">3 เสาหลัก</a>
                    <a href="#calculator" class="hover:text-sky-500 transition-colors">คำนวณเวลาครู</a>
                    <a href="#students" class="hover:text-sky-500 transition-colors">ผลทดสอบนักเรียน</a>
                </div>

                <div class="flex items-center space-x-3">
                    <button id="themeToggle" class="p-2.5 rounded-xl bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all">
                        <i id="themeIcon" class="fa-solid fa-moon"></i>
                    </button>
                    <a href="#pitch" class="bg-sky-600 hover:bg-sky-700 text-white font-medium px-4 py-2 rounded-xl shadow-sm text-sm transition-all flex items-center gap-2">
                        <i class="fa-solid fa-rocket text-xs"></i> Pitch Deck
                    </a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Main Container -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-12">

        <!-- Hero Section -->
        <section id="overview" class="relative overflow-hidden rounded-3xl bg-gradient-to-br from-slate-900 via-indigo-950 to-slate-900 text-white p-8 sm:p-12 shadow-2xl border border-slate-800">
            <div class="absolute -right-20 -top-20 w-96 h-96 bg-sky-500/10 rounded-full blur-3xl pointer-events-none"></div>
            <div class="relative z-10 max-w-3xl space-y-6">
                <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-sky-500/10 border border-sky-500/30 text-sky-300 text-xs font-semibold uppercase tracking-wider">
                    <i class="fa-solid fa-brain"></i> AI-Augmented Educational Architecture
                </div>
                <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight leading-tight">
                    ยกระดับ Active Learning <br>
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-sky-400 via-indigo-300 to-emerald-400">คืนเวลาให้ครู เพิ่มทักษะให้ผู้เรียน</span>
                </h1>
                <p class="text-slate-300 text-base sm:text-lg font-light leading-relaxed">
                    ระบบนิเวศการเรียนรู้สมาร์ทครบวงจร ผสานนวัตกรรม Socio-STEM และระบบประเมินผลอัตโนมัติ เพื่อการเรียนรู้แบบ Personalized ไร้ขีดจำกัด
                </p>
                <div class="pt-2 flex flex-wrap gap-4">
                    <a href="#calculator" class="bg-sky-500 hover:bg-sky-400 text-slate-950 font-semibold px-6 py-3 rounded-xl transition-all shadow-lg shadow-sky-500/25 flex items-center gap-2">
                        <i class="fa-solid fa-calculator"></i> คำนวณเวลาที่ประหยัดได้
                    </a>
                    <a href="#students" class="bg-slate-800/80 hover:bg-slate-700 text-slate-200 border border-slate-700 font-medium px-6 py-3 rounded-xl transition-all flex items-center gap-2">
                        <i class="fa-solid fa-vial"></i> ผลประเมิน ม.4
                    </a>
                </div>
            </div>
        </section>

        <!-- Metrics Overview Grid -->
        <section class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition-shadow">
                <div class="w-12 h-12 rounded-xl bg-emerald-100 dark:bg-emerald-950/60 text-emerald-600 dark:text-emerald-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-clock-rotate-left"></i>
                </div>
                <h3 class="text-2xl font-bold text-slate-900 dark:text-white">65%</h3>
                <p class="text-slate-500 dark:text-slate-400 text-sm mt-1">ลดเวลาเตรียมสอนและตรวจข้อสอบของครู</p>
            </div>
            <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition-shadow">
                <div class="w-12 h-12 rounded-xl bg-sky-100 dark:bg-sky-950/60 text-sky-600 dark:text-sky-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-chart-line"></i>
                </div>
                <h3 class="text-2xl font-bold text-slate-900 dark:text-white">2.5x</h3>
                <p class="text-slate-500 dark:text-slate-400 text-sm mt-1">การมีส่วนร่วมในชั้นเรียน (Active Engagement)</p>
            </div>
            <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition-shadow">
                <div class="w-12 h-12 rounded-xl bg-indigo-100 dark:bg-indigo-950/60 text-indigo-600 dark:text-indigo-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-user-check"></i>
                </div>
                <h3 class="text-2xl font-bold text-slate-900 dark:text-white">100%</h3>
                <p class="text-slate-500 dark:text-slate-400 text-sm mt-1">Personalized Path สำหรับนักเรียนทุกคน</p>
            </div>
        </section>

        <!-- Interactive Calculator & Chart Section -->
        <section id="calculator" class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-start">
            <!-- Left: Interactive Simulator -->
            <div class="p-6 sm:p-8 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm space-y-6">
                <div>
                    <h2 class="text-xl font-bold text-slate-900 dark:text-white flex items-center gap-2">
                        <i class="fa-solid fa-sliders text-sky-500"></i> ตัวคำนวณเวลาประหยัดสำหรับครู (Live)
                    </h2>
                    <p class="text-sm text-slate-500 dark:text-slate-400 mt-1">
                        ปรับสไลเดอร์เพื่อคำนวณเวลาที่ AI ช่วยลดภาระงานสอน
                    </p>
                </div>

                <div class="space-y-4">
                    <div>
                        <div class="flex justify-between text-sm font-medium mb-2">
                            <span>จำนวนห้องเรียนที่สอน:</span>
                            <span id="classesValue" class="text-sky-600 dark:text-sky-400 font-bold">5 ห้อง</span>
                        </div>
                        <input id="classesInput" type="range" min="1" max="10" value="5" class="w-full h-2 bg-slate-200 dark:bg-slate-700 rounded-lg appearance-none cursor-pointer accent-sky-500">
                    </div>

                    <div>
                        <div class="flex justify-between text-sm font-medium mb-2">
                            <span>ชั่วโมงเตรียมสอน/ตรวจงานต่อสัปดาห์:</span>
                            <span id="hoursValue" class="text-sky-600 dark:text-sky-400 font-bold">15 ชั่วโมง</span>
                        </div>
                        <input id="hoursInput" type="range" min="5" max="35" value="15" class="w-full h-2 bg-slate-200 dark:bg-slate-700 rounded-lg appearance-none cursor-pointer accent-sky-500">
                    </div>
                </div>

                <div class="p-4 rounded-xl bg-sky-50 dark:bg-sky-950/40 border border-sky-100 dark:border-sky-900 space-y-2">
                    <div class="text-xs text-sky-600 dark:text-sky-400 font-semibold uppercase tracking-wider">ประมาณการเวลาที่ประหยัดได้</div>
                    <div class="flex items-baseline gap-2">
                        <span id="savedHoursText" class="text-3xl font-extrabold text-sky-700 dark:text-sky-300">9.75</span>
                        <span class="text-sm text-slate-600 dark:text-slate-400 font-medium">ชั่วโมง / สัปดาห์</span>
                    </div>
                    <p class="text-xs text-slate-500 dark:text-slate-400">
                        คิดเป็น <span id="savedPercentText" class="font-bold text-emerald-600">65%</span> ของเวลาทำงานเอกสารและเตรียมการสอนเดิม
                    </p>
                </div>
            </div>

            <!-- Right: Dynamic Chart -->
            <div class="p-6 sm:p-8 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col justify-between h-full">
                <div>
                    <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-2">สัดส่วนการใช้เวลาของครูผู้สอน</h3>
                    <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">เปรียบเทียบระหว่างรูปแบบเดิม vs ระบบ Smart Learning</p>
                </div>
                <div class="relative w-full h-64">
                    <canvas id="timeComparisonChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Student Feedback Section (M.4 Male Testers) -->
        <section id="students" class="space-y-6">
            <div class="flex flex-col md:flex-row md:items-end justify-between gap-4">
                <div>
                    <h2 class="text-2xl font-bold text-slate-900 dark:text-white">ผลการทดสอบจริงจากนักเรียน (ชั้น ม.4)</h2>
                    <p class="text-sm text-slate-500 dark:text-slate-400">ข้อมูลจากกลุ่มตัวอย่างผู้ทดสอบชายทั้ง 3 สายการเรียน</p>
                </div>
                <span class="inline-flex items-center gap-2 text-xs font-semibold px-3 py-1.5 rounded-lg bg-emerald-100 dark:bg-emerald-950 text-emerald-700 dark:text-emerald-300 border border-emerald-200 dark:border-emerald-800">
                    <i class="fa-solid fa-check-double"></i> ผ่านการปรับปรุงตาม Feedback แล้ว
                </span>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Student 1 -->
                <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm space-y-4">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-700 flex items-center justify-center font-bold text-slate-700 dark:text-slate-200">
                            ม.4
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900 dark:text-white">ผู้ทดสอบคนที่ 1</h4>
                            <p class="text-xs text-slate-500 dark:text-slate-400">สายวิทยาศาสตร์-คณิตศาสตร์</p>
                        </div>
                    </div>

                    <div class="space-y-3 text-xs leading-relaxed text-slate-600 dark:text-slate-300">
                        <div>
                            <span class="font-semibold text-emerald-600 dark:text-emerald-400">สิ่งที่ทำได้ดี:</span>
                            ระบบคำนวณและแสดงกราฟพัฒนาการชัดเจน ทำให้ติดตามความก้าวหน้าในการเรียนวิชาคำนวณได้ทันที
                        </div>
                        <div>
                            <span class="font-semibold text-amber-600 dark:text-amber-400">ข้อเสนอแนะ:</span>
                            ควรอัปเดตข้อมูลโครงงานและภารกิจกลุ่มให้เป็นปัจจุบันแบบรายสัปดาห์
                        </div>
                        <div>
                            <span class="font-semibold text-sky-600 dark:text-sky-400">วิธีปรับปรุง:</span>
                            เพิ่มระบบการบันทึกความก้าวหน้างานกลุ่มอัตโนมัติพร้อมการแจ้งเตือน
                        </div>
                    </div>
                </div>

                <!-- Student 2 -->
                <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm space-y-4">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-700 flex items-center justify-center font-bold text-slate-700 dark:text-slate-200">
                            ม.4
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900 dark:text-white">ผู้ทดสอบคนที่ 2</h4>
                            <p class="text-xs text-slate-500 dark:text-slate-400">สายศิลป์-คำนวณ</p>
                        </div>
                    </div>

                    <div class="space-y-3 text-xs leading-relaxed text-slate-600 dark:text-slate-300">
                        <div>
                            <span class="font-semibold text-emerald-600 dark:text-emerald-400">สิ่งที่ทำได้ดี:</span>
                            หน้าตาโปรแกรมใช้งานง่าย สบายตา และมีโหมดมืดที่ช่วยลดความล้าของสายตาเวลบทวนบทเรียนตอนกลางคืน
                        </div>
                        <div>
                            <span class="font-semibold text-amber-600 dark:text-amber-400">ข้อเสนอแนะ:</span>
                            อยากให้มีสวิตช์เปิดปิดโหมดมืดที่สังเกตเห็นได้ง่ายและใช้งานได้สะดวกในทุกหน้า
                        </div>
                        <div>
                            <span class="font-semibold text-sky-600 dark:text-sky-400">วิธีปรับปรุง:</span>
                            ติดตั้งปุ่มสลับธีมบนแถบเมนูด้านบนให้สามารถปรับได้ทันที
                        </div>
                    </div>
                </div>

                <!-- Student 3 -->
                <div class="p-6 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm space-y-4">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-slate-100 dark:bg-slate-700 flex items-center justify-center font-bold text-slate-700 dark:text-slate-200">
                            ม.4
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900 dark:text-white">ผู้ทดสอบคนที่ 3</h4>
                            <p class="text-xs text-slate-500 dark:text-slate-400">สายศิลป์-ภาษา</p>
                        </div>
                    </div>

                    <div class="space-y-3 text-xs leading-relaxed text-slate-600 dark:text-slate-300">
                        <div>
                            <span class="font-semibold text-emerald-600 dark:text-emerald-400">สิ่งที่ทำได้ดี:</span>
                            มีผู้ช่วยตอบคำถามที่ตอบได้รวดเร็ว ช่วยให้ทบทวนบทเรียนด้วยตัวเองได้สะดวก
                        </div>
                        <div>
                            <span class="font-semibold text-amber-600 dark:text-amber-400">ข้อเสนอแนะ:</span>
                            ควรมีระบบสร้างแรงจูงใจและสรุปคำถามที่พบบ่อยเพิ่มเติม
                        </div>
                        <div>
                            <span class="font-semibold text-sky-600 dark:text-sky-400">วิธีปรับปรุง:</span>
                            เพิ่มระบบสะสมคะแนนภารกิจพร้อมกล่องผู้ช่วยถามตอบแบบด่วน
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Final Optimization Summary Section -->
        <section class="p-6 sm:p-8 rounded-2xl bg-gradient-to-r from-sky-900 via-indigo-900 to-slate-900 text-white shadow-xl">
            <h3 class="text-lg font-bold mb-2 flex items-center gap-2">
                <i class="fa-solid fa-wand-magic-sparkles text-sky-400"></i>
                สรุปการปรับปรุงระบบรอบสุดท้ายก่อนนำเสนอ
            </h3>
            <p class="text-slate-300 text-sm leading-relaxed">
                การปรับปรุงระบบ Smart Learning รอบสุดท้ายได้เพิ่มแดชบอร์ดติดตามงานกลุ่มและโครงงาน SMT รายสัปดาห์ พร้อมติดตั้งสวิตช์โหมดมืดถนอมสายตาและกล่องแชต AI Study Buddy ช่วยตอบข้อสงสัยตลอด 24 ชั่วโมง รวมถึงเพิ่มระบบสะสมแต้มภารกิจรายวันและตราความสำเร็จเพื่อสร้างแรงจูงใจในการเรียนรู้ ซึ่งแก้ไขปัญหาได้ตรงตามข้อเสนอแนะของผู้ทดสอบทุกคนเรียบร้อยครับ
            </p>
        </section>

    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 mt-12 py-8">
        <div class="max-w-7xl mx-auto px-4 text-center text-xs text-slate-500 dark:text-slate-400 space-y-2">
            <p>© 2026 EduTransform Matrix. All rights reserved.</p>
            <p>Designed for Smart Educational Framework Project Pitching</p>
        </div>
    </footer>

    <!-- Interactive Script -->
    <script>
        // Theme Toggle Logic
        const themeToggleBtn = document.getElementById('themeToggle');
        const themeIcon = document.getElementById('themeIcon');

        themeToggleBtn.addEventListener('click', () => {
            document.documentElement.classList.toggle('dark');
            if (document.documentElement.classList.contains('dark')) {
                themeIcon.className = 'fa-solid fa-sun text-amber-400';
            } else {
                themeIcon.className = 'fa-solid fa-moon';
            }
        });

        // Calculator Interactive Logic
        const classesInput = document.getElementById('classesInput');
        const hoursInput = document.getElementById('hoursInput');
        const classesValue = document.getElementById('classesValue');
        const hoursValue = document.getElementById('hoursValue');
        const savedHoursText = document.getElementById('savedHoursText');

        function updateCalculator() {
            const classes = parseInt(classesInput.value);
            const hours = parseInt(hoursInput.value);
            
            classesValue.textContent = classes + ' ห้อง';
            hoursValue.textContent = hours + ' ชั่วโมง';
            
            // Formula: Base 65% efficiency gain with scaling class factor
            const totalHours = hours * (classes / 5);
            const saved = (totalHours * 0.65).toFixed(1);
            
            savedHoursText.textContent = saved;
            
            // Dynamic Update Chart
            timeChart.data.datasets[0].data = [hours, Math.max(2, (hours * 0.35)).toFixed(1)];
            timeChart.update();
        }

        classesInput.addEventListener('input', updateCalculator);
        hoursInput.addEventListener('input', updateCalculator);

        // Chart.js Implementation
        const ctx = document.getElementById('timeComparisonChart').getContext('2d');
        const timeChart = new Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['แบบเดิม (Hours)', 'Smart Learning (Hours)'],
                datasets: [{
                    label: 'เวลาที่ใช้ต่อสัปดาห์',
                    data: [15, 5.25],
                    backgroundColor: [
                        'rgba(148, 163, 184, 0.6)',
                        'rgba(14, 165, 233, 0.8)'
                    ],
                    borderColor: [
                        'rgba(148, 163, 184, 1)',
                        'rgba(14, 165, 233, 1)'
                    ],
                    borderWidth: 1,
                    borderRadius: 8
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: false }
                },
                scales: {
                    y: {
                        beginAtZero: true,
                        grid: { color: 'rgba(148, 163, 184, 0.1)' }
                    },
                    x: {
                        grid: { display: false }
                    }
                }
            }
        });
    </script>
</body>
</html>
