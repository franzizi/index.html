<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ezekiel Franztio Jatiputra | Broadcast Multimedia & Audio Specialist</title>
    
    <!-- Google Fonts: Fredoka & Comic Neue -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Comic+Neue:ital,wght@0,400;0,700;1,700&family=Fredoka:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Fredoka', 'sans-serif'],
                        comic: ['"Comic Neue"', 'cursive'],
                    },
                    colors: {
                        peanuts: {
                            bg: '#fffdf5',
                            card: '#ffffff',
                            black: '#1a1a1a',
                            red: '#e63946',
                            yellow: '#ffd166',
                            blue: '#8ecae6',
                            green: '#06d6a0',
                            purple: '#c77dff',
                        }
                    },
                    boxShadow: {
                        'comic': '4px 4px 0px #1a1a1a',
                        'comic-lg': '6px 6px 0px #1a1a1a',
                        'comic-xl': '8px 8px 0px #1a1a1a',
                        'comic-sm': '2px 2px 0px #1a1a1a',
                    }
                }
            }
        }
    </script>

    <style>
        /* Comic Global Styling */
        body {
            background-color: #fffdf5;
            color: #1a1a1a;
            background-image: radial-gradient(#1a1a1a 0.75px, transparent 0.75px);
            background-size: 24px 24px;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #fffdf5;
            border-left: 3px solid #1a1a1a;
        }
        ::-webkit-scrollbar-thumb {
            background: #ffd166;
            border: 2px solid #1a1a1a;
            border-radius: 6px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #e63946;
        }

        /* Comic Card Styling */
        .comic-box {
            background-color: #ffffff;
            border: 3px solid #1a1a1a;
            box-shadow: 6px 6px 0px #1a1a1a;
            border-radius: 18px;
            transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
        }

        .comic-box:hover {
            transform: translate(-3px, -3px);
            box-shadow: 9px 9px 0px #1a1a1a;
        }

        .comic-box-sm {
            background-color: #ffffff;
            border: 3px solid #1a1a1a;
            box-shadow: 4px 4px 0px #1a1a1a;
            border-radius: 14px;
            transition: all 0.15s ease;
        }

        .comic-box-sm:hover {
            transform: translate(-2px, -2px);
            box-shadow: 6px 6px 0px #1a1a1a;
        }

        /* Comic Button Effects */
        .comic-btn {
            border: 3px solid #1a1a1a;
            box-shadow: 4px 4px 0px #1a1a1a;
            font-weight: 700;
            border-radius: 12px;
            transition: all 0.15s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .comic-btn:hover {
            transform: translate(-2px, -2px);
            box-shadow: 6px 6px 0px #1a1a1a;
        }

        .comic-btn:active {
            transform: translate(2px, 2px);
            box-shadow: 1px 1px 0px #1a1a1a;
        }

        /* Comic Speech Bubble Pointer */
        .speech-bubble {
            position: relative;
            background: #ffffff;
            border: 3px solid #1a1a1a;
            box-shadow: 4px 4px 0px #1a1a1a;
            border-radius: 16px;
        }

        .speech-bubble::after {
            content: '';
            position: absolute;
            bottom: -14px;
            left: 28px;
            border-width: 14px 14px 0 0;
            border-style: solid;
            border-color: #ffffff transparent;
            display: block;
            width: 0;
            filter: drop-shadow(2px 2px 0px #1a1a1a);
        }

        /* Charlie Brown Zigzag Banner */
        .zigzag-pattern {
            background: repeating-linear-gradient(
                -45deg,
                #ffd166,
                #ffd166 12px,
                #1a1a1a 12px,
                #1a1a1a 16px
            );
        }

        /* Float animation */
        @keyframes comicFloat {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-8px) rotate(1deg); }
        }
        .animate-comic-float {
            animation: comicFloat 3.5s ease-in-out infinite;
        }
        
        @keyframes tailWag {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(12deg); }
        }
        .animate-tail {
            transform-origin: bottom left;
            animation: tailWag 1.2s ease-in-out infinite;
        }
    </style>
</head>
<body class="selection:bg-peanuts-yellow selection:text-peanuts-black">

    <!-- Toast Notification (Comic Bubble Style) -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-32 opacity-0 transition-all duration-300 comic-box-sm bg-peanuts-yellow px-5 py-3.5 flex items-center gap-3 text-sm font-bold border-4 border-peanuts-black">
        <i class="fa-solid fa-bell text-peanuts-red text-lg animate-bounce"></i>
        <span id="toast-message">Email berhasil disalin! 🐾</span>
    </div>

    <!-- NAVBAR -->
    <header class="fixed top-0 left-0 w-full z-40 bg-peanuts-bg/95 border-b-4 border-peanuts-black backdrop-blur-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <!-- Logo with Snoopy Ear Icon -->
            <a href="#hero" class="flex items-center gap-3 group">
                <div class="w-11 h-11 rounded-xl bg-peanuts-red border-3 border-peanuts-black shadow-comic flex items-center justify-center text-white font-extrabold text-xl group-hover:rotate-6 transition-transform">
                    <i class="fa-solid fa-dog"></i>
                </div>
                <div class="flex flex-col">
                    <span class="font-bold text-peanuts-black tracking-wide text-lg leading-tight">Ezekiel Franztio</span>
                    <span class="text-xs font-comic font-bold text-peanuts-red uppercase tracking-wider">Broadcast & Media</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-6 text-sm font-bold">
                <a href="#about" class="px-3 py-1.5 rounded-lg hover:bg-peanuts-yellow border-2 border-transparent hover:border-peanuts-black transition-all">Profil</a>
                <a href="#skills" class="px-3 py-1.5 rounded-lg hover:bg-peanuts-blue border-2 border-transparent hover:border-peanuts-black transition-all">Kemampuan</a>
                <a href="#portfolio" class="px-3 py-1.5 rounded-lg hover:bg-peanuts-purple hover:text-white border-2 border-transparent hover:border-peanuts-black transition-all">Portofolio</a>
                <a href="#hobbies" class="px-3 py-1.5 rounded-lg hover:bg-peanuts-green border-2 border-transparent hover:border-peanuts-black transition-all">Hobi</a>
                <a href="#contact" class="px-3 py-1.5 rounded-lg hover:bg-peanuts-red hover:text-white border-2 border-transparent hover:border-peanuts-black transition-all">Kontak</a>
            </nav>

            <!-- CTA Right Header -->
            <div class="hidden md:flex items-center gap-3">
                <a href="#contact" class="comic-btn bg-peanuts-yellow hover:bg-yellow-300 text-peanuts-black px-4 py-2 text-xs uppercase tracking-wide">
                    <i class="fa-solid fa-comment-dots"></i> Hubungi Saya
                </a>
            </div>

            <!-- Mobile Hamburger Button -->
            <button id="mobile-menu-btn" class="md:hidden p-2 rounded-xl border-3 border-peanuts-black bg-peanuts-yellow shadow-comic focus:outline-none" aria-label="Toggle Menu">
                <i class="fa-solid fa-bars text-xl text-peanuts-black" id="menu-icon"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden border-t-4 border-peanuts-black bg-peanuts-bg px-6 py-6 space-y-3 font-bold">
            <a href="#about" class="mobile-link block p-3 rounded-xl bg-white border-2 border-peanuts-black shadow-comic-sm">Profil</a>
            <a href="#skills" class="mobile-link block p-3 rounded-xl bg-peanuts-blue border-2 border-peanuts-black shadow-comic-sm">Kemampuan</a>
            <a href="#portfolio" class="mobile-link block p-3 rounded-xl bg-peanuts-purple text-white border-2 border-peanuts-black shadow-comic-sm">Portofolio</a>
            <a href="#hobbies" class="mobile-link block p-3 rounded-xl bg-peanuts-green border-2 border-peanuts-black shadow-comic-sm">Hobi</a>
            <a href="#contact" class="mobile-link block p-3 rounded-xl bg-peanuts-red text-white border-2 border-peanuts-black shadow-comic-sm">Kontak</a>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="hero" class="pt-32 pb-16 md:pt-40 md:pb-28 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
            
            <!-- Hero Left Content -->
            <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                
                <!-- Speech Bubble Status -->
                <div class="inline-block relative">
                    <div class="speech-bubble px-4 py-2 text-xs sm:text-sm font-bold font-comic flex items-center gap-2 text-peanuts-black">
                        <span class="w-3 h-3 rounded-full bg-peanuts-red animate-ping"></span>
                        <i class="fa-solid fa-broadcast-tower text-peanuts-red"></i>
                        <span>🔴 LIVE IN THE STUDIO! Welcome to Snoopy's Desk!</span>
                    </div>
                </div>

                <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-peanuts-black leading-tight">
                    Halo, Saya <br/>
                    <span class="relative inline-block bg-peanuts-yellow px-4 py-1 mt-1 rounded-2xl border-4 border-peanuts-black shadow-comic transform -rotate-1">
                        Ezekiel Franztio Jatiputra
                    </span>
                </h1>

                <!-- Subtitle Tagline -->
                <p class="text-xl font-bold font-comic text-peanuts-red tracking-wide">
                    Broadcast Multimedia Student • Audio & Live Switcher Specialist
                </p>

                <p class="text-slate-800 text-base sm:text-lg font-medium leading-relaxed max-w-2xl mx-auto lg:mx-0">
                    Berfokus pada tata kelola produksi siaran studio, sound engineering (Midas M32), live streaming multi-kamera (vMix), serta perancangan visual UI/UX web komersial.
                </p>

                <!-- Action Buttons -->
                <div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 pt-3">
                    <a href="#portfolio" class="comic-btn bg-peanuts-red hover:bg-red-600 text-white px-7 py-3.5 text-base">
                        <i class="fa-solid fa-wand-magic-sparkles"></i> Lihat Portofolio
                    </a>
                    <a href="#contact" class="comic-btn bg-peanuts-blue hover:bg-blue-300 text-peanuts-black px-7 py-3.5 text-base">
                        <i class="fa-solid fa-envelope"></i> Hubungi Kontak
                    </a>
                </div>

                <!-- Comic Quick Info Badges -->
                <div class="grid grid-cols-3 gap-3 pt-6 max-w-md mx-auto lg:mx-0">
                    <div class="comic-box-sm bg-white p-3 text-center">
                        <div class="text-2xl font-extrabold text-peanuts-red">15+</div>
                        <div class="text-xs font-bold text-slate-700">Live Shows</div>
                    </div>
                    <div class="comic-box-sm bg-peanuts-yellow p-3 text-center">
                        <div class="text-2xl font-extrabold text-peanuts-black">100%</div>
                        <div class="text-xs font-bold text-slate-800">Audio Clarity</div>
                    </div>
                    <div class="comic-box-sm bg-peanuts-blue p-3 text-center">
                        <div class="text-2xl font-extrabold text-peanuts-black">Temanggung</div>
                        <div class="text-xs font-bold text-slate-800">Base Location</div>
                    </div>
                </div>

            </div>

            <!-- Hero Right Snoopy & Woodstock Wagon SVG Illustration -->
            <div class="lg:col-span-5 flex justify-center">
                <div class="comic-box bg-white p-6 w-full max-w-md text-center relative overflow-hidden animate-comic-float">
                    
                    <!-- Comic Title Strip -->
                    <div class="bg-peanuts-black text-peanuts-yellow font-comic font-bold text-xs py-1.5 px-4 rounded-lg uppercase tracking-widest mb-4 inline-block shadow-sm">
                        PEANUTS STUDIO BROADCAST // PANEL #1
                    </div>

                    <!-- Custom SVG: Snoopy Pulling Woodstock in Red Wagon -->
                    <div class="relative w-full h-64 flex items-center justify-center my-2">
                        <svg class="w-full h-full max-h-60" viewBox="0 0 400 300" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <!-- Background Sun/Circle -->
                            <circle cx="200" cy="140" r="90" fill="#FFEAA7" stroke="#1A1A1A" stroke-width="4"/>
                            
                            <!-- Floating Sound & Camera Notes -->
                            <path d="M70 70 Q75 50 90 60 Q100 70 80 85 Z" fill="#FFD166" stroke="#1A1A1A" stroke-width="3"/>
                            <text x="75" y="75" font-family="Fredoka" font-size="16" font-weight="bold" fill="#1A1A1A">🎵</text>
                            <text x="310" y="80" font-family="Fredoka" font-size="20" font-weight="bold" fill="#1A1A1A">🎥</text>
                            
                            <!-- Ground Line -->
                            <line x1="20" y1="240" x2="380" y2="240" stroke="#1A1A1A" stroke-width="5" stroke-linecap="round"/>
                            <line x1="40" y1="248" x2="360" y2="248" stroke="#1A1A1A" stroke-width="3" stroke-linecap="round" stroke-dasharray="8 8"/>

                            <!-- RED WAGON (Peanuts Classic Toy Wagon) -->
                            <g id="red-wagon">
                                <!-- Wagon Box Body -->
                                <path d="M60 170 L150 170 L145 210 L65 210 Z" fill="#E63946" stroke="#1A1A1A" stroke-width="4" stroke-linejoin="round"/>
                                <rect x="55" y="165" width="100" height="10" rx="3" fill="#D62828" stroke="#1A1A1A" stroke-width="3"/>
                                <!-- Wagon Pull Handle Line -->
                                <line x1="145" y1="205" x2="220" y2="185" stroke="#1A1A1A" stroke-width="4" stroke-linecap="round"/>
                                <!-- Wagon Wheels -->
                                <circle cx="80" cy="220" r="14" fill="#1A1A1A"/>
                                <circle cx="80" cy="220" r="5" fill="#FFFFFF"/>
                                <circle cx="130" cy="220" r="14" fill="#1A1A1A"/>
                                <circle cx="130" cy="220" r="5" fill="#FFFFFF"/>
                            </g>

                            <!-- WOODSTOCK IN THE WAGON -->
                            <g id="woodstock">
                                <!-- Woodstock Body -->
                                <path d="M95 155 Q105 140 115 150 Q120 160 110 165 Z" fill="#FFD166" stroke="#1A1A1A" stroke-width="3"/>
                                <!-- Head & Tuft Hair -->
                                <circle cx="102" cy="138" r="10" fill="#FFD166" stroke="#1A1A1A" stroke-width="3"/>
                                <path d="M100 128 L96 120 M103 127 L102 118 M106 128 L108 120" stroke="#1A1A1A" stroke-width="3" stroke-linecap="round"/>
                                <!-- Eye & Beak -->
                                <circle cx="106" cy="136" r="1.5" fill="#1A1A1A"/>
                                <path d="M112 138 L120 140 L112 143 Z" fill="#FFD166" stroke="#1A1A1A" stroke-width="2"/>
                                <!-- Headphones on Woodstock -->
                                <path d="M93 135 C93 124 111 124 111 135" fill="none" stroke="#E63946" stroke-width="3"/>
                                <rect x="91" y="133" width="4" height="8" rx="2" fill="#1A1A1A"/>
                                <rect x="109" y="133" width="4" height="8" rx="2" fill="#1A1A1A"/>
                            </g>

                            <!-- SNOOPY WALKING / PULLING -->
                            <g id="snoopy">
                                <!-- Snoopy Body -->
                                <path d="M220 170 C210 190 230 225 255 225 C275 225 285 195 275 165 C260 155 235 155 220 170 Z" fill="#FFFFFF" stroke="#1A1A1A" stroke-width="4" stroke-linejoin="round"/>
                                
                                <!-- Snoopy Black Spot on Back -->
                                <path d="M230 185 Q235 175 245 185 Q240 195 230 185 Z" fill="#1A1A1A"/>

                                <!-- Snoopy Feet walking -->
                                <ellipse cx="235" cy="232" rx="14" ry="8" fill="#FFFFFF" stroke="#1A1A1A" stroke-width="4"/>
                                <ellipse cx="270" cy="232" rx="14" ry="8" fill="#FFFFFF" stroke="#1A1A1A" stroke-width="4"/>
                                <!-- Toe lines -->
                                <line x1="238" y1="228" x2="238" y2="236" stroke="#1A1A1A" stroke-width="2"/>
                                <line x1="273" y1="228" x2="273" y2="236" stroke="#1A1A1A" stroke-width="2"/>

                                <!-- Arms -->
                                <path d="M235 180 Q220 185 220 188" stroke="#1A1A1A" stroke-width="4" stroke-linecap="round"/>

                                <!-- Snoopy Neck & Collar -->
                                <rect x="235" y="152" width="22" height="6" rx="2" fill="#E63946" stroke="#1A1A1A" stroke-width="2"/>

                                <!-- Snoopy Head -->
                                <path d="M230 150 C220 135 225 105 260 105 C295 105 325 125 320 145 C315 160 280 162 250 158 Z" fill="#FFFFFF" stroke="#1A1A1A" stroke-width="4" stroke-linejoin="round"/>
                                
                                <!-- Nose -->
                                <ellipse cx="320" cy="132" rx="8" ry="7" fill="#1A1A1A"/>
                                <ellipse cx="318" cy="130" rx="2" ry="1.5" fill="#FFFFFF"/>

                                <!-- Snoopy Ear (Classic Droopy Black Ear) -->
                                <path d="M242 122 C232 125 220 145 228 165 C236 175 250 165 248 140 Z" fill="#1A1A1A" stroke="#1A1A1A" stroke-width="2"/>

                                <!-- Eye & Smile -->
                                <circle cx="278" cy="126" r="3" fill="#1A1A1A"/>
                                <path d="M280 140 Q292 148 302 138" stroke="#1A1A1A" stroke-width="3" fill="none" stroke-linecap="round"/>

                                <!-- Tail -->
                                <path d="M222 195 Q210 190 205 198" class="animate-tail" stroke="#1A1A1A" stroke-width="4" stroke-linecap="round"/>
                            </g>
                        </svg>
                    </div>

                    <!-- Caption Tag -->
                    <div class="bg-peanuts-yellow border-2 border-peanuts-black p-2.5 rounded-xl text-xs font-bold font-comic text-peanuts-black">
                        "Joe Cool Audio Engineer on his way to the Live Broadcast Studio!" 🎧
                    </div>

                </div>
            </div>

        </div>
    </section>

    <!-- PROFIL & PENJELASAN (ABOUT ME - COMIC PANELS) -->
    <section id="about" class="py-16 bg-white border-y-4 border-peanuts-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto space-y-2 mb-12">
                <span class="px-3 py-1 bg-peanuts-red text-white text-xs font-bold uppercase rounded-md border-2 border-peanuts-black shadow-comic-sm inline-block">PANEL STORY</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-peanuts-black">Tentang Profil Saya</h2>
                <p class="text-slate-700 font-comic font-bold text-base">Perjalanan teknis & kreatif Ezekiel di dunia siaran multimedia.</p>
            </div>

            <!-- Bento Comic Strip Panels -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                
                <!-- Panel 1: Audio Engineering Midas M32 -->
                <div class="comic-box p-6 bg-peanuts-bg md:col-span-2 flex flex-col justify-between space-y-4">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="w-10 h-10 rounded-xl bg-peanuts-yellow border-2 border-peanuts-black flex items-center justify-center text-peanuts-black text-xl font-bold shadow-comic-sm">
                                <i class="fa-solid fa-sliders"></i>
                            </span>
                            <span class="font-comic font-bold text-xs bg-peanuts-black text-white px-2.5 py-1 rounded">PANEL #1</span>
                        </div>
                        <h3 class="text-2xl font-extrabold text-peanuts-black">Audio Engineering & Midas M32 Master</h3>
                        <p class="text-slate-800 text-sm font-medium leading-relaxed">
                            Sebagai mahasiswa Broadcast Multimedia, fokus utama saya adalah mengelola tata suara siaran langsung (*live broadcast audio*) menggunakan konsol digital industri <strong class="text-peanuts-red">Midas M32 Live & Stage Box DL16/DL32</strong>. Berpengalaman mengatur signal routing, mikrofonisasi studio, gain staging, hingga sound monitoring tanpa *latency*.
                        </p>
                    </div>
                    <div class="pt-3 border-t-2 border-peanuts-black flex flex-wrap gap-2 text-xs font-bold">
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">Digital Routing</span>
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">Stage Box System</span>
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">Live Mixing</span>
                    </div>
                </div>

                <!-- Panel 2: Live Streaming vMix -->
                <div class="comic-box p-6 bg-peanuts-blue flex flex-col justify-between space-y-4">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="w-10 h-10 rounded-xl bg-white border-2 border-peanuts-black flex items-center justify-center text-peanuts-black text-xl font-bold shadow-comic-sm">
                                <i class="fa-solid fa-tower-broadcast"></i>
                            </span>
                            <span class="font-comic font-bold text-xs bg-peanuts-black text-white px-2.5 py-1 rounded">PANEL #2</span>
                        </div>
                        <h3 class="text-xl font-extrabold text-peanuts-black">vMix Live Switching</h3>
                        <p class="text-slate-800 text-sm font-medium leading-relaxed">
                            Mengoperasikan software <strong class="text-peanuts-black">vMix Production</strong> untuk siaran multi-kamera, integrasi title graphics lower-thirds, video routing NDI, dan live stream ke berbagai platform.
                        </p>
                    </div>
                    <div class="pt-3 border-t-2 border-peanuts-black flex flex-wrap gap-2 text-xs font-bold">
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">vMix Multi-Cam</span>
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">NDI Protocol</span>
                    </div>
                </div>

                <!-- Panel 3: Video Post-Production -->
                <div class="comic-box p-6 bg-peanuts-purple text-white flex flex-col justify-between space-y-4">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="w-10 h-10 rounded-xl bg-white text-peanuts-black border-2 border-peanuts-black flex items-center justify-center text-xl font-bold shadow-comic-sm">
                                <i class="fa-solid fa-film"></i>
                            </span>
                            <span class="font-comic font-bold text-xs bg-white text-peanuts-black px-2.5 py-1 rounded border border-peanuts-black">PANEL #3</span>
                        </div>
                        <h3 class="text-xl font-extrabold text-white">Video & Motion Graphics</h3>
                        <p class="text-purple-100 text-sm font-medium leading-relaxed">
                            Menguasai <strong class="text-peanuts-yellow">Adobe Premiere Pro & After Effects</strong> untuk cutting video liputan, motion graphics, serta pengolahan warna (*color grading*).
                        </p>
                    </div>
                    <div class="pt-3 border-t-2 border-white flex flex-wrap gap-2 text-xs font-bold text-peanuts-black">
                        <span class="px-2.5 py-1 bg-peanuts-yellow rounded-md border-2 border-peanuts-black">Premiere Pro</span>
                        <span class="px-2.5 py-1 bg-peanuts-yellow rounded-md border-2 border-peanuts-black">After Effects</span>
                    </div>
                </div>

                <!-- Panel 4: UI/UX Web Redesign (Figma) -->
                <div class="comic-box p-6 bg-peanuts-yellow md:col-span-2 flex flex-col justify-between space-y-4">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="w-10 h-10 rounded-xl bg-white border-2 border-peanuts-black flex items-center justify-center text-peanuts-black text-xl font-bold shadow-comic-sm">
                                <i class="fa-solid fa-pen-nib"></i>
                            </span>
                            <span class="font-comic font-bold text-xs bg-peanuts-black text-white px-2.5 py-1 rounded">PANEL #4</span>
                        </div>
                        <h3 class="text-2xl font-extrabold text-peanuts-black">UI/UX Figma Design & Redesign Portal TVRI</h3>
                        <p class="text-slate-800 text-sm font-medium leading-relaxed">
                            Selain di balik kamera & konsol mixer, saya juga aktif merancang pengalaman pengguna (*wireframing & prototyping*) aplikasi/website media di <strong class="text-peanuts-red">Figma & Canva</strong>. Salah satu karya utama saya adalah merancang ulang antarmuka dashboard streaming TVRI agar lebih interaktif dan ramah pengguna.
                        </p>
                    </div>
                    <div class="pt-3 border-t-2 border-peanuts-black flex flex-wrap gap-2 text-xs font-bold">
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">Figma Prototype</span>
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">TVRI Dashboard UI</span>
                        <span class="px-2.5 py-1 bg-white rounded-md border-2 border-peanuts-black">Canva Design</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- KEMAMPUAN (SKILLS COMIC BADGES) -->
    <section id="skills" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto space-y-2 mb-12">
            <span class="px-3 py-1 bg-peanuts-yellow text-peanuts-black text-xs font-bold uppercase rounded-md border-2 border-peanuts-black shadow-comic-sm inline-block">SKILL SET</span>
            <h2 class="text-3xl sm:text-4xl font-extrabold text-peanuts-black">Kemampuan Teknis</h2>
            <p class="text-slate-700 font-comic font-bold text-base">Perangkat keras & perangkat lunak siaran yang dikuasai.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            
            <!-- Skill 1: Midas M32 -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-yellow border-2 border-peanuts-black flex items-center justify-center text-peanuts-black font-bold text-lg">
                            <i class="fa-solid fa-sliders"></i>
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">Midas M32 Live</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Digital Audio Console</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-red text-white rounded border border-peanuts-black">ADVANCED</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-yellow h-full w-[92%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

            <!-- Skill 2: vMix Switcher -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-blue border-2 border-peanuts-black flex items-center justify-center text-peanuts-black font-bold text-lg">
                            <i class="fa-solid fa-desktop"></i>
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">vMix Switcher</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Live Video Switcher</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-blue text-peanuts-black rounded border border-peanuts-black">EXPERT</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-blue h-full w-[88%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

            <!-- Skill 3: Adobe Premiere Pro -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-purple text-white border-2 border-peanuts-black flex items-center justify-center font-extrabold text-base">
                            Pr
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">Adobe Premiere Pro</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Video Editing</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-purple text-white rounded border border-peanuts-black">MAHIR</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-purple h-full w-[85%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

            <!-- Skill 4: Adobe After Effects -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-red text-white border-2 border-peanuts-black flex items-center justify-center font-extrabold text-base">
                            Ae
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">Adobe After Effects</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Motion & VFX</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-red text-white rounded border border-peanuts-black">MEDIUM</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-red h-full w-[78%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

            <!-- Skill 5: Figma UI/UX -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-green border-2 border-peanuts-black flex items-center justify-center text-peanuts-black font-bold text-lg">
                            <i class="fa-brands fa-figma"></i>
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">Figma (UI/UX)</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Wireframe & Design</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-green text-peanuts-black rounded border border-peanuts-black">MAHIR</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-green h-full w-[84%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

            <!-- Skill 6: ENG Camera & Canva -->
            <div class="comic-box-sm p-5 bg-white space-y-3">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-peanuts-bg border-2 border-peanuts-black flex items-center justify-center text-peanuts-black font-bold text-lg">
                            <i class="fa-solid fa-camera"></i>
                        </div>
                        <div>
                            <h4 class="font-extrabold text-peanuts-black text-base">ENG Camera & Canva</h4>
                            <span class="text-xs font-comic font-bold text-slate-600">Field Cam & Visuals</span>
                        </div>
                    </div>
                    <span class="text-xs font-bold px-2 py-0.5 bg-peanuts-yellow text-peanuts-black rounded border border-peanuts-black">ADVANCED</span>
                </div>
                <div class="w-full bg-slate-200 h-3 rounded-full border-2 border-peanuts-black overflow-hidden">
                    <div class="bg-peanuts-yellow h-full w-[88%] border-r-2 border-peanuts-black"></div>
                </div>
            </div>

        </div>
    </section>

    <!-- PORTFOLIO SECTION -->
    <section id="portfolio" class="py-16 bg-peanuts-bg border-y-4 border-peanuts-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto space-y-2 mb-12">
                <span class="px-3 py-1 bg-peanuts-purple text-white text-xs font-bold uppercase rounded-md border-2 border-peanuts-black shadow-comic-sm inline-block">SHOWCASE</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-peanuts-black">Portofolio Terpilih</h2>
                <p class="text-slate-700 font-comic font-bold text-base">Sampel proyek nyata desain UI/UX dan produksi siaran.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Card 1: TVRI Figma UI Redesign -->
                <div class="comic-box bg-white overflow-hidden flex flex-col justify-between group">
                    <div>
                        <!-- Header Banner -->
                        <div class="h-44 bg-peanuts-yellow border-b-4 border-peanuts-black p-4 flex flex-col justify-between relative">
                            <div class="flex justify-between items-center">
                                <span class="bg-white text-peanuts-black text-xs font-bold font-comic px-2.5 py-1 rounded border-2 border-peanuts-black">FIGMA UI/UX</span>
                                <i class="fa-brands fa-figma text-2xl text-peanuts-black"></i>
                            </div>
                            <div class="text-center bg-white p-3 rounded-xl border-3 border-peanuts-black shadow-comic-sm">
                                <span class="font-extrabold text-base text-peanuts-black">TVRI DASHBOARD REDESIGN</span>
                            </div>
                        </div>

                        <div class="p-6 space-y-3">
                            <h3 class="text-xl font-extrabold text-peanuts-black group-hover:text-peanuts-red transition-colors">Redesign UI Figma Portal TVRI</h3>
                            <p class="text-slate-700 text-sm font-medium leading-relaxed">
                                Konsep perancangan antarmuka (wireframing) modern untuk platform siaran TVRI. Memudahkan pemirsa mengakses jadwal live streaming dan dokumentasi acara TV.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <a href="https://www.figma.com" target="_blank" rel="noopener" class="comic-btn w-full bg-peanuts-yellow hover:bg-yellow-300 text-peanuts-black py-2.5 text-xs uppercase">
                            <span>Buka Figma Link</span> <i class="fa-solid fa-arrow-up-right-from-square"></i>
                        </a>
                    </div>
                </div>

                <!-- Card 2: Multi-Cam Live Broadcast Setup -->
                <div class="comic-box bg-white overflow-hidden flex flex-col justify-between group">
                    <div>
                        <!-- Header Banner -->
                        <div class="h-44 bg-peanuts-blue border-b-4 border-peanuts-black p-4 flex flex-col justify-between relative">
                            <div class="flex justify-between items-center">
                                <span class="bg-white text-peanuts-black text-xs font-bold font-comic px-2.5 py-1 rounded border-2 border-peanuts-black">LIVE BROADCAST</span>
                                <i class="fa-solid fa-sliders text-2xl text-peanuts-black"></i>
                            </div>
                            <div class="text-center bg-white p-3 rounded-xl border-3 border-peanuts-black shadow-comic-sm">
                                <span class="font-extrabold text-base text-peanuts-black">MIDAS M32 & vMix SETUP</span>
                            </div>
                        </div>

                        <div class="p-6 space-y-3">
                            <h3 class="text-xl font-extrabold text-peanuts-black group-hover:text-peanuts-red transition-colors">Multi-Cam Live Broadcast Directing</h3>
                            <p class="text-slate-700 text-sm font-medium leading-relaxed">
                                Integrasi tata suara siaran langsung konsol Midas M32 Live dengan vMix multi-kamera switcher secara real-time tanpa delay.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <button onclick="openModal('Proyek Multi-Cam Live Broadcast', 'Sistem siaran ini mengintegrasikan Stage Box Midas DL16 dengan audio routing 16+ input channel studio, equalizer vokal live, dan pengiriman sinyal audio NDI ke vMix switcher.')" class="comic-btn w-full bg-peanuts-blue hover:bg-blue-300 text-peanuts-black py-2.5 text-xs uppercase">
                            <span>Detail Teknis</span> <i class="fa-solid fa-circle-info"></i>
                        </button>
                    </div>
                </div>

                <!-- Card 3: Dokumenter Temanggung -->
                <div class="comic-box bg-white overflow-hidden flex flex-col justify-between group">
                    <div>
                        <!-- Header Banner -->
                        <div class="h-44 bg-peanuts-red border-b-4 border-peanuts-black p-4 flex flex-col justify-between relative">
                            <div class="flex justify-between items-center">
                                <span class="bg-white text-peanuts-black text-xs font-bold font-comic px-2.5 py-1 rounded border-2 border-peanuts-black">DOCUMENTARY</span>
                                <i class="fa-solid fa-video text-2xl text-white"></i>
                            </div>
                            <div class="text-center bg-white p-3 rounded-xl border-3 border-peanuts-black shadow-comic-sm">
                                <span class="font-extrabold text-base text-peanuts-black">KULTUR TEMANGGUNG</span>
                            </div>
                        </div>

                        <div class="p-6 space-y-3">
                            <h3 class="text-xl font-extrabold text-peanuts-black group-hover:text-peanuts-red transition-colors">Dokumenter Kebudayaan Temanggung</h3>
                            <p class="text-slate-700 text-sm font-medium leading-relaxed">
                                Produksi video liputan kebudayaan lokal menggunakan ENG Camera setup, penataan audio mikrofon klip, dan color grading Premiere Pro.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <button onclick="openModal('Dokumenter Temanggung', 'Liputan visual budaya lokal daerah Temanggung. Proses meliputi riset lapangan, rekaman kamera ENG, wawancara narasumber, penyuntingan klip di Premiere Pro, serta motion graphics After Effects.')" class="comic-btn w-full bg-peanuts-red hover:bg-red-600 text-white py-2.5 text-xs uppercase">
                            <span>Detail Teknis</span> <i class="fa-solid fa-circle-info"></i>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- HOBI (HOBBIES SECTION) -->
    <section id="hobbies" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto space-y-2 mb-12">
            <span class="px-3 py-1 bg-peanuts-green text-peanuts-black text-xs font-bold uppercase rounded-md border-2 border-peanuts-black shadow-comic-sm inline-block">FUN & INTERESTS</span>
            <h2 class="text-3xl sm:text-4xl font-extrabold text-peanuts-black">Hobi & Eksplorasi</h2>
            <p class="text-slate-700 font-comic font-bold text-base">Kegiatan favorit Ezekiel di luar jam studio siaran.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            
            <!-- Hobby 1: Coffee Brewing -->
            <div class="comic-box bg-white p-7 space-y-4 relative overflow-hidden group">
                <div class="w-14 h-14 rounded-2xl bg-peanuts-yellow border-3 border-peanuts-black flex items-center justify-center text-peanuts-black text-2xl shadow-comic-sm">
                    ☕
                </div>
                <div class="space-y-2">
                    <span class="text-xs font-bold font-comic text-peanuts-red uppercase tracking-wider">Lokal Temanggung</span>
                    <h3 class="text-2xl font-extrabold text-peanuts-black">Manual Coffee Brewing</h3>
                    <p class="text-slate-700 text-sm font-medium leading-relaxed">
                        Mengeksplorasi ekstraksi biji kopi khas <strong class="text-peanuts-black">Robusta Temanggung</strong> dengan teknik seduh manual (V60 & AeroPress). Melatih ketelitian rasio seperti halnya *tuning audio mixer*!
                    </p>
                </div>
                <div class="pt-3 border-t-2 border-peanuts-black text-xs font-bold font-comic text-slate-800">
                    <i class="fa-solid fa-mug-saucer text-peanuts-red mr-1"></i> Robusta Temanggung Specialty
                </div>
            </div>

            <!-- Hobby 2: Street Photography -->
            <div class="comic-box bg-white p-7 space-y-4 relative overflow-hidden group">
                <div class="w-14 h-14 rounded-2xl bg-peanuts-blue border-3 border-peanuts-black flex items-center justify-center text-peanuts-black text-2xl shadow-comic-sm">
                    📷
                </div>
                <div class="space-y-2">
                    <span class="text-xs font-bold font-comic text-peanuts-blue uppercase tracking-wider">Visual Framing</span>
                    <h3 class="text-2xl font-extrabold text-peanuts-black">Street Photography</h3>
                    <p class="text-slate-700 text-sm font-medium leading-relaxed">
                        Menangkap momen candid jalanan, permainan cahaya alami, dan komposisi frame sinematik. Melatih kepekaan visual saat mengambil gambar siaran studio.
                    </p>
                </div>
                <div class="pt-3 border-t-2 border-peanuts-black text-xs font-bold font-comic text-slate-800">
                    <i class="fa-solid fa-camera text-peanuts-blue mr-1"></i> Frame & Color Grading
                </div>
            </div>

            <!-- Hobby 3: VALORANT Gaming -->
            <div class="comic-box bg-white p-7 space-y-4 relative overflow-hidden group">
                <div class="w-14 h-14 rounded-2xl bg-peanuts-red text-white border-3 border-peanuts-black flex items-center justify-center text-2xl shadow-comic-sm">
                    🎯
                </div>
                <div class="space-y-2">
                    <span class="text-xs font-bold font-comic text-peanuts-red uppercase tracking-wider">Reflex & Focus</span>
                    <h3 class="text-2xl font-extrabold text-peanuts-black">Tactical Gaming (VALORANT)</h3>
                    <p class="text-slate-700 text-sm font-medium leading-relaxed">
                        Bermain game taktis seperti VALORANT untuk melatih refleks cepat, komunikasi tim yang terarah di bawah tekanan, serta eksekusi strategi instan.
                    </p>
                </div>
                <div class="pt-3 border-t-2 border-peanuts-black text-xs font-bold font-comic text-slate-800">
                    <i class="fa-solid fa-gamepad text-peanuts-red mr-1"></i> Team Callout & Strategy
                </div>
            </div>

        </div>
    </section>

    <!-- KONTAK & LOKASI (COMIC MAILBOX SECTION) -->
    <section id="contact" class="py-16 bg-white border-t-4 border-peanuts-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-start">
                
                <!-- Left Info & Mailbox -->
                <div class="lg:col-span-5 space-y-6">
                    <div>
                        <span class="px-3 py-1 bg-peanuts-red text-white text-xs font-bold uppercase rounded-md border-2 border-peanuts-black shadow-comic-sm inline-block">SNOOPY'S MAILBOX</span>
                        <h2 class="text-3xl sm:text-4xl font-extrabold text-peanuts-black mt-2">Hubungi Kontak</h2>
                        <p class="text-slate-700 font-comic font-bold text-base mt-2">
                            Ingin berdiskusi seputar proyek siaran live broadcast, sound engineering, atau desain UI/UX? Kirimkan pesan Anda!
                        </p>
                    </div>

                    <div class="space-y-4">
                        
                        <!-- Email Card -->
                        <div class="comic-box-sm p-4 bg-peanuts-bg flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-lg bg-peanuts-red text-white border-2 border-peanuts-black flex items-center justify-center text-lg">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <div class="text-xs font-bold font-comic text-slate-600">Email Utama</div>
                                    <div class="text-sm font-extrabold text-peanuts-black">ezekiel.jatiputra@gmail.com</div>
                                </div>
                            </div>
                            <button onclick="copyToClipboard('ezekiel.jatiputra@gmail.com')" class="comic-btn bg-peanuts-yellow hover:bg-yellow-300 text-peanuts-black p-2 text-xs" title="Salin Email">
                                <i class="fa-regular fa-copy"></i>
                            </button>
                        </div>

                        <!-- Instagram Card -->
                        <a href="https://instagram.com/ezekiel.jatiputra" target="_blank" rel="noopener" class="comic-box-sm p-4 bg-peanuts-bg flex items-center justify-between block group">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-lg bg-peanuts-purple text-white border-2 border-peanuts-black flex items-center justify-center text-lg">
                                    <i class="fa-brands fa-instagram"></i>
                                </div>
                                <div>
                                    <div class="text-xs font-bold font-comic text-slate-600">Instagram</div>
                                    <div class="text-sm font-extrabold text-peanuts-black group-hover:text-peanuts-red transition-colors">@ezekiel.jatiputra</div>
                                </div>
                            </div>
                            <i class="fa-solid fa-arrow-up-right-from-square text-peanuts-black text-xs mr-2"></i>
                        </a>

                        <!-- Location Card -->
                        <div class="comic-box-sm p-4 bg-peanuts-bg flex items-center gap-3">
                            <div class="w-10 h-10 rounded-lg bg-peanuts-green border-2 border-peanuts-black flex items-center justify-center text-lg text-peanuts-black">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <div class="text-xs font-bold font-comic text-slate-600">Lokasi Domisili</div>
                                <div class="text-sm font-extrabold text-peanuts-black">Temanggung, Jawa Tengah, Indonesia</div>
                            </div>
                        </div>

                    </div>
                </div>

                <!-- Right Form -->
                <div class="lg:col-span-7">
                    <div class="comic-box bg-peanuts-bg p-6 sm:p-8 space-y-4">
                        <h3 class="text-2xl font-extrabold text-peanuts-black flex items-center gap-2">
                            <i class="fa-solid fa-paper-plane text-peanuts-red"></i> Kirim Pesan Cepat
                        </h3>

                        <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                                <div>
                                    <label for="nama" class="block text-xs font-bold text-peanuts-black uppercase mb-1">Nama Anda</label>
                                    <input type="text" id="nama" required placeholder="Masukkan nama..." class="w-full bg-white border-3 border-peanuts-black rounded-xl px-4 py-2.5 text-sm font-bold text-peanuts-black focus:outline-none focus:bg-yellow-50">
                                </div>
                                <div>
                                    <label for="email" class="block text-xs font-bold text-peanuts-black uppercase mb-1">Alamat Email</label>
                                    <input type="email" id="email" required placeholder="nama@email.com" class="w-full bg-white border-3 border-peanuts-black rounded-xl px-4 py-2.5 text-sm font-bold text-peanuts-black focus:outline-none focus:bg-yellow-50">
                                </div>
                            </div>

                            <div>
                                <label for="subjek" class="block text-xs font-bold text-peanuts-black uppercase mb-1">Subjek Pesan</label>
                                <input type="text" id="subjek" required placeholder="Diskusi Midas M32 / vMix..." class="w-full bg-white border-3 border-peanuts-black rounded-xl px-4 py-2.5 text-sm font-bold text-peanuts-black focus:outline-none focus:bg-yellow-50">
                            </div>

                            <div>
                                <label for="pesan" class="block text-xs font-bold text-peanuts-black uppercase mb-1">Pesan</label>
                                <textarea id="pesan" rows="4" required placeholder="Tuliskan pesan Anda di sini..." class="w-full bg-white border-3 border-peanuts-black rounded-xl px-4 py-2.5 text-sm font-bold text-peanuts-black focus:outline-none focus:bg-yellow-50 resize-none"></textarea>
                            </div>

                            <button type="submit" class="comic-btn w-full bg-peanuts-red hover:bg-red-600 text-white py-3.5 text-base uppercase">
                                <i class="fa-solid fa-paper-plane"></i> Kirim Pesan Sekarang
                            </button>
                        </form>
                    </div>
                </div>

            </div>

        </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-8 bg-peanuts-black text-white text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-center sm:text-left font-comic">
            <div>
                <p class="font-bold text-sm text-peanuts-yellow">&copy; <span id="year"></span> Ezekiel Franztio Jatiputra 🐾</p>
                <p class="text-slate-400 mt-0.5">Broadcast Multimedia & Audio Specialist • Temanggung, Central Java</p>
            </div>
            
            <div class="flex items-center space-x-4 text-lg">
                <a href="https://instagram.com/ezekiel.jatiputra" target="_blank" rel="noopener" class="hover:text-peanuts-yellow transition-colors" title="Instagram">
                    <i class="fa-brands fa-instagram"></i>
                </a>
                <a href="mailto:ezekiel.jatiputra@gmail.com" class="hover:text-peanuts-red transition-colors" title="Email Direct">
                    <i class="fa-solid fa-envelope"></i>
                </a>
            </div>
        </div>
    </footer>

    <!-- COMIC MODAL POPUP -->
    <div id="modal" class="fixed inset-0 z-50 bg-peanuts-black/70 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="comic-box max-w-lg w-full bg-white p-6 space-y-4 animate-comic-float">
            <div class="flex items-center justify-between border-b-3 border-peanuts-black pb-3">
                <h3 id="modal-title" class="text-xl font-extrabold text-peanuts-black">Detail Proyek</h3>
                <button onclick="closeModal()" class="w-8 h-8 rounded-lg bg-peanuts-red text-white border-2 border-peanuts-black flex items-center justify-center font-bold">
                    ✕
                </button>
            </div>
            <p id="modal-content" class="text-slate-800 font-comic font-bold text-sm leading-relaxed">
                Deskripsi detail teknis komik...
            </p>
            <div class="pt-2 text-right">
                <button onclick="closeModal()" class="comic-btn bg-peanuts-yellow text-peanuts-black px-5 py-2 text-xs uppercase">
                    Tutup Modal
                </button>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Set dynamic year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuIcon = document.getElementById('menu-icon');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
            if(mobileMenu.classList.contains('hidden')) {
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            } else {
                menuIcon.classList.remove('fa-bars');
                menuIcon.classList.add('fa-xmark');
            }
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            });
        });

        // Toast Notification
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            toastMsg.textContent = message;
            toast.classList.remove('translate-y-32', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');

            setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-32', 'opacity-0');
            }, 3000);
        }

        // Copy Email to Clipboard safely
        function copyToClipboard(text) {
            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(text);
            } else {
                const textArea = document.createElement("textarea");
                textArea.value = text;
                textArea.style.position = "fixed";
                textArea.style.left = "-999999px";
                document.body.appendChild(textArea);
                textArea.focus();
                textArea.select();
                try {
                    document.execCommand('copy');
                } catch (error) {
                    console.error('Fallback failed', error);
                }
                document.body.removeChild(textArea);
            }
            showToast('Email (' + text + ') berhasil disalin! 🐾');
        }

        // Contact Form Handling
        function handleFormSubmit(event) {
            event.preventDefault();
            const nama = document.getElementById('nama').value;
            showToast(`Terima kasih ${nama}, pesan Anda sudah terikirim! 🐾`);
            document.getElementById('contact-form').reset();
        }

        // Modal Functions
        function openModal(title, content) {
            document.getElementById('modal-title').textContent = title;
            document.getElementById('modal-content').textContent = content;
            document.getElementById('modal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
        }

        window.onclick = function(event) {
            const modal = document.getElementById('modal');
            if (event.target === modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
