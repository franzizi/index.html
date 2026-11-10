<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ezekiel Franztio Jatiputra | Broadcast Multimedia & Media Production</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            dark: '#0a0d14',
                            card: '#121824',
                            border: '#1e293b',
                            accent: '#00f2fe',
                            purple: '#7928ca',
                            pink: '#ff0080',
                            glow: 'rgba(0, 242, 254, 0.15)'
                        }
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'float': 'float 4s ease-in-out infinite',
                        'bar-bounce': 'barBounce 1.2s ease-in-out infinite alternate',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-10px)' },
                        },
                        barBounce: {
                            '0%': { height: '15%' },
                            '100%': { height: '100%' }
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0a0d14;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #00f2fe;
        }

        /* Glassmorphic cards */
        .glass-card {
            background: rgba(18, 24, 36, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card:hover {
            border-color: rgba(0, 242, 254, 0.3);
            box-shadow: 0 0 25px rgba(0, 242, 254, 0.1);
        }

        /* Glow Text Effect */
        .text-glow {
            text-shadow: 0 0 12px rgba(0, 242, 254, 0.4);
        }

        /* Audio Visualizer Bars */
        .v-bar {
            width: 4px;
            background: linear-gradient(to top, #00f2fe, #7928ca);
            border-radius: 2px;
        }
    </style>
</head>
<body class="bg-brand-dark text-slate-200 font-sans selection:bg-cyan-500 selection:text-black min-h-screen relative overflow-x-hidden">

    <!-- Glowing Background Orbs -->
    <div class="fixed top-0 left-1/4 w-96 h-96 bg-cyan-500/10 rounded-full blur-[120px] pointer-events-none -z-10"></div>
    <div class="fixed bottom-1/3 right-10 w-96 h-96 bg-purple-600/10 rounded-full blur-[140px] pointer-events-none -z-10"></div>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-32 opacity-0 transition-all duration-300 glass-card px-5 py-4 rounded-xl border border-cyan-500/30 flex items-center gap-3 text-sm shadow-2xl">
        <i class="fa-solid fa-circle-check text-cyan-400 text-lg"></i>
        <span id="toast-message" class="text-white font-medium">Email berhasil disalin!</span>
    </div>

    <!-- NAVBAR -->
    <header class="fixed top-0 left-0 w-full z-40 glass-card border-b border-slate-800/60 bg-brand-dark/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <!-- Logo / Brand -->
            <a href="#hero" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-cyan-500 to-purple-600 flex items-center justify-center text-black font-extrabold text-lg shadow-lg group-hover:scale-105 transition-transform">
                    EF
                </div>
                <div class="flex flex-col">
                    <span class="font-bold text-slate-100 tracking-wide text-base leading-tight group-hover:text-cyan-400 transition-colors">Ezekiel Franztio</span>
                    <span class="text-xs text-slate-400 tracking-wider uppercase font-medium">Broadcast & Media</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                <a href="#about" class="text-slate-300 hover:text-cyan-400 transition-colors">Profil</a>
                <a href="#skills" class="text-slate-300 hover:text-cyan-400 transition-colors">Kemampuan</a>
                <a href="#portfolio" class="text-slate-300 hover:text-cyan-400 transition-colors">Portofolio</a>
                <a href="#hobbies" class="text-slate-300 hover:text-cyan-400 transition-colors">Hobi</a>
                <a href="#contact" class="text-slate-300 hover:text-cyan-400 transition-colors">Kontak</a>
            </nav>

            <!-- CTA Right Header -->
            <div class="hidden md:flex items-center gap-4">
                <a href="#contact" class="relative inline-flex items-center justify-center p-0.5 overflow-hidden text-xs font-semibold text-slate-100 rounded-xl group bg-gradient-to-br from-cyan-500 to-purple-600 group-hover:from-cyan-500 group-hover:to-purple-600 hover:text-white shadow-md hover:shadow-cyan-500/20 transition-all">
                    <span class="relative px-4 py-2 transition-all ease-in duration-75 bg-brand-dark rounded-[10px] group-hover:bg-opacity-0">
                        <i class="fa-solid fa-paper-plane mr-2 text-cyan-400 group-hover:text-white"></i> Hubungi Saya
                    </span>
                </a>
            </div>

            <!-- Mobile Hamburger Button -->
            <button id="mobile-menu-btn" class="md:hidden text-slate-300 hover:text-cyan-400 focus:outline-none p-2" aria-label="Toggle Navigation">
                <i class="fa-solid fa-bars text-2xl" id="menu-icon"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden glass-card border-t border-slate-800 px-6 py-6 space-y-4">
            <a href="#about" class="mobile-link block text-slate-200 hover:text-cyan-400 text-base font-medium">Profil</a>
            <a href="#skills" class="mobile-link block text-slate-200 hover:text-cyan-400 text-base font-medium">Kemampuan</a>
            <a href="#portfolio" class="mobile-link block text-slate-200 hover:text-cyan-400 text-base font-medium">Portofolio</a>
            <a href="#hobbies" class="mobile-link block text-slate-200 hover:text-cyan-400 text-base font-medium">Hobi</a>
            <a href="#contact" class="mobile-link block text-slate-200 hover:text-cyan-400 text-base font-medium">Kontak</a>
            <div class="pt-4 border-t border-slate-800">
                <a href="#contact" class="mobile-link block text-center w-full py-3 bg-gradient-to-r from-cyan-500 to-purple-600 text-black font-bold rounded-xl text-sm">
                    Hubungi Saya
                </a>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="hero" class="pt-32 pb-20 md:pt-44 md:pb-32 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 min-h-[90vh] flex items-center">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center w-full">
            
            <!-- Left Text Content -->
            <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                
                <!-- Status Badge -->
                <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-slate-900/90 border border-cyan-500/30 text-cyan-400 text-xs font-semibold tracking-wide">
                    <span class="w-2 h-2 rounded-full bg-cyan-400 animate-ping"></span>
                    <span>Broadcasting & Visual Production Specialist</span>
                </div>

                <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white tracking-tight leading-[1.15]">
                    Halo, Saya <br class="hidden sm:inline"/>
                    <span class="bg-gradient-to-r from-cyan-400 via-teal-300 to-purple-500 bg-clip-text text-transparent text-glow">
                        Ezekiel Franztio Jatiputra
                    </span>
                </h1>

                <p class="text-lg sm:text-xl text-cyan-200/90 font-medium tracking-wide">
                    Mahasiswa Broadcast Multimedia & Media Production
                </p>

                <p class="text-slate-400 text-base sm:text-lg leading-relaxed max-w-2xl mx-auto lg:mx-0">
                    Berfokus pada tata kelola produksi siaran studio, audio engineering, live streaming multi-kamera, serta perancangan antarmuka visual UI/UX web dan media interaktif.
                </p>

                <!-- Action Buttons -->
                <div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 pt-4">
                    <a href="#portfolio" class="px-7 py-3.5 rounded-xl bg-gradient-to-r from-cyan-500 to-blue-600 text-black font-bold text-sm hover:opacity-90 hover:shadow-lg hover:shadow-cyan-500/25 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-play"></i> Lihat Portofolio
                    </a>
                    <a href="#contact" class="px-7 py-3.5 rounded-xl glass-card text-white font-semibold text-sm hover:bg-slate-800 hover:border-slate-600 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-envelope text-cyan-400"></i> Hubungi Kontak
                    </a>
                </div>

                <!-- Live Quick Stats -->
                <div class="grid grid-cols-3 gap-4 pt-8 border-t border-slate-800/80 max-w-md mx-auto lg:mx-0 text-left">
                    <div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-white">15+</div>
                        <div class="text-xs text-slate-400 mt-0.5">Live Broadcast</div>
                    </div>
                    <div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-white">100%</div>
                        <div class="text-xs text-slate-400 mt-0.5">Audio Precision</div>
                    </div>
                    <div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-white">Temanggung</div>
                        <div class="text-xs text-slate-400 mt-0.5">Base Location</div>
                    </div>
                </div>

            </div>

            <!-- Right Interactive Broadcast Control Display -->
            <div class="lg:col-span-5 flex justify-center">
                <div class="relative w-full max-w-md">
                    <!-- Outer Glow Effect -->
                    <div class="absolute -inset-1 bg-gradient-to-r from-cyan-500 to-purple-600 rounded-3xl blur-xl opacity-30 group-hover:opacity-100 transition duration-1000 group-hover:duration-200"></div>

                    <!-- Virtual Studio Rack Display Box -->
                    <div class="relative glass-card rounded-2xl p-6 space-y-6 border border-slate-700/80">
                        
                        <!-- Header Screen -->
                        <div class="flex items-center justify-between pb-4 border-b border-slate-800">
                            <div class="flex items-center gap-3">
                                <div class="w-3 h-3 rounded-full bg-red-500 animate-pulse"></div>
                                <span class="text-xs font-mono font-bold text-slate-300 uppercase tracking-wider">STUDIO LIVE FEED // ON AIR</span>
                            </div>
                            <span class="text-xs font-mono text-cyan-400 bg-cyan-950/60 px-2.5 py-1 rounded border border-cyan-800">Midas M32 Active</span>
                        </div>

                        <!-- Profile Avatar Card Inside Studio Display -->
                        <div class="flex items-center gap-4 bg-slate-900/80 p-4 rounded-xl border border-slate-800">
                            <div class="relative">
                                <div class="w-16 h-16 rounded-xl bg-gradient-to-br from-cyan-500 to-indigo-600 p-0.5 shadow-md">
                                    <div class="w-full h-full bg-slate-900 rounded-[10px] flex items-center justify-center text-cyan-400 text-2xl font-bold">
                                        <i class="fa-solid fa-headset"></i>
                                    </div>
                                </div>
                                <span class="absolute -bottom-1 -right-1 w-4 h-4 bg-emerald-500 border-2 border-slate-900 rounded-full"></span>
                            </div>
                            <div>
                                <h3 class="font-bold text-white text-base">Ezekiel F. Jatiputra</h3>
                                <p class="text-xs text-slate-400 mt-0.5"><i class="fa-solid fa-location-dot text-cyan-400 mr-1"></i> Temanggung, Jawa Tengah</p>
                                <span class="inline-block text-[10px] font-semibold text-purple-300 bg-purple-950/60 px-2 py-0.5 rounded mt-1">Broadcast Multimedia</span>
                            </div>
                        </div>

                        <!-- Audio Visualizer Simulation -->
                        <div class="space-y-2 bg-slate-950/90 p-4 rounded-xl border border-slate-800/80">
                            <div class="flex justify-between text-xs text-slate-400 font-mono">
                                <span>AUDIO MASTER L/R</span>
                                <span class="text-emerald-400">-3 dB (OPTIMAL)</span>
                            </div>
                            <div class="h-10 flex items-end justify-between gap-1 px-1">
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.1s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.3s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.2s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.5s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.4s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.7s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.2s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.6s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.3s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.8s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.4s"></div>
                                <div class="v-bar animate-bar-bounce" style="animation-delay: 0.1s"></div>
                            </div>
                        </div>

                        <!-- Quick Badges Studio Equipment -->
                        <div class="grid grid-cols-2 gap-2 text-xs font-mono">
                            <div class="bg-slate-900/60 p-2.5 rounded-lg border border-slate-800 text-slate-300 flex items-center gap-2">
                                <i class="fa-solid fa-sliders text-cyan-400"></i> Midas M32 Live
                            </div>
                            <div class="bg-slate-900/60 p-2.5 rounded-lg border border-slate-800 text-slate-300 flex items-center gap-2">
                                <i class="fa-solid fa-tower-broadcast text-purple-400"></i> vMix Switcher
                            </div>
                            <div class="bg-slate-900/60 p-2.5 rounded-lg border border-slate-800 text-slate-300 flex items-center gap-2">
                                <i class="fa-solid fa-video text-teal-400"></i> ENG Cam Setup
                            </div>
                            <div class="bg-slate-900/60 p-2.5 rounded-lg border border-slate-800 text-slate-300 flex items-center gap-2">
                                <i class="fa-solid fa-pen-nib text-pink-400"></i> Figma UI Wireframe
                            </div>
                        </div>

                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- PROFIL & PENJELASAN (ABOUT ME) -->
    <section id="about" class="py-20 bg-slate-950/60 border-y border-slate-800/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <!-- Section Header -->
            <div class="text-center max-w-3xl mx-auto space-y-3 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-cyan-400">Tentang Saya</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">Profil & Latar Belakang Profesional</p>
                <p class="text-slate-400 text-sm sm:text-base">Mengkombinasikan ketelitian teknis peralatan siaran audio-visual dengan estetika desain digital modern.</p>
            </div>

            <!-- Bento Grid Layout -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                
                <!-- Card 1: Studio Broadcast & Audio Engineering -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between space-y-4 md:col-span-2 group">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-cyan-500/10 border border-cyan-500/30 flex items-center justify-center text-cyan-400 text-xl group-hover:bg-cyan-500 group-hover:text-black transition-all">
                            <i class="fa-solid fa-sliders"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Pengalaman Siaran Studio & Audio Engineering</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Sebagai mahasiswa Broadcast Multimedia, saya aktif menangani tata suara siaran langsung (*live broadcast audio*) menggunakan konsol digital industri seperti <strong class="text-cyan-300">Midas M32 Live & Stage Box System</strong>. Berpengalaman merumuskan signal routing, mikrofonisasi studio, gain staging, hingga sound monitoring bebas lag untuk acara siaran tingkat tinggi.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-slate-800 flex flex-wrap gap-2 text-xs">
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Audio Routing</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Digital Mixers</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Multi-Channel Recording</span>
                    </div>
                </div>

                <!-- Card 2: Live Streaming Ops -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between space-y-4 group">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-purple-500/10 border border-purple-500/30 flex items-center justify-center text-purple-400 text-xl group-hover:bg-purple-500 group-hover:text-black transition-all">
                            <i class="fa-solid fa-tower-broadcast"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Live Streaming Multi-Cam</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Terbiasa mengoperasikan software <strong class="text-purple-300">vMix Production</strong> untuk kebutuhan siaran multi-kamera, integrasi title graphics overlay, NDI video routing, dan kustomisasi skenario siaran langsung secara konsisten.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-slate-800 flex flex-wrap gap-2 text-xs">
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">vMix System</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">ENG Setup</span>
                    </div>
                </div>

                <!-- Card 3: Video Production & Post-processing -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between space-y-4 group">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-indigo-500/10 border border-indigo-500/30 flex items-center justify-center text-indigo-400 text-xl group-hover:bg-indigo-500 group-hover:text-black transition-all">
                            <i class="fa-solid fa-film"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Video Editing & Motion</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Menguasai <strong class="text-indigo-300">Adobe Premiere Pro & After Effects</strong> untuk penyuntingan video liputan berita, sinematografi acara, pengolahan efek visual motion graphics, serta tata warna (*color grading*).
                        </p>
                    </div>
                    <div class="pt-4 border-t border-slate-800 flex flex-wrap gap-2 text-xs">
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Premiere Pro</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">After Effects</span>
                    </div>
                </div>

                <!-- Card 4: UI/UX Web Design -->
                <div class="glass-card rounded-2xl p-7 flex flex-col justify-between space-y-4 md:col-span-2 group">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-pink-500/10 border border-pink-500/30 flex items-center justify-center text-pink-400 text-xl group-hover:bg-pink-500 group-hover:text-black transition-all">
                            <i class="fa-solid fa-pen-nib"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Desain UI/UX Web Media</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Tidak hanya di belakang layar kaca siaran, saya juga mengeksplorasi pembuatan rancangan pengalaman pengguna (*UI/UX Wireframing*) menggunakan <strong class="text-pink-300">Figma & Canva</strong>. Salah satunya merancang konsep ulang antarmuka (redesign) dashboard platform TV broadcasting interaktif agar lebih efisien dan ramah pengguna.
                        </p>
                    </div>
                    <div class="pt-4 border-t border-slate-800 flex flex-wrap gap-2 text-xs">
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Figma Wireframing</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">UI Broadcast Dashboard</span>
                        <span class="px-2.5 py-1 rounded-md bg-slate-900 text-slate-300 border border-slate-800">Canva Visuals</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- KEMAMPUAN (SKILLS) SECTION -->
    <section id="skills" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto space-y-3 mb-16">
            <h2 class="text-xs font-bold uppercase tracking-widest text-cyan-400">Penguasaan Alat & Software</h2>
            <p class="text-3xl sm:text-4xl font-extrabold text-white">Kemampuan Teknis (Skills)</p>
            <p class="text-slate-400 text-sm sm:text-base">Daftar perangkat keras studio broadcast dan software kreatif yang saya kuasai.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            
            <!-- Skill 1: Midas M32 Live -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-cyan-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-cyan-950 border border-cyan-800 flex items-center justify-center text-cyan-400">
                            <i class="fa-solid fa-sliders text-lg"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">Midas M32 Live & Stage Box</h4>
                            <span class="text-xs text-slate-400">Audio Digital Console</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Sound Routing & Mixing</span>
                        <span class="text-cyan-400">Tingkat Lanjut</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-cyan-500 to-blue-500 rounded-full w-[90%]"></div>
                    </div>
                </div>
            </div>

            <!-- Skill 2: vMix Switcher -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-purple-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-purple-950 border border-purple-800 flex items-center justify-center text-purple-400">
                            <i class="fa-solid fa-tv text-lg"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">vMix Production</h4>
                            <span class="text-xs text-slate-400">Live Video Switcher</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Multi-Cam Streaming</span>
                        <span class="text-purple-400">Tingkat Lanjut</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-purple-500 to-indigo-500 rounded-full w-[88%]"></div>
                    </div>
                </div>
            </div>

            <!-- Skill 3: Adobe Premiere Pro -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-indigo-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-indigo-950 border border-indigo-800 flex items-center justify-center text-indigo-400 font-black text-lg">
                            Pr
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">Adobe Premiere Pro</h4>
                            <span class="text-xs text-slate-400">Video Editing & Cutting</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Post-Production</span>
                        <span class="text-indigo-400">Mahir</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-indigo-500 to-blue-500 rounded-full w-[85%]"></div>
                    </div>
                </div>
            </div>

            <!-- Skill 4: Adobe After Effects -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-blue-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-blue-950 border border-blue-800 flex items-center justify-center text-blue-400 font-black text-lg">
                            Ae
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">Adobe After Effects</h4>
                            <span class="text-xs text-slate-400">Motion Graphics & VFX</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Lower Thirds & Graphics</span>
                        <span class="text-blue-400">Menengah</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-blue-500 to-cyan-500 rounded-full w-[78%]"></div>
                    </div>
                </div>
            </div>

            <!-- Skill 5: Figma (UI/UX Wireframing) -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-pink-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-pink-950 border border-pink-800 flex items-center justify-center text-pink-400">
                            <i class="fa-brands fa-figma text-xl"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">Figma (UI/UX)</h4>
                            <span class="text-xs text-slate-400">Wireframing & Prototyping</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Layouting Web & App</span>
                        <span class="text-pink-400">Mahir</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-pink-500 to-purple-500 rounded-full w-[82%]"></div>
                    </div>
                </div>
            </div>

            <!-- Skill 6: ENG Camera Setup -->
            <div class="glass-card rounded-xl p-6 space-y-4 hover:border-teal-500/40 transition-all">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-lg bg-teal-950 border border-teal-800 flex items-center justify-center text-teal-400">
                            <i class="fa-solid fa-camera-retro text-lg"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-white text-base">ENG Camera Setup</h4>
                            <span class="text-xs text-slate-400">Field & Studio Camera</span>
                        </div>
                    </div>
                </div>
                <div class="space-y-1.5">
                    <div class="flex justify-between text-xs font-semibold">
                        <span class="text-slate-300">Framing & Rigging</span>
                        <span class="text-teal-400">Tingkat Lanjut</span>
                    </div>
                    <div class="w-full h-2 bg-slate-900 rounded-full overflow-hidden border border-slate-800">
                        <div class="h-full bg-gradient-to-r from-teal-500 to-emerald-500 rounded-full w-[88%]"></div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- PORTFOLIO SECTION -->
    <section id="portfolio" class="py-20 bg-slate-950/60 border-y border-slate-800/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto space-y-3 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-cyan-400">Karya Terpilih</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">Portofolio Broadcast & UI/UX</p>
                <p class="text-slate-400 text-sm sm:text-base">Kumpulan sampel proyek siaran media, tata suara studio, serta rancangan antarmuka Figma.</p>
            </div>

            <!-- Portfolio Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Project 1: Figma TVRI UI Redesign -->
                <div class="glass-card rounded-2xl overflow-hidden group border border-slate-800 flex flex-col justify-between">
                    <div>
                        <!-- Project Visual Header -->
                        <div class="relative h-48 bg-slate-900 overflow-hidden flex items-center justify-center border-b border-slate-800">
                            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-transparent to-transparent z-10"></div>
                            <!-- Mockup Graphic Screen -->
                            <div class="w-11/12 h-36 bg-slate-950 rounded-lg border border-pink-500/30 p-3 shadow-xl transform group-hover:scale-105 transition-transform duration-500 flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-800 pb-2">
                                    <span class="text-[10px] font-bold text-pink-400 flex items-center gap-1">
                                        <i class="fa-brands fa-figma"></i> TVRI DASHBOARD WIREFRAME
                                    </span>
                                    <span class="text-[9px] bg-pink-950 text-pink-300 px-1.5 py-0.5 rounded">UI/UX</span>
                                </div>
                                <div class="grid grid-cols-3 gap-1.5 my-auto">
                                    <div class="h-10 bg-slate-900 rounded border border-slate-800"></div>
                                    <div class="h-10 bg-slate-900 rounded border border-slate-800"></div>
                                    <div class="h-10 bg-cyan-950/60 rounded border border-cyan-800"></div>
                                </div>
                                <div class="h-2 bg-slate-800 rounded w-2/3"></div>
                            </div>
                        </div>

                        <!-- Details -->
                        <div class="p-6 space-y-3">
                            <div class="flex items-center gap-2 text-xs font-semibold text-pink-400">
                                <i class="fa-brands fa-figma"></i> Figma Prototype
                            </div>
                            <h3 class="text-xl font-bold text-white group-hover:text-cyan-400 transition-colors">Redesign UI Figma TVRI Platform</h3>
                            <p class="text-slate-400 text-sm leading-relaxed">
                                Konsep perancangan antarmuka (wireframing) modern untuk aplikasi streaming & berita TVRI. Memfokuskan kemudahan navigasi jadwal acara siaran langsung dan arsip program TV.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <a href="https://www.figma.com" target="_blank" rel="noopener font-semibold" class="w-full py-2.5 rounded-xl bg-slate-900 border border-slate-700 hover:border-pink-500 text-slate-200 hover:text-white text-xs flex items-center justify-center gap-2 transition-all">
                            <span>Buka Figma Link</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>
                </div>

                <!-- Project 2: Midas M32 & vMix Live Stream -->
                <div class="glass-card rounded-2xl overflow-hidden group border border-slate-800 flex flex-col justify-between">
                    <div>
                        <!-- Project Visual Header -->
                        <div class="relative h-48 bg-slate-900 overflow-hidden flex items-center justify-center border-b border-slate-800">
                            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-transparent to-transparent z-10"></div>
                            <!-- Mockup Graphic Screen -->
                            <div class="w-11/12 h-36 bg-slate-950 rounded-lg border border-cyan-500/30 p-3 shadow-xl transform group-hover:scale-105 transition-transform duration-500 flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-800 pb-2">
                                    <span class="text-[10px] font-bold text-cyan-400 flex items-center gap-1">
                                        <i class="fa-solid fa-sliders"></i> LIVE AUDIO & STREAMING SETUP
                                    </span>
                                    <span class="text-[9px] bg-cyan-950 text-cyan-300 px-1.5 py-0.5 rounded">Studio</span>
                                </div>
                                <div class="flex items-center justify-around my-auto">
                                    <div class="text-center">
                                        <div class="text-cyan-400 text-lg font-bold"><i class="fa-solid fa-microphone"></i></div>
                                        <span class="text-[9px] text-slate-400">M32 Live</span>
                                    </div>
                                    <div class="text-slate-600 text-xs"><i class="fa-solid fa-arrow-right"></i></div>
                                    <div class="text-center">
                                        <div class="text-purple-400 text-lg font-bold"><i class="fa-solid fa-desktop"></i></div>
                                        <span class="text-[9px] text-slate-400">vMix Video</span>
                                    </div>
                                </div>
                                <div class="h-1.5 bg-gradient-to-r from-cyan-500 to-purple-600 rounded"></div>
                            </div>
                        </div>

                        <!-- Details -->
                        <div class="p-6 space-y-3">
                            <div class="flex items-center gap-2 text-xs font-semibold text-cyan-400">
                                <i class="fa-solid fa-tower-broadcast"></i> Live Production
                            </div>
                            <h3 class="text-xl font-bold text-white group-hover:text-cyan-400 transition-colors">Multi-Cam Live Broadcast Setup</h3>
                            <p class="text-slate-400 text-sm leading-relaxed">
                                Pengaturan siaran langsung multi-kamera menggunakan sistem konsol Midas M32 Live dan vMix switcher. Mengatur audio routing 16+ input channel studio secara *real-time*.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <button onclick="openModal('Proyek Live Broadcast', 'Pengaturan teknis siaran ini mencakup instalasi Stage Box Midas DL16, pengolahan equalizer mik vocal live, dan penyampaian sinyal NDI ke vMix switcher tanpa latency untuk kebutuhan siaran TV internet.')" class="w-full py-2.5 rounded-xl bg-slate-900 border border-slate-700 hover:border-cyan-500 text-slate-200 hover:text-white text-xs flex items-center justify-center gap-2 transition-all">
                            <span>Lihat Detail Teknis</span>
                            <i class="fa-solid fa-circle-info text-[10px]"></i>
                        </button>
                    </div>
                </div>

                <!-- Project 3: ENG Camera News Shooting -->
                <div class="glass-card rounded-2xl overflow-hidden group border border-slate-800 flex flex-col justify-between">
                    <div>
                        <!-- Project Visual Header -->
                        <div class="relative h-48 bg-slate-900 overflow-hidden flex items-center justify-center border-b border-slate-800">
                            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-transparent to-transparent z-10"></div>
                            <!-- Mockup Graphic Screen -->
                            <div class="w-11/12 h-36 bg-slate-950 rounded-lg border border-purple-500/30 p-3 shadow-xl transform group-hover:scale-105 transition-transform duration-500 flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-800 pb-2">
                                    <span class="text-[10px] font-bold text-purple-400 flex items-center gap-1">
                                        <i class="fa-solid fa-video"></i> ENG BROADCAST CAM
                                    </span>
                                    <span class="text-[9px] bg-purple-950 text-purple-300 px-1.5 py-0.5 rounded">Video</span>
                                </div>
                                <div class="flex items-center justify-center space-x-2 my-auto">
                                    <i class="fa-solid fa-film text-3xl text-purple-500"></i>
                                </div>
                                <div class="flex justify-between text-[8px] text-slate-500 font-mono">
                                    <span>REC 4K UHD</span>
                                    <span>24 FPS</span>
                                </div>
                            </div>
                        </div>

                        <!-- Details -->
                        <div class="p-6 space-y-3">
                            <div class="flex items-center gap-2 text-xs font-semibold text-purple-400">
                                <i class="fa-solid fa-video"></i> Production
                            </div>
                            <h3 class="text-xl font-bold text-white group-hover:text-cyan-400 transition-colors">Dokumenter Kebudayaan Temanggung</h3>
                            <p class="text-slate-400 text-sm leading-relaxed">
                                Produksi video dokumenter menggunakan teknik rekaman ENG Camera, penataan lighting lapangan, serta penyuntingan akhir di Adobe Premiere Pro & After Effects.
                            </p>
                        </div>
                    </div>

                    <div class="p-6 pt-0">
                        <button onclick="openModal('Dokumenter Temanggung', 'Proyek liputan dokumenter yang mengangkat budaya dan potensi lokal Temanggung. Meliputi proses pengambilan gambar liputan lapangan, wawancara, audio mastering, hingga color grading.')" class="w-full py-2.5 rounded-xl bg-slate-900 border border-slate-700 hover:border-purple-500 text-slate-200 hover:text-white text-xs flex items-center justify-center gap-2 transition-all">
                            <span>Lihat Detail Teknis</span>
                            <i class="fa-solid fa-circle-info text-[10px]"></i>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- HOBI (HOBBIES) SECTION -->
    <section id="hobbies" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        
        <div class="text-center max-w-3xl mx-auto space-y-3 mb-16">
            <h2 class="text-xs font-bold uppercase tracking-widest text-cyan-400">Aktivitas & Minat</h2>
            <p class="text-3xl sm:text-4xl font-extrabold text-white">Hobi & Eksplorasi</p>
            <p class="text-slate-400 text-sm sm:text-base">Kegiatan yang melatih kreativitas, fokus, dan ketelitian saya di luar jam studi siaran.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            
            <!-- Hobby 1: Manual Coffee Brewing -->
            <div class="glass-card rounded-2xl p-8 space-y-6 relative overflow-hidden group">
                <div class="absolute -right-4 -bottom-4 text-slate-800/40 text-9xl font-black group-hover:text-cyan-500/10 transition-colors">
                    <i class="fa-solid fa-mug-hot"></i>
                </div>
                <div class="w-14 h-14 rounded-2xl bg-amber-500/10 border border-amber-500/30 flex items-center justify-center text-amber-400 text-2xl">
                    <i class="fa-solid fa-mug-saucer"></i>
                </div>
                <div class="space-y-2 relative z-10">
                    <span class="text-xs font-semibold text-amber-400 tracking-wider uppercase">Lokal Pride Temanggung</span>
                    <h3 class="text-2xl font-bold text-white">Manual Coffee Brewing</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Mengeksplorasi ekstraksi biji kopi khas <strong class="text-amber-300">Robusta Temanggung</strong> dengan metode seduh manual (V60, AeroPress, & French Press). Mengasah presisi rasio gramasi dan suhu air layaknya *precision audio tuning*.
                    </p>
                </div>
                <div class="flex items-center gap-2 text-xs font-mono text-slate-400 pt-2 border-t border-slate-800">
                    <i class="fa-solid fa-seedling text-amber-400"></i> Robusta Temanggung Specialty
                </div>
            </div>

            <!-- Hobby 2: Street Photography & Cinematography -->
            <div class="glass-card rounded-2xl p-8 space-y-6 relative overflow-hidden group">
                <div class="absolute -right-4 -bottom-4 text-slate-800/40 text-9xl font-black group-hover:text-purple-500/10 transition-colors">
                    <i class="fa-solid fa-camera"></i>
                </div>
                <div class="w-14 h-14 rounded-2xl bg-purple-500/10 border border-purple-500/30 flex items-center justify-center text-purple-400 text-2xl">
                    <i class="fa-solid fa-camera-retro"></i>
                </div>
                <div class="space-y-2 relative z-10">
                    <span class="text-xs font-semibold text-purple-400 tracking-wider uppercase">Visual Storytelling</span>
                    <h3 class="text-2xl font-bold text-white">Street Photography & Cinematography</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Menangkap momen kehidupan jalanan otentik, pencahayaan alami, dan komposisi frame sinematik. Melatih kepekaan mata visual saat mengatur pengambilan gambar siaran studio.
                    </p>
                </div>
                <div class="flex items-center gap-2 text-xs font-mono text-slate-400 pt-2 border-t border-slate-800">
                    <i class="fa-solid fa-eye text-purple-400"></i> Frame & Color Sensitivity
                </div>
            </div>

            <!-- Hobby 3: Tactical Gaming (VALORANT) -->
            <div class="glass-card rounded-2xl p-8 space-y-6 relative overflow-hidden group">
                <div class="absolute -right-4 -bottom-4 text-slate-800/40 text-9xl font-black group-hover:text-red-500/10 transition-colors">
                    <i class="fa-solid fa-gamepad"></i>
                </div>
                <div class="w-14 h-14 rounded-2xl bg-red-500/10 border border-red-500/30 flex items-center justify-center text-red-400 text-2xl">
                    <i class="fa-solid fa-crosshairs"></i>
                </div>
                <div class="space-y-2 relative z-10">
                    <span class="text-xs font-semibold text-red-400 tracking-wider uppercase">Esports & Focus</span>
                    <h3 class="text-2xl font-bold text-white">Tactical Gaming (VALORANT)</h3>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Bermain game taktis seperti <strong class="text-red-400">VALORANT</strong> untuk melatih refleks cepat, komunikasi tim yang presisi di bawah tekanan, serta pengambilan keputusan strategis secara instan.
                    </p>
                </div>
                <div class="flex items-center gap-2 text-xs font-mono text-slate-400 pt-2 border-t border-slate-800">
                    <i class="fa-solid fa-users text-red-400"></i> Communication & Strategy
                </div>
            </div>

        </div>
    </section>

    <!-- KONTAK & LOKASI SECTION -->
    <section id="contact" class="py-20 bg-slate-950/80 border-t border-slate-800/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
                
                <!-- Left Info & Location Box -->
                <div class="lg:col-span-5 space-y-8">
                    <div>
                        <h2 class="text-xs font-bold uppercase tracking-widest text-cyan-400">Mari Terhubung</h2>
                        <h3 class="text-3xl sm:text-4xl font-extrabold text-white mt-2">Hubungi Kontak</h3>
                        <p class="text-slate-400 text-sm mt-3 leading-relaxed">
                            Tertarik untuk berkolaborasi dalam proyek broadcast siaran, produksi video multi-cam, sound engineering, atau diskusi visual UI/UX? Silakan hubungi saya melalui saluran berikut.
                        </p>
                    </div>

                    <!-- Direct Contact Cards -->
                    <div class="space-y-4">
                        
                        <!-- Email Card -->
                        <div class="glass-card p-5 rounded-2xl flex items-center justify-between group">
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 rounded-xl bg-cyan-500/10 border border-cyan-500/30 flex items-center justify-center text-cyan-400 text-xl">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <div class="text-xs text-slate-400 font-medium">Email Resmi</div>
                                    <div class="text-sm sm:text-base font-bold text-white group-hover:text-cyan-400 transition-colors">
                                        ezekiel.jatiputra@gmail.com
                                    </div>
                                </div>
                            </div>
                            <button onclick="copyToClipboard('ezekiel.jatiputra@gmail.com')" class="p-2.5 rounded-lg bg-slate-900 border border-slate-700 hover:border-cyan-500 text-slate-300 hover:text-white text-xs transition-all" title="Salin Email">
                                <i class="fa-regular fa-copy"></i>
                            </button>
                        </div>

                        <!-- Instagram Card -->
                        <a href="https://instagram.com/ezekiel.jatiputra" target="_blank" rel="noopener" class="glass-card p-5 rounded-2xl flex items-center justify-between group block">
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 rounded-xl bg-pink-500/10 border border-pink-500/30 flex items-center justify-center text-pink-400 text-xl">
                                    <i class="fa-brands fa-instagram"></i>
                                </div>
                                <div>
                                    <div class="text-xs text-slate-400 font-medium">Instagram</div>
                                    <div class="text-sm sm:text-base font-bold text-white group-hover:text-pink-400 transition-colors">
                                        @ezekiel.jatiputra
                                    </div>
                                </div>
                            </div>
                            <i class="fa-solid fa-arrow-up-right-from-square text-slate-500 group-hover:text-pink-400 transition-colors text-xs pr-2"></i>
                        </a>

                        <!-- Location Card -->
                        <div class="glass-card p-5 rounded-2xl flex items-center gap-4">
                            <div class="w-12 h-12 rounded-xl bg-emerald-500/10 border border-emerald-500/30 flex items-center justify-center text-emerald-400 text-xl">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <div class="text-xs text-slate-400 font-medium">Domisili & Lokasi</div>
                                <div class="text-sm sm:text-base font-bold text-white">
                                    Temanggung, Jawa Tengah, Indonesia
                                </div>
                            </div>
                        </div>

                    </div>
                </div>

                <!-- Right Quick Interactive Message Form -->
                <div class="lg:col-span-7">
                    <div class="glass-card p-8 rounded-3xl border border-slate-800 space-y-6">
                        <h4 class="text-xl font-bold text-white flex items-center gap-2">
                            <i class="fa-solid fa-paper-plane text-cyan-400 text-lg"></i>
                            Kirim Pesan Langsung
                        </h4>
                        
                        <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                                <div class="space-y-1.5">
                                    <label for="nama" class="text-xs font-semibold text-slate-300">Nama Lengkap</label>
                                    <input type="text" id="nama" required placeholder="Masukkan nama Anda" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 focus:outline-none focus:border-cyan-400 transition-colors">
                                </div>
                                <div class="space-y-1.5">
                                    <label for="email" class="text-xs font-semibold text-slate-300">Alamat Email</label>
                                    <input type="email" id="email" required placeholder="nama@email.com" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 focus:outline-none focus:border-cyan-400 transition-colors">
                                </div>
                            </div>

                            <div class="space-y-1.5">
                                <label for="subjek" class="text-xs font-semibold text-slate-300">Subjek Proyek / Diskusi</label>
                                <input type="text" id="subjek" required placeholder="Contoh: Kolaborasi Audio Engineering / vMix Broadcast" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 focus:outline-none focus:border-cyan-400 transition-colors">
                            </div>

                            <div class="space-y-1.5">
                                <label for="pesan" class="text-xs font-semibold text-slate-300">Isi Pesan</label>
                                <textarea id="pesan" rows="4" required placeholder="Tuliskan detail pesan atau pertanyaan Anda di sini..." class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white placeholder-slate-500 focus:outline-none focus:border-cyan-400 transition-colors resize-none"></textarea>
                            </div>

                            <button type="submit" class="w-full py-3.5 bg-gradient-to-r from-cyan-500 to-indigo-600 hover:opacity-90 text-black font-extrabold rounded-xl text-sm transition-all shadow-lg shadow-cyan-500/20 flex items-center justify-center gap-2">
                                <i class="fa-solid fa-paper-plane"></i> Kirim Pesan Sekarang
                            </button>
                        </form>
                    </div>
                </div>

            </div>

        </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-8 bg-brand-dark border-t border-slate-900 text-slate-500 text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-center sm:text-left">
            <div>
                <p>&copy; <span id="year"></span> Ezekiel Franztio Jatiputra. Hak Cipta Dilindungi.</p>
                <p class="text-slate-600 mt-1">Broadcast Multimedia & Media Production • Temanggung, Jawa Tengah</p>
            </div>
            
            <div class="flex items-center space-x-4 text-base">
                <a href="https://instagram.com/ezekiel.jatiputra" target="_blank" rel="noopener" class="text-slate-400 hover:text-pink-400 transition-colors" title="Instagram">
                    <i class="fa-brands fa-instagram"></i>
                </a>
                <a href="mailto:ezekiel.jatiputra@gmail.com" class="text-slate-400 hover:text-cyan-400 transition-colors" title="Email Direct">
                    <i class="fa-solid fa-envelope"></i>
                </a>
            </div>
        </div>
    </footer>

    <!-- PROJECT DETAIL MODAL -->
    <div id="modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="glass-card max-w-lg w-full rounded-2xl p-6 border border-slate-700 space-y-4 animate-float">
            <div class="flex items-center justify-between border-b border-slate-800 pb-3">
                <h3 id="modal-title" class="text-lg font-bold text-white">Detail Proyek</h3>
                <button onclick="closeModal()" class="text-slate-400 hover:text-white p-1">
                    <i class="fa-solid fa-xmark text-xl"></i>
                </button>
            </div>
            <p id="modal-content" class="text-slate-300 text-sm leading-relaxed">
                Deskripsi teknis...
            </p>
            <div class="pt-2 text-right">
                <button onclick="closeModal()" class="px-5 py-2 rounded-xl bg-cyan-500 text-black font-bold text-xs hover:bg-cyan-400 transition-all">
                    Tutup
                </button>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Set dynamic year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle Logic
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

        // Close mobile menu when clicking any link
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            });
        });

        // Toast Notification Function
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

        // Copy Text to Clipboard Safely
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
                    console.error('Copy fallback failed', error);
                }
                document.body.removeChild(textArea);
            }
            showToast('Email (' + text + ') berhasil disalin!');
        }

        // Contact Form Submission Simulation
        function handleFormSubmit(event) {
            event.preventDefault();
            const nama = document.getElementById('nama').value;
            showToast(`Terima kasih ${nama}, pesan Anda berhasil dikirim!`);
            document.getElementById('contact-form').reset();
        }

        // Modal Logic
        function openModal(title, content) {
            document.getElementById('modal-title').textContent = title;
            document.getElementById('modal-content').textContent = content;
            document.getElementById('modal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('modal');
            if (event.target === modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
