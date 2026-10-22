`html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Qanday qilib buyurtmani tekshirib olish mumkin? | Uzum Qo'llanma</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        uzum: {
                            DEFAULT: '#7000FF',
                            hover: '#5A00CC',
                            light: '#F3E8FF',
                            dark: '#400099',
                            bg: '#F5F5F7',
                        }
                    },
                    keyframes: {
                        pulseGlow: {
                            '0%, 100%': { boxShadow: '0 0 15px rgba(112, 0, 255, 0.35)' },
                            '50%': { boxShadow: '0 0 28px rgba(112, 0, 255, 0.75)' },
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-8px)' },
                        },
                        scanLine: {
                            '0%': { top: '5%' },
                            '100%': { top: '90%' }
                        },
                        shimmer: {
                            '100%': { transform: 'translateX(100%)' }
                        },
                        popIn: {
                            '0%': { transform: 'scale(0.85)', opacity: '0' },
                            '100%': { transform: 'scale(1)', opacity: '1' }
                        }
                    },
                    animation: {
                        'pulse-glow': 'pulseGlow 2.5s infinite ease-in-out',
                        'float': 'float 3.5s infinite ease-in-out',
                        'scan': 'scanLine 2s infinite alternate ease-in-out',
                        'pop-in': 'popIn 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards'
                    }
                }
            }
        }
    </script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #F4F4F7;
            color: #0F172A;
            -webkit-tap-highlight-color: transparent;
        }

        /* Scroll Animation Reveal Class */
        .reveal {
            opacity: 0;
            transform: translateY(28px);
            transition: all 0.6s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Custom Shimmer Effect */
        .shimmer-box {
            position: relative;
            overflow: hidden;
        }
        .shimmer-box::after {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            transform: translateX(-100%);
            background-image: linear-gradient(
                90deg,
                rgba(255, 255, 255, 0) 0,
                rgba(255, 255, 255, 0.25) 20%,
                rgba(255, 255, 255, 0.5) 60%,
                rgba(255, 255, 255, 0)
            );
            animation: shimmer 3s infinite;
            content: '';
        }

        /* Custom Checkbox Animation */
        .check-item input:checked + div {
            background-color: #7000FF;
            border-color: #7000FF;
            color: white;
        }

        ::-webkit-scrollbar {
            width: 6px;}
        ::-webkit-scrollbar-track {
            background: #F1F1F5;
        }
        ::-webkit-scrollbar-thumb {
            background: #7000FF;
            border-radius: 4px;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center justify-start pb-20 pt-4 px-3 sm:px-4">

    <!-- MAIN WRAPPER -->
    <div class="w-full max-w-md mx-auto space-y-5">

        <!-- HEADER SECTION -->
        <header class="bg-gradient-to-br from-[#7000FF] via-[#851DFF] to-[#4A00B3] text-white rounded-3xl p-6 shadow-2xl relative overflow-hidden reveal active">
            <!-- Glow Accents -->
            <div class="absolute -right-8 -bottom-8 w-40 h-40 bg-purple-400/20 rounded-full blur-2xl pointer-events-none"></div>
            <div class="absolute -left-8 -top-8 w-32 h-32 bg-white/10 rounded-full blur-xl pointer-events-none"></div>

            <div class="relative z-10 flex flex-col items-center text-center">
                <!-- Floating Icon Badge -->
                <div class="w-16 h-16 bg-white/15 backdrop-blur-md rounded-2xl flex items-center justify-center mb-3.5 shadow-lg border border-white/20 animate-float">
                    <i data-lucide="package-search" class="w-9 h-9 text-white"></i>
                </div>
                
                <span class="bg-white/20 text-white text-[11px] font-bold px-3.5 py-1 rounded-full uppercase tracking-wider mb-2 backdrop-blur-md border border-white/20">
                    Uzum Market Qo'llanmasi
                </span>

                <h1 class="text-2xl font-extrabold leading-tight tracking-tight">
                    Qanday qilib buyurtmani tekshirib olish mumkin?
                </h1>

                <p class="text-xs text-purple-100 mt-2 max-w-xs leading-relaxed opacity-90">
                    Buyurtma holatini ko'rish, QR-kodni operatorga ko'rsatish va topshirish punktida (PVZ) to'g'ri qabul qilish bo'yicha ko'rgazmali yo'riqnoma.
                </p>
            </div>
        </header>

        <!-- INTERACTIVE PROGRESS STEPS -->
        <div class="bg-white rounded-2xl p-3.5 shadow-sm border border-gray-100 flex justify-between items-center px-5 reveal">
            <a href="#step-1" class="flex flex-col items-center group cursor-pointer">
                <span class="w-9 h-9 rounded-full bg-uzum text-white font-extrabold text-xs flex items-center justify-center shadow-md shadow-uzum/30 group-hover:scale-110 transition-transform">1</span>
                <span class="text-[11px] font-bold text-gray-700 mt-1.5">Profil</span>
            </a>
            <div class="h-[2px] flex-1 bg-purple-200 mx-2 -mt-4"></div>
            <a href="#step-2" class="flex flex-col items-center group cursor-pointer">
                <span class="w-9 h-9 rounded-full bg-uzum text-white font-extrabold text-xs flex items-center justify-center shadow-md shadow-uzum/30 group-hover:scale-110 transition-transform">2</span>
                <span class="text-[11px] font-bold text-gray-700 mt-1.5">Buyurtmalar</span>
            </a>
            <div class="h-[2px] flex-1 bg-purple-200 mx-2 -mt-4"></div>
            <a href="#step-3" class="flex flex-col items-center group cursor-pointer">
                <span class="w-9 h-9 rounded-full bg-uzum text-white font-extrabold text-xs flex items-center justify-center shadow-md shadow-uzum/30 group-hover:scale-110 transition-transform">3</span>
                <span class="text-[11px] font-bold text-gray-700 mt-1.5">QR-Kodi</span>
            </a>
        </div>

        <!-- STEP 1: PROFILGA KIRISH -->
        <section id="step-1" class="bg-white rounded-3xl p-5 shadow-sm border border-gray-100 space-y-4 reveal">
            <div class="flex items-center gap-3">
                <span class="w-8 h-8 bg-purple-100 text-uzum rounded-full font-extrabold text-xs flex items-center justify-center">1</span><div>
                    <h2 class="font-bold text-gray-900 text-base leading-tight">Profil bo'limiga kiring</h2>
                    <span class="text-[11px] text-gray-400">Birinchi bosqich</span>
                </div>
            </div>
            
            <p class="text-xs text-gray-600 leading-relaxed">
                Uzum Market ilovasida pastki o'ng burchakda joylashgan <b>"Profil"</b> tugmasini bosing va o'zingizning profilinigizga kiring.
            </p>

            <!-- Mock Profile Screen -->
            <div class="bg-gray-50 border border-gray-200 rounded-2xl p-4 space-y-3 transition-all">
                <!-- User Profile Banner -->
                <div class="bg-gradient-to-r from-uzum to-purple-600 text-white rounded-xl p-4 flex items-center gap-3 shadow-md shimmer-box">
                    <div class="w-12 h-12 bg-white/20 rounded-full flex items-center justify-center font-bold text-lg border border-white/30 backdrop-blur-xs">
                        👤
                    </div>
                    <div>
                        <div class="font-extrabold text-base tracking-wide">UZUM MARKET</div>
                        <div class="text-xs text-purple-200 font-mono tracking-widest mt-0.5">+998  *  </div>
                    </div>
                </div>

                <!-- Active Order Banner -->
                <div class="bg-white border border-gray-200 rounded-xl p-3 flex justify-between items-center shadow-2xs">
                    <div class="space-y-1">
                        <div class="text-[11px] font-bold text-gray-800">Buyurtma №13652345-0053</div>
                        <span class="inline-block px-2 py-0.5 bg-emerald-100 text-emerald-800 font-extrabold text-[10px] rounded-md">
                            YETKAZIB BERILYAPTI
                        </span>
                    </div>
                    <!-- Purple Styled Box Icon -->
                    <div class="w-11 h-11 bg-gradient-to-br from-uzum to-purple-900 rounded-xl flex items-center justify-center shadow-sm text-lg">
                        📦
                    </div>
                </div>
            </div>
        </section>

        <!-- STEP 2: BUYURTMALARIM BO'LIMI -->
        <section id="step-2" class="bg-white rounded-3xl p-5 shadow-sm border border-gray-100 space-y-4 reveal">
            <div class="flex items-center gap-3">
                <span class="w-8 h-8 bg-purple-100 text-uzum rounded-full font-extrabold text-xs flex items-center justify-center">2</span>
                <div>
                    <h2 class="font-bold text-gray-900 text-base leading-tight">"Buyurtmalarim" bo'limini tanlang</h2>
                    <span class="text-[11px] text-gray-400">Ikkinchi bosqich</span>
                </div>
            </div>

            <p class="text-xs text-gray-600 leading-relaxed">
                Profil menyusi ro'yxatidan buyurtmalaringiz holatini ko'rish uchun <b>"Buyurtmalarim"</b> tugmasini tanlang.
            </p>

            <!-- Mock Menu Item with Animation -->
            <div class="space-y-2">
                <div class="p-3.5 bg-purple-50/70 border-2 border-uzum/40 rounded-2xl flex items-center justify-between cursor-pointer group hover:bg-purple-100/60 transition-all shadow-xs">
                    <div class="flex items-center gap-3">
                        <div class="w-9 h-9 rounded-xl bg-uzum text-white flex items-center justify-center shadow-sm">
                            <i data-lucide="shopping-bag" class="w-4 h-4"></i>
                        </div>
                        <div>
                            <span class="font-bold text-xs text-gray-900 block">Buyurtmalarim</span>
                            <span class="text-[10px] text-purple-700 font-medium">Barcha aktiv buyurtmalar</span>
                        </div>
                    </div>
                    <i data-lucide="chevron-right" class="w-5 h-5 text-uzum group-hover:translate-x-1.5 transition-transform"></i>
                </div><div class="p-3 bg-white border border-gray-100 rounded-2xl flex items-center justify-between opacity-50">
                    <div class="flex items-center gap-3">
                        <div class="w-8 h-8 rounded-lg bg-gray-100 text-gray-500 flex items-center justify-center">
                            <i data-lucide="globe" class="w-4 h-4"></i>
                        </div>
                        <span class="text-xs text-gray-700 font-medium">Xorijdan buyurtmalarim</span>
                    </div>
                    <i data-lucide="chevron-right" class="w-4 h-4 text-gray-400"></i>
                </div>
            </div>
        </section>

        <!-- STEP 3: BUYURTMA KODI VA MANZIL -->
        <section id="step-3" class="bg-white rounded-3xl p-5 shadow-sm border border-gray-100 space-y-4 reveal">
            <div class="flex items-center gap-3">
                <span class="w-8 h-8 bg-purple-100 text-uzum rounded-full font-extrabold text-xs flex items-center justify-center">3</span>
                <div>
                    <h2 class="font-bold text-gray-900 text-base leading-tight">Buyurtma kodini va manzilni ko'ring</h2>
                    <span class="text-[11px] text-gray-400">Uchinchi bosqich</span>
                </div>
            </div>

            <p class="text-xs text-gray-600 leading-relaxed">
                <b>"Faollar"</b> oynasida tayyor bo'lgan buyurtmangizni tanlang va topshirish punktida (PVZ) ko'rsatish uchun binafsha rangli tugmani bosing.
            </p>

            <!-- Mock Card Preview -->
            <div class="bg-gray-50 border border-gray-200 rounded-2xl p-4 space-y-3.5 relative overflow-hidden">
                <div class="flex justify-between items-start">
                    <div>
                        <span class="inline-block px-2.5 py-1 bg-emerald-100 text-emerald-800 text-[10px] font-extrabold rounded-md uppercase tracking-wider mb-1">
                            OLIB KETISH MUMKIN
                        </span>
                        <div class="font-extrabold text-sm text-gray-900">Buyurtma №13652345-0052</div>
                        <div class="text-[11px] text-uzum font-semibold mt-0.5">27-Oktyabrgacha saqlaymiz</div>
                    </div>
                </div>

                <!-- Purple Box Container -->
                <div class="bg-white p-3 rounded-xl border border-gray-100 flex items-center gap-3 shadow-2xs">
                    <div class="w-14 h-14 bg-gradient-to-br from-uzum via-purple-600 to-indigo-900 rounded-xl flex items-center justify-center text-2xl shadow-md text-white animate-pulse-glow">
                        📦
                    </div>
                    <div>
                        <div class="font-extrabold text-xs text-gray-900">4 ta tovar</div>
                        <div class="text-xs text-amber-600 font-bold mt-0.5">To'lash uchun: 171 600 so'm</div>
                    </div>
                </div>

                <!-- Pulse Action Button -->
                <button onclick="openModal()" class="w-full bg-uzum hover:bg-uzum-hover active:scale-98 transition-all text-white font-bold py-3.5 px-4 rounded-xl shadow-lg shadow-uzum/30 flex items-center justify-center gap-2 text-xs sm:text-sm animate-pulse-glow">
                    <i data-lucide="qr-code" class="w-5 h-5"></i>
                    <span>Buyurtmani olish (QR-kod)</span>
                </button>
            </div>
        </section>

        <!-- CHECKLIST & TIPS SECTION -->
        <section class="bg-white rounded-3xl p-5 shadow-sm border border-gray-100 space-y-4 reveal">
            <div class="flex items-center gap-2.5 text-uzum font-bold text-sm">
                <i data-lucide="check-circle-2" class="w-5 h-5"></i>
                <span>Topshirish punktidagi (PVZ) eslatmalar:</span>
            </div><!-- Interactive Checklist -->
            <div class="space-y-2.5">
                <label class="check-item flex items-start gap-3 p-3 bg-purple-50/50 rounded-xl border border-purple-100/80 cursor-pointer hover:bg-purple-100/50 transition-colors">
                    <input type="checkbox" checked class="hidden">
                    <div class="w-5 h-5 rounded-md border-2 border-purple-300 flex items-center justify-center shrink-0 mt-0.5 transition-colors">
                        <i data-lucide="check" class="w-3.5 h-3.5"></i>
                    </div>
                    <span class="text-xs text-gray-700 leading-relaxed font-medium">
                        Kassa operatoriga kodingizni yoki buyurtma raqamini ko'rsating.
                    </span>
                </label>

                <label class="check-item flex items-start gap-3 p-3 bg-purple-50/50 rounded-xl border border-purple-100/80 cursor-pointer hover:bg-purple-100/50 transition-colors">
                    <input type="checkbox" checked class="hidden">
                    <div class="w-5 h-5 rounded-md border-2 border-purple-300 flex items-center justify-center shrink-0 mt-0.5 transition-colors">
                        <i data-lucide="check" class="w-3.5 h-3.5"></i>
                    </div>
                    <span class="text-xs text-gray-700 leading-relaxed font-medium">
                        Mahsulotni operator qarshisida ochib, butunligini tekshiring.
                    </span>
                </label>

                <label class="check-item flex items-start gap-3 p-3 bg-purple-50/50 rounded-xl border border-purple-100/80 cursor-pointer hover:bg-purple-100/50 transition-colors">
                    <input type="checkbox" checked class="hidden">
                    <div class="w-5 h-5 rounded-md border-2 border-purple-300 flex items-center justify-center shrink-0 mt-0.5 transition-colors">
                        <i data-lucide="check" class="w-3.5 h-3.5"></i>
                    </div>
                    <span class="text-xs text-gray-700 leading-relaxed font-medium">
                        Kamchilik yoki shikastlanish bo'lsa, joyida bepul qaytarishingiz mumkin.
                    </span>
                </label>
            </div>
        </section>

        <!-- FOOTER -->
        <footer class="text-center text-xs text-gray-400 pt-3 pb-2 space-y-1">
            <p>© 2026 Uzum Market Qo'llanmasi</p>
            <p class="text-[10px] text-gray-400">Barcha ma'lumotlar foydalanuvchilar uchun qulaylik maqsadida tayyorlandi</p>
        </footer>

    </div>

    <!-- QR & BARCODE MODAL -->
    <div id="qrModal" class="fixed inset-0 bg-black/60 backdrop-blur-xs z-50 flex items-center justify-center p-4 opacity-0 pointer-events-none transition-opacity duration-300">
        <div id="modalContent" class="bg-white w-full max-w-xs rounded-3xl p-6 text-center shadow-2xl transform scale-90 transition-transform duration-300 space-y-4 relative border border-purple-100">
            
            <button onclick="closeModal()" class="absolute top-4 right-4 w-8 h-8 bg-gray-100 hover:bg-gray-200 rounded-full flex items-center justify-center text-gray-600 transition-colors">
                ✕
            </button>

            <div class="inline-block p-2.5 bg-purple-100 text-uzum rounded-2xl">
                <i data-lucide="scan-line" class="w-7 h-7"></i>
            </div>

            <div>
                <h3 class="font-extrabold text-gray-900 text-base">Olib ketish kodi</h3>
                <p class="text-xs text-gray-500 mt-0.5">Ushbu kodni kassa operatoriga ko'rsating</p>
            </div>

            <!-- Simulated Barcode Box with Scanning Laser -->
            <div class="bg-gray-50 border border-gray-200 rounded-2xl p-4 flex flex-col items-center justify-center relative overflow-hidden">
                <!-- Laser Scanner Line -->
                <div class="absolute inset-x-0 h-0.5 bg-uzum shadow-[0_0_10px_#7000FF] animate-scan"></div><!-- Simulated Barcode Lines -->
                <div class="flex items-center justify-center gap-1.5 h-20 w-full px-2 mb-2">
                    <div class="w-1.5 h-full bg-gray-900 rounded-xs"></div>
                    <div class="w-0.5 h-full bg-gray-900"></div>
                    <div class="w-2 h-full bg-gray-900 rounded-xs"></div>
                    <div class="w-1 h-full bg-gray-900"></div>
                    <div class="w-3 h-full bg-gray-900 rounded-xs"></div>
                    <div class="w-0.5 h-full bg-gray-900"></div>
                    <div class="w-2 h-full bg-gray-900 rounded-xs"></div>
                    <div class="w-1.5 h-full bg-gray-900 rounded-xs"></div>
                    <div class="w-0.5 h-full bg-gray-900"></div>
                    <div class="w-2.5 h-full bg-gray-900 rounded-xs"></div>
                </div>
                <div class="font-mono text-sm font-extrabold tracking-widest text-gray-800">
                    № 13652345-0052
                </div>
            </div>

            <button onclick="closeModal()" class="w-full bg-uzum text-white font-bold py-3 rounded-xl text-xs hover:bg-uzum-hover transition-colors shadow-md">
                Tushunarli
            </button>
        </div>
    </div>

    <!-- FLOATING HELPER BUTTON -->
    <a href="#step-1" class="fixed bottom-4 right-4 bg-uzum text-white w-12 h-12 rounded-full flex items-center justify-center shadow-2xl border-2 border-white animate-float z-40">
        <i data-lucide="arrow-up" class="w-6 h-6"></i>
    </a>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Lucide Icons Render
        lucide.createIcons();

        // Reveal on scroll logic
        function revealOnScroll() {
            const reveals = document.querySelectorAll('.reveal');
            const windowHeight = window.innerHeight;

            reveals.forEach(el => {
                const elementTop = el.getBoundingClientRect().top;
                const elementVisible = 50;

                if (elementTop < windowHeight - elementVisible) {
                    el.classList.add('active');
                }
            });
        }

        window.addEventListener('scroll', revealOnScroll);
        window.addEventListener('load', revealOnScroll);

        // Modal Controls
        const modal = document.getElementById('qrModal');
        const modalContent = document.getElementById('modalContent');

        function openModal() {
            modal.classList.remove('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-90');
            modalContent.classList.add('scale-100');
        }

        function closeModal() {
            modal.classList.add('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-100');
            modalContent.classList.add('scale-90');
        }

        // Close when clicking overlay
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                closeModal();
            }
        });
    </script>
</body>
</html>
`
