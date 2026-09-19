# crownedbytej.com
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crowned By Tej | Premium Regal Turban & Pagg Tying Services</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts for Regal Typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Cinzel:wght@400;500;600;700;800;900&family=Montserrat:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            950: '#030712',
                            900: '#0a1128',
                            800: '#0f1c3f',
                            700: '#1c2d5a',
                        },
                        burgundy: {
                            950: '#1a0309',
                            900: '#2b040e',
                            800: '#4a0e17',
                            700: '#6b111e',
                        },
                        gold: {
                            100: '#fffbeb',
                            200: '#fef08a',
                            300: '#fde047',
                            400: '#eab308',
                            500: '#d97706',
                            600: '#b45309',
                        }
                    },
                    fontFamily: {
                        brand: ['Cinzel Decorative', 'serif'],
                        heading: ['Cinzel', 'serif'],
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Montserrat', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Metallic Gold Gradient Text */
        .text-gold-metallic {
            background: linear-gradient(135deg, #BF953F 0%, #FCF6BA 25%, #B38728 50%, #FBF5B7 75%, #AA771C 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Gold Shimmer Button Animation */
        @keyframes shimmer {
            0% { background-position: -200% 0; }
            100% { background-position: 200% 0; }
        }

        .shimmer-btn {
            background: linear-gradient(90deg, #B38728 0%, #FBF5B7 50%, #AA771C 100%);
            background-size: 200% 100%;
            animation: shimmer 4s infinite linear;
        }

        /* Subtle Gold Royal Glow */
        .royal-glow {
            box-shadow: 0 0 25px rgba(212, 175, 55, 0.25);
        }

        .royal-glow-hover:hover {
            box-shadow: 0 0 35px rgba(212, 175, 55, 0.45);
            transform: translateY(-2px);
        }

        /* Royal Pattern Background */
        .bg-pattern {
            background-color: #050a18;
            background-image: radial-gradient(rgba(191, 149, 63, 0.1) 1px, transparent 1px);
            background-size: 30px 30px;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0a1128;
        }
        ::-webkit-scrollbar-thumb {
            background: #b38728;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #fcf6ba;
        }
    </style>
</head>
<body class="bg-navy-950 text-slate-200 font-sans antialiased selection:bg-gold-500 selection:text-navy-950 bg-pattern relative">

    <!-- Canvas for Floating Gold Particles -->
    <canvas id="particles-canvas" class="fixed inset-0 pointer-events-none z-0"></canvas>

    <header class="fixed top-0 left-0 right-0 z-50 bg-navy-900/90 backdrop-blur-md border-b border-gold-500/30 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-24">
                
                <!-- Text-Only Wording Brand Name (Strictly No Logo Image) -->
                <a href="#" class="flex flex-col group">
                    <span class="font-brand font-bold text-2xl sm:text-3xl text-gold-metallic tracking-wider drop-shadow-md group-hover:opacity-90 transition">
                        CROWNED BY TEJ
                    </span>
                    <span class="font-heading text-[9px] sm:text-[10px] tracking-[0.38em] text-gold-300 uppercase -mt-1 font-semibold">
                        The Royal Turban Master
                    </span>
                </a>

                <!-- Navigation Links -->
                <nav class="hidden lg:flex items-center space-x-8 font-heading text-xs uppercase tracking-widest text-slate-300 font-medium">
                    <a href="#about" class="hover:text-gold-300 transition-colors">Heritage</a>
                    <a href="#styles" class="hover:text-gold-300 transition-colors">Royal Styles</a>
                    <a href="#estimator" class="hover:text-gold-300 transition-colors">Crown Estimator</a>
                    <a href="#packages" class="hover:text-gold-300 transition-colors">Packages</a>
                    <a href="#testimonials" class="hover:text-gold-300 transition-colors">Reviews</a>
                    <a href="#faq" class="hover:text-gold-300 transition-colors">FAQ</a>
                </nav>

                <!-- CTA Action Button -->
                <div class="hidden sm:block">
                    <a href="#booking" class="shimmer-btn text-navy-950 font-heading font-bold text-xs uppercase tracking-widest px-6 py-3 border border-gold-300 shadow-md hover:scale-105 transition-transform block text-center">
                        Request Crown
                    </a>
                </div>

                <!-- Mobile Navigation Button -->
                <div class="lg:hidden">
                    <button id="mobile-menu-btn" class="text-gold-400 p-2 focus:outline-none" aria-label="Toggle Navigation">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Navigation Menu -->
        <div id="mobile-menu" class="hidden lg:hidden bg-navy-900 border-b border-gold-500/30 px-6 py-6 space-y-4 font-heading text-center text-xs uppercase tracking-widest">
            <a href="#about" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">Heritage</a>
            <a href="#styles" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">Royal Styles</a>
            <a href="#estimator" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">Crown Estimator</a>
            <a href="#packages" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">Packages</a>
            <a href="#testimonials" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">Reviews</a>
            <a href="#faq" class="block py-2 text-slate-200 hover:text-gold-300 mobile-link">FAQ</a>
            <a href="#booking" class="inline-block w-full shimmer-btn text-navy-950 font-bold py-3 mt-2 border border-gold-300 mobile-link">
                Request Crown
            </a>
        </div>
    </header>

    <main class="relative z-10 pt-24">
        <section class="relative min-h-[88vh] flex items-center justify-center overflow-hidden py-20 px-4">
            <!-- Glow Accents -->
            <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[550px] h-[550px] bg-burgundy-800/30 rounded-full blur-[140px] pointer-events-none"></div>
            <div class="absolute top-1/3 right-10 w-[300px] h-[300px] bg-gold-600/15 rounded-full blur-[100px] pointer-events-none"></div>

            <div class="relative max-w-5xl mx-auto text-center z-10 space-y-8">
                <!-- Royal Badge Header -->
                <div class="inline-flex items-center space-x-3 px-5 py-2 rounded-full border border-gold-500/40 bg-navy-900/80 backdrop-blur-md">
                    <span class="w-2 h-2 rounded-full bg-gold-400 animate-pulse"></span>
                    <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-300">The Apex of Regal Grace</span>
                    <span class="w-2 h-2 rounded-full bg-gold-400 animate-pulse"></span>
                </div>

                <!-- Main Title Typography -->
                <h1 class="font-brand text-4xl sm:text-6xl md:text-7xl font-bold tracking-tight text-slate-100 leading-tight">
                    CROWNED BY TEJ
                </h1>

                <!-- Elegant Tagline -->
                <div class="font-serif italic text-2xl sm:text-3xl text-gold-metallic max-w-3xl mx-auto">
                    “Where Sacred Tradition Meets Architectural Royalty”
                </div>

                <!-- Narrative Paragraph -->
                <p class="font-sans text-slate-300 text-sm sm:text-base max-w-2xl mx-auto leading-relaxed font-light">
                    Transforming the traditional Punjabi Pagg into a magnificent crown of royal stature. Symmetrical precision, sharp razor-edge folds (Pech), and regal posture crafted for Grooms, VIPs, and Noble Occasions.
                </p>

                <!-- Action Buttons -->
                <div class="flex flex-col sm:flex-row items-center justify-center gap-5 pt-4">
                    <a href="#estimator" class="w-full sm:w-auto shimmer-btn text-navy-950 font-heading font-bold px-8 py-4 text-xs tracking-widest uppercase border border-gold-200 royal-glow-hover transition-all">
                        Customize Your Crown
                    </a>
                    <a href="#styles" class="w-full sm:w-auto bg-navy-800/80 hover:bg-navy-700 text-gold-300 font-heading font-semibold px-8 py-4 text-xs tracking-widest uppercase border border-gold-500/40 hover:border-gold-400 transition-all backdrop-blur-md">
                        Explore Royal Styles
                    </a>
                </div>

                <!-- Key Metrics -->
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6 pt-12 border-t border-gold-500/20 max-w-4xl mx-auto">
                    <div class="p-3">
                        <div class="font-heading text-3xl font-bold text-gold-metallic">1,200+</div>
                        <div class="font-sans text-[11px] tracking-wider uppercase text-slate-400 mt-1">Grooms Crowned</div>
                    </div>
                    <div class="p-3">
                        <div class="font-heading text-3xl font-bold text-gold-metallic">100%</div>
                        <div class="font-sans text-[11px] tracking-wider uppercase text-slate-400 mt-1">Symmetrical Precision</div>
                    </div>
                    <div class="p-3">
                        <div class="font-heading text-3xl font-bold text-gold-metallic">15+</div>
                        <div class="font-sans text-[11px] tracking-wider uppercase text-slate-400 mt-1">Years of Mastery</div>
                    </div>
                    <div class="p-3">
                        <div class="font-heading text-3xl font-bold text-gold-metallic">VIP</div>
                        <div class="font-sans text-[11px] tracking-wider uppercase text-slate-400 mt-1">Concierge Service</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="about" class="py-24 bg-navy-900/60 border-y border-gold-500/20 relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                    
                    <!-- Left Decorative Royal Frame -->
                    <div class="lg:col-span-5 relative">
                        <div class="p-8 sm:p-12 border-2 border-gold-500/40 bg-burgundy-950/60 backdrop-blur-md relative shadow-2xl">
                            <!-- Corner Accents -->
                            <div class="absolute -top-3 -left-3 w-6 h-6 border-t-2 border-l-2 border-gold-300"></div>
                            <div class="absolute -top-3 -right-3 w-6 h-6 border-t-2 border-r-2 border-gold-300"></div>
                            <div class="absolute -bottom-3 -left-3 w-6 h-6 border-b-2 border-l-2 border-gold-300"></div>
                            <div class="absolute -bottom-3 -right-3 w-6 h-6 border-b-2 border-r-2 border-gold-300"></div>

                            <span class="font-heading text-xs tracking-[0.4em] text-gold-400 uppercase block mb-2">Our Sacred Philosophy</span>
                            <h3 class="font-brand text-2xl sm:text-3xl font-bold text-slate-100 mb-6">Perfection in Every Fold</h3>
                            
                            <p class="text-slate-300 font-sans text-xs sm:text-sm leading-relaxed mb-6 font-light">
                                In royal Punjabi culture, a turban is not merely fabric—it is an emblem of royalty, dignity, honor, and sovereign grace. At Crowned By Tej, every turban is meticulously architecturalized to complement your facial structure and attire.
                            </p>
                            
                            <div class="space-y-4 border-t border-gold-500/20 pt-6">
                                <div class="flex items-start space-x-3">
                                    <i class="fa-solid fa-gem text-gold-400 mt-1 text-sm"></i>
                                    <div>
                                        <h4 class="font-heading text-xs font-bold text-slate-200 uppercase tracking-wider">Tailored Crown Contours</h4>
                                        <p class="text-[11px] text-slate-400">Sculpted to enhance facial symmetry and posture.</p>
                                    </div>
                                </div>
                                <div class="flex items-start space-x-3">
                                    <i class="fa-solid fa-shield-halved text-gold-400 mt-1 text-sm"></i>
                                    <div>
                                        <h4 class="font-heading text-xs font-bold text-slate-200 uppercase tracking-wider">All-Day Structural Integrity</h4>
                                        <p class="text-[11px] text-slate-400">Guaranteed firmness from morning Anand Karaj to midnight celebrations.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Right Narrative Column -->
                    <div class="lg:col-span-7 space-y-6">
                        <div>
                            <span class="font-heading text-xs uppercase tracking-[0.3em] text-gold-400 font-semibold">Master Artisan</span>
                            <h2 class="font-heading text-3xl sm:text-4xl lg:text-5xl font-bold text-slate-100 mt-1">
                                Royal Craftsmanship & Heritage
                            </h2>
                        </div>

                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed font-light">
                            Tej Singh has spent over 15 years mastering the rare art of classic and modern turban geometry. Having tied crowns for international grooms, high-profile galas, and VIP functions across the globe, his signature technique produces razor-sharp layers, balanced heights, and royal poise.
                        </p>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 pt-2">
                            <div class="bg-navy-950/70 p-6 border border-gold-500/20">
                                <i class="fa-solid fa-crown text-2xl text-gold-400 mb-3 block"></i>
                                <h4 class="font-heading text-sm font-bold text-slate-200 mb-1 uppercase tracking-wider">Noble Aesthetics</h4>
                                <p class="text-xs text-slate-400 leading-relaxed">
                                    Calibrated folds to ensure a monarchical stance and camera-ready angle from 360 degrees.
                                </p>
                            </div>
                            <div class="bg-navy-950/70 p-6 border border-gold-500/20">
                                <i class="fa-solid fa-wand-magic-sparkles text-2xl text-gold-400 mb-3 block"></i>
                                <h4 class="font-heading text-sm font-bold text-slate-200 mb-1 uppercase tracking-wider">Accessory Integration</h4>
                                <p class="text-xs text-slate-400 leading-relaxed">
                                    Seamless placement of jeweled Kalgis, royal Sehras, and pearl strands without compromising stability.
                                </p>
                            </div>
                        </div>

                        <div class="pt-4">
                            <blockquote class="border-l-2 border-gold-400 pl-4 italic text-slate-300 font-serif text-base sm:text-lg">
                                “A turban is not placed upon your head; it is sculpted upon it with reverence, precision, and majesty.”
                                <footer class="text-xs font-heading not-italic text-gold-400 mt-2 uppercase tracking-widest">— Tej Singh</footer>
                            </blockquote>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <section id="styles" class="py-24 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-12 space-y-4">
                <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-400 font-semibold">Gallery of Folds</span>
                <h2 class="font-heading text-3xl sm:text-5xl font-bold text-slate-100">Interactive Royal Styles</h2>
                <div class="w-24 h-0.5 bg-gradient-to-r from-transparent via-gold-400 to-transparent mx-auto"></div>
                <p class="text-slate-300 text-xs sm:text-sm font-light">
                    Explore our signature crown styles. Filter by occasion to discover the ideal geometry for your royal persona.
                </p>
            </div>

            <!-- Filter Category Tabs -->
            <div class="flex flex-wrap items-center justify-center gap-3 mb-12" id="style-filters">
                <button onclick="filterStyles('all')" class="filter-btn active font-heading text-xs uppercase tracking-widest px-5 py-2.5 border border-gold-400 bg-burgundy-900/80 text-gold-200 transition">
                    All Styles
                </button>
                <button onclick="filterStyles('groom')" class="filter-btn font-heading text-xs uppercase tracking-widest px-5 py-2.5 border border-slate-700 bg-navy-900/60 text-slate-300 hover:border-gold-400 transition">
                    Groom Specials
                </button>
                <button onclick="filterStyles('classic')" class="filter-btn font-heading text-xs uppercase tracking-widest px-5 py-2.5 border border-slate-700 bg-navy-900/60 text-slate-300 hover:border-gold-400 transition">
                    Classic Royal
                </button>
                <button onclick="filterStyles('modern')" class="filter-btn font-heading text-xs uppercase tracking-widest px-5 py-2.5 border border-slate-700 bg-navy-900/60 text-slate-300 hover:border-gold-400 transition">
                    Modern Sharp
                </button>
            </div>

            <!-- Style Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="styles-container">
                <!-- Javascript will inject dynamic style cards -->
            </div>
        </section>

        <section id="estimator" class="py-24 bg-gradient-to-b from-navy-900 via-navy-950 to-navy-900 border-t border-gold-500/30">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                
                <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
                    <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-400 font-semibold">Bespoke Planning</span>
                    <h2 class="font-heading text-3xl sm:text-5xl font-bold text-slate-100">Crown Estimator Calculator</h2>
                    <p class="text-slate-300 text-xs sm:text-sm font-light">
                        Customize your royal session details below to generate an instant estimate and transfer it directly to your reservation form.
                    </p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 bg-navy-950/90 border border-gold-500/40 p-6 sm:p-10 shadow-2xl relative">
                    
                    <!-- Left: Customization Options -->
                    <div class="lg:col-span-8 space-y-8">
                        
                        <!-- 1. Occasion Stature -->
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-widest mb-4">
                                1. Select Occasion Stature
                            </label>
                            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                                <button type="button" onclick="selectOccasion('groom', 180)" class="occasion-btn active p-4 border border-gold-500 bg-burgundy-900/60 text-center hover:border-gold-300 transition text-xs font-heading uppercase tracking-wider text-slate-100">
                                    <i class="fa-solid fa-crown text-gold-400 text-xl block mb-2"></i>
                                    Royal Groom
                                </button>
                                <button type="button" onclick="selectOccasion('barati', 75)" class="occasion-btn p-4 border border-slate-700 bg-navy-900/60 text-center hover:border-gold-300 transition text-xs font-heading uppercase tracking-wider text-slate-300">
                                    <i class="fa-solid fa-user-tie text-slate-400 text-xl block mb-2"></i>
                                    Barat / Family
                                </button>
                                <button type="button" onclick="selectOccasion('executive', 85)" class="occasion-btn p-4 border border-slate-700 bg-navy-900/60 text-center hover:border-gold-300 transition text-xs font-heading uppercase tracking-wider text-slate-300">
                                    <i class="fa-solid fa-building text-slate-400 text-xl block mb-2"></i>
                                    Executive Formal
                                </button>
                                <button type="button" onclick="selectOccasion('vip', 220)" class="occasion-btn p-4 border border-slate-700 bg-navy-900/60 text-center hover:border-gold-300 transition text-xs font-heading uppercase tracking-wider text-slate-300">
                                    <i class="fa-solid fa-star text-slate-400 text-xl block mb-2"></i>
                                    Gala VIP Concierge
                                </button>
                            </div>
                        </div>

                        <!-- 2. Fabric Choice -->
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-widest mb-4">
                                2. Select Fabric Grade
                            </label>
                            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                                <label class="cursor-pointer p-4 border border-gold-500/60 bg-navy-900/60 flex flex-col justify-between hover:border-gold-400">
                                    <input type="radio" name="fabric" value="Full Voile" checked onchange="updateEstimator()" class="sr-only">
                                    <div>
                                        <span class="font-heading text-xs text-slate-100 font-bold block uppercase tracking-wider">Full Voile</span>
                                        <span class="text-[11px] text-slate-400 font-light block mt-1">Lightweight, crisp layers, classic drape.</span>
                                    </div>
                                    <span class="text-xs text-gold-400 font-semibold mt-3 block">Included</span>
                                </label>
                                <label class="cursor-pointer p-4 border border-slate-700 bg-navy-900/60 flex flex-col justify-between hover:border-gold-400">
                                    <input type="radio" name="fabric" value="Rubia Heavy" onchange="updateEstimator()" class="sr-only">
                                    <div>
                                        <span class="font-heading text-xs text-slate-100 font-bold block uppercase tracking-wider">Rubia Heavy</span>
                                        <span class="text-[11px] text-slate-400 font-light block mt-1">Higher thread density, bold firmness.</span>
                                    </div>
                                    <span class="text-xs text-gold-400 font-semibold mt-3 block">+$15</span>
                                </label>
                                <label class="cursor-pointer p-4 border border-slate-700 bg-navy-900/60 flex flex-col justify-between hover:border-gold-400">
                                    <input type="radio" name="fabric" value="Malmal Soft Royal" onchange="updateEstimator()" class="sr-only">
                                    <div>
                                        <span class="font-heading text-xs text-slate-100 font-bold block uppercase tracking-wider">Malmal Soft Royal</span>
                                        <span class="text-[11px] text-slate-400 font-light block mt-1">Ultra-delicate luxury heritage touch.</span>
                                    </div>
                                    <span class="text-xs text-gold-400 font-semibold mt-3 block">+$20</span>
                                </label>
                            </div>
                        </div>

                        <!-- 3. Palette Theme & Person Count -->
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                            <div>
                                <label class="block font-heading text-xs text-gold-300 uppercase tracking-widest mb-3">
                                    3. Royal Palette Theme
                                </label>
                                <select id="color-palette" onchange="updateEstimator()" class="w-full bg-navy-900 border border-gold-500/40 text-slate-200 text-xs font-sans p-3 focus:outline-none focus:border-gold-300">
                                    <option value="Royal Burgundy & Gold Accent">Royal Burgundy & Gold Accent</option>
                                    <option value="Imperial Deep Navy & Silver">Imperial Deep Navy & Silver</option>
                                    <option value="Monarch Emerald Green">Monarch Emerald Green</option>
                                    <option value="Pristine Ivory Pearl">Pristine Ivory Pearl</option>
                                    <option value="Maharaja Crimson Red">Maharaja Crimson Red</option>
                                    <option value="Custom Bespoke Color Match">Custom Bespoke Color Match (+$30)</option>
                                </select>
                            </div>

                            <div>
                                <label class="block font-heading text-xs text-gold-300 uppercase tracking-widest mb-3">
                                    4. Number of Heads to Crown
                                </label>
                                <div class="flex items-center space-x-3">
                                    <button type="button" onclick="adjustHeadCount(-1)" class="w-10 h-10 border border-gold-500/40 bg-navy-900 text-gold-300 hover:bg-gold-500/20 font-bold text-base">-</button>
                                    <span id="head-count" class="font-heading text-lg font-bold text-slate-100 w-10 text-center">1</span>
                                    <button type="button" onclick="adjustHeadCount(1)" class="w-10 h-10 border border-gold-500/40 bg-navy-900 text-gold-300 hover:bg-gold-500/20 font-bold text-base">+</button>
                                    <span class="text-xs text-slate-400 ml-2">Person(s)</span>
                                </div>
                            </div>
                        </div>

                        <!-- 4. Royal Accessories -->
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-widest mb-3">
                                5. Royal Ornaments & Add-Ons
                            </label>
                            <div class="space-y-2">
                                <label class="flex items-center space-x-3 text-xs text-slate-300 cursor-pointer">
                                    <input type="checkbox" id="acc-kalgi" onchange="updateEstimator()" class="rounded border-gold-500/40 text-gold-500 focus:ring-0">
                                    <span>Jeweled Royal Kalgi Placement & Balance (+$25)</span>
                                </label>
                                <label class="flex items-center space-x-3 text-xs text-slate-300 cursor-pointer">
                                    <input type="checkbox" id="acc-sehra" onchange="updateEstimator()" class="rounded border-gold-500/40 text-gold-500 focus:ring-0">
                                    <span>Groom Sehra / Pearl Strings Attachment (+$20)</span>
                                </label>
                                <label class="flex items-center space-x-3 text-xs text-slate-300 cursor-pointer">
                                    <input type="checkbox" id="acc-reception" onchange="updateEstimator()" class="rounded border-gold-500/40 text-gold-500 focus:ring-0">
                                    <span>On-Site Reception Restyle & Evening Touch-Up (+$90)</span>
                                </label>
                            </div>
                        </div>

                    </div>

                    <!-- Right: Summary Price Output Card -->
                    <div class="lg:col-span-4 bg-burgundy-950/60 border border-gold-500/50 p-6 flex flex-col justify-between relative shadow-xl">
                        <div class="space-y-6">
                            <div class="border-b border-gold-500/30 pb-4">
                                <span class="font-heading text-[10px] text-gold-400 uppercase tracking-widest block">Estimated Royal Package</span>
                                <div id="total-price" class="font-heading text-4xl font-bold text-gold-metallic mt-1">$180</div>
                                <p class="text-[11px] text-slate-400 mt-1">Includes custom starching, precision tying & style lock.</p>
                            </div>

                            <div class="space-y-3 text-xs font-sans">
                                <div class="flex justify-between text-slate-300">
                                    <span>Base Stature:</span>
                                    <span id="summary-occasion" class="font-semibold text-slate-100">Royal Groom</span>
                                </div>
                                <div class="flex justify-between text-slate-300">
                                    <span>Fabric Grade:</span>
                                    <span id="summary-fabric" class="font-semibold text-slate-100">Full Voile</span>
                                </div>
                                <div class="flex justify-between text-slate-300">
                                    <span>Color Theme:</span>
                                    <span id="summary-color" class="font-semibold text-slate-100">Burgundy & Gold</span>
                                </div>
                                <div class="flex justify-between text-slate-300">
                                    <span>Head Count:</span>
                                    <span id="summary-count" class="font-semibold text-slate-100">1 Person</span>
                                </div>
                                <div class="flex justify-between text-slate-300 border-t border-gold-500/20 pt-2">
                                    <span>Add-ons Total:</span>
                                    <span id="summary-addons" class="font-semibold text-gold-400">$0</span>
                                </div>
                            </div>

                            <div class="bg-navy-950 p-3 border border-gold-500/30 text-[11px] text-slate-400 leading-relaxed">
                                <i class="fa-solid fa-clock text-gold-400 mr-1.5"></i>
                                Est. Tying Time: <strong id="summary-time" class="text-slate-200">45 - 60 mins</strong>
                            </div>
                        </div>

                        <div class="pt-6">
                            <a href="#booking" onclick="transferEstimateToBooking()" class="w-full shimmer-btn text-navy-950 font-heading font-bold text-xs uppercase tracking-widest py-3 border border-gold-200 text-center block">
                                Lock In This Estimate
                            </a>
                        </div>
                    </div>

                </div>

            </div>
        </section>

        <section id="packages" class="py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
                <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-400 font-semibold">Tiered Curations</span>
                <h2 class="font-heading text-3xl sm:text-5xl font-bold text-slate-100">Royal Service Packages</h2>
                <div class="w-24 h-0.5 bg-gradient-to-r from-transparent via-gold-400 to-transparent mx-auto"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">
                
                <!-- Package 1 -->
                <div class="bg-navy-900/60 border border-gold-500/20 p-8 flex flex-col justify-between hover:border-gold-500/50 transition">
                    <div class="space-y-6">
                        <div>
                            <span class="font-heading text-xs tracking-widest text-gold-400 uppercase">Single Executive</span>
                            <h3 class="font-heading text-2xl font-bold text-slate-100 mt-1">Signature Session</h3>
                            <div class="text-3xl font-bold text-slate-100 mt-3 font-heading">$120 <span class="text-xs text-slate-400 font-normal">/ session</span></div>
                        </div>
                        <ul class="space-y-3 text-xs text-slate-300 border-t border-gold-500/20 pt-6">
                            <li class="flex items-center"><i class="fa-solid fa-check text-gold-400 mr-3"></i> 1-on-1 bespoke styling session</li>
                            <li class="flex items-center"><i class="fa-solid fa-check text-gold-400 mr-3"></i> Choice of Amritsari, Wattan, or Pochvi style</li>
                            <li class="flex items-center"><i class="fa-solid fa-check text-gold-400 mr-3"></i> Fabric steaming & symmetry alignment</li>
                            <li class="flex items-center"><i class="fa-solid fa-check text-gold-400 mr-3"></i> Beard alignment styling check</li>
                        </ul>
                    </div>
                    <a href="#booking" class="mt-8 block text-center border border-gold-500/40 text-gold-300 font-heading text-xs uppercase tracking-widest py-3 hover:bg-gold-500/10 transition">
                        Select Signature
                    </a>
                </div>

                <!-- Package 2 (Featured Groom Package) -->
                <div class="bg-burgundy-950/70 border-2 border-gold-400 p-8 flex flex-col justify-between relative shadow-2xl royal-glow">
                    <div class="absolute -top-3.5 left-1/2 -translate-x-1/2 bg-gold-400 text-navy-950 font-heading text-[10px] font-bold uppercase tracking-widest px-4 py-1">
                        Most Requested
                    </div>
                    <div class="space-y-6">
                        <div>
                            <span class="font-heading text-xs tracking-widest text-gold-300 uppercase">Groom's Crown</span>
                            <h3 class="font-heading text-2xl font-bold text-slate-100 mt-1">Wedding Groom Crown</h3>
                            <div class="text-3xl font-bold text-gold-metallic mt-3 font-heading">$260 <span class="text-xs text-slate-300 font-normal">/ complete wedding day</span></div>
                        </div>
                        <ul class="space-y-3 text-xs text-slate-200 border-t border-gold-500/30 pt-6">
                            <li class="flex items-center"><i class="fa-solid fa-crown text-gold-400 mr-3"></i> Master Groom Royal Patiala / Wattan Crown</li>
                            <li class="flex items-center"><i class="fa-solid fa-gem text-gold-400 mr-3"></i> Kalgi, Sehra & Pearl Strand Attachment</li>
                            <li class="flex items-center"><i class="fa-solid fa-shirt text-gold-400 mr-3"></i> Premium Starching & Steaming Preparation</li>
                            <li class="flex items-center"><i class="fa-solid fa-user-plus text-gold-400 mr-3"></i> Includes 1 Assistant Tyer for Father/Brother</li>
                            <li class="flex items-center"><i class="fa-solid fa-car text-gold-400 mr-3"></i> On-location venue travel included</li>
                        </ul>
                    </div>
                    <a href="#booking" class="mt-8 block text-center shimmer-btn text-navy-950 font-heading text-xs font-bold uppercase tracking-widest py-3.5 border border-gold-200">
                        Reserve Groom Crown
                    </a>
                </div>

                <!-- Package 3 -->
                <div class="bg-navy-900/60 border border-gold-500/20 p-8 flex flex-col justify-between hover:border-gold-500/50 transition">
                    <div class="space-y-6">
                        <div>
                            <span class="font-heading text-xs tracking-widest text-gold-400 uppercase">Barat & Entourage</span>
                            <h3 class="font-heading text-2xl font-bold text-slate-100 mt-1">Royal Barat Group</h3>
                            <div class="text-3xl font-bold text-slate-100 mt-3 font-heading">$480 <span class="text-xs text-slate-400 font-normal">/ up to 5 people</span></div>
                        </div>
                        <ul class="space-y-3 text-xs text-slate-300 border-t border-gold-500/20 pt-6">
                            <li class="flex items-center"><i class="fa-solid fa-users text-gold-400 mr-3"></i> Complete styling for 5 groomsmen / baratis</li>
                            <li class="flex items-center"><i class="fa-solid fa-palette text-gold-400 mr-3"></i> Color-coordinated matching symmetry</li>
                            <li class="flex items-center"><i class="fa-solid fa-user-group text-gold-400 mr-3"></i> 2 Master Tyers dispatched on-location</li>
                            <li class="flex items-center"><i class="fa-solid fa-plus text-gold-400 mr-3"></i> Extra persons at discounted rate ($80/ea)</li>
                        </ul>
                    </div>
                    <a href="#booking" class="mt-8 block text-center border border-gold-500/40 text-gold-300 font-heading text-xs uppercase tracking-widest py-3 hover:bg-gold-500/10 transition">
                        Reserve Barat Group
                    </a>
                </div>

            </div>
        </section>

        <section id="testimonials" class="py-24 bg-navy-900/40 border-y border-gold-500/20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
                    <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-400 font-semibold">Client Praise</span>
                    <h2 class="font-heading text-3xl sm:text-5xl font-bold text-slate-100">Words of Royalty</h2>
                    <p class="text-slate-300 text-xs sm:text-sm font-light">
                        Hear from grooms and VIPs who experienced the distinction of Crowned By Tej.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="bg-navy-950 p-8 border border-gold-500/30 relative flex flex-col justify-between">
                        <i class="fa-solid fa-quote-left text-gold-500/20 text-5xl absolute top-4 right-4"></i>
                        <p class="text-slate-300 text-xs sm:text-sm font-light leading-relaxed italic relative z-10 mb-6">
                            “Tej converted my wedding morning into a royal experience. The Patiala Shahi crown he sculpted was so comfortable and sharp that it remained flawless through 14 hours of festivities.”
                        </p>
                        <div>
                            <div class="font-heading text-xs font-bold text-gold-300 uppercase tracking-wider">Harpreet S. Dhillon</div>
                            <div class="text-[10px] text-slate-400 uppercase tracking-widest font-heading mt-0.5">Royal Groom • Vancouver</div>
                        </div>
                    </div>

                    <div class="bg-navy-950 p-8 border border-gold-500/30 relative flex flex-col justify-between">
                        <i class="fa-solid fa-quote-left text-gold-500/20 text-5xl absolute top-4 right-4"></i>
                        <p class="text-slate-300 text-xs sm:text-sm font-light leading-relaxed italic relative z-10 mb-6">
                            “We reserved Crowned By Tej for our groomsmen squad of 8. The speed, razor-sharp symmetry, and regal coordination left our guests in absolute awe.”
                        </p>
                        <div>
                            <div class="font-heading text-xs font-bold text-gold-300 uppercase tracking-wider">Gurjot S. & Entourage</div>
                            <div class="text-[10px] text-slate-400 uppercase tracking-widest font-heading mt-0.5">Barat Group • Surrey</div>
                        </div>
                    </div>

                    <div class="bg-navy-950 p-8 border border-gold-500/30 relative flex flex-col justify-between">
                        <i class="fa-solid fa-quote-left text-gold-500/20 text-5xl absolute top-4 right-4"></i>
                        <p class="text-slate-300 text-xs sm:text-sm font-light leading-relaxed italic relative z-10 mb-6">
                            “The sharpness of Tej’s Wattan Wali style is unmatched anywhere else. He knows exactly how to position the crown to frame your face and posture perfectly.”
                        </p>
                        <div>
                            <div class="font-heading text-xs font-bold text-gold-300 uppercase tracking-wider">Navdeep S. Grewal</div>
                            <div class="text-[10px] text-slate-400 uppercase tracking-widest font-heading mt-0.5">Executive Gala Client</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="faq" class="py-24 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 space-y-4">
                <span class="font-heading text-xs tracking-[0.3em] uppercase text-gold-400 font-semibold">Clarifications</span>
                <h2 class="font-heading text-3xl sm:text-5xl font-bold text-slate-100">Frequently Asked Questions</h2>
                <div class="w-24 h-0.5 bg-gradient-to-r from-transparent via-gold-400 to-transparent mx-auto"></div>
            </div>

            <div class="space-y-4" id="faq-accordion">
                <!-- FAQ Item 1 -->
                <div class="border border-gold-500/30 bg-navy-900/60 overflow-hidden">
                    <button onclick="toggleFaq(1)" class="w-full p-5 text-left font-heading text-sm font-bold text-slate-200 flex justify-between items-center hover:text-gold-300 transition">
                        <span>How far in advance should I book for my wedding?</span>
                        <i id="faq-icon-1" class="fa-solid fa-chevron-down text-gold-400 transition-transform"></i>
                    </button>
                    <div id="faq-ans-1" class="hidden px-5 pb-5 text-xs text-slate-300 font-light leading-relaxed border-t border-gold-500/10 pt-3">
                        We recommend reserving your booking 3 to 6 months in advance for peak wedding seasons (Spring/Summer). However, feel free to submit a reservation request for last-minute dates and we will do our best to accommodate your royal schedule.
                    </div>
                </div>

                <!-- FAQ Item 2 -->
                <div class="border border-gold-500/30 bg-navy-900/60 overflow-hidden">
                    <button onclick="toggleFaq(2)" class="w-full p-5 text-left font-heading text-sm font-bold text-slate-200 flex justify-between items-center hover:text-gold-300 transition">
                        <span>Do you provide fabric and starching, or do I bring my own?</span>
                        <i id="faq-icon-2" class="fa-solid fa-chevron-down text-gold-400 transition-transform"></i>
                    </button>
                    <div id="faq-ans-2" class="hidden px-5 pb-5 text-xs text-slate-300 font-light leading-relaxed border-t border-gold-500/10 pt-3">
                        We offer both choices! We can bring pre-starched, premium Full Voile or Rubia fabric matching your color palette, or we can expertly prepare, steam, and starch fabric that you supply.
                    </div>
                </div>

                <!-- FAQ Item 3 -->
                <div class="border border-gold-500/30 bg-navy-900/60 overflow-hidden">
                    <button onclick="toggleFaq(3)" class="w-full p-5 text-left font-heading text-sm font-bold text-slate-200 flex justify-between items-center hover:text-gold-300 transition">
                        <span>Can Tej travel to destination weddings outside the local region?</span>
                        <i id="faq-icon-3" class="fa-solid fa-chevron-down text-gold-400 transition-transform"></i>
                    </button>
                    <div id="faq-ans-3" class="hidden px-5 pb-5 text-xs text-slate-300 font-light leading-relaxed border-t border-gold-500/10 pt-3">
                        Yes. Tej regularly travels worldwide for destination weddings and elite galas. Travel and lodging arrangements are calculated into a bespoke concierge package.
                    </div>
                </div>

                <!-- FAQ Item 4 -->
                <div class="border border-gold-500/30 bg-navy-900/60 overflow-hidden">
                    <button onclick="toggleFaq(4)" class="w-full p-5 text-left font-heading text-sm font-bold text-slate-200 flex justify-between items-center hover:text-gold-300 transition">
                        <span>How long does a Groom royal turban tying session take?</span>
                        <i id="faq-icon-4" class="fa-solid fa-chevron-down text-gold-400 transition-transform"></i>
                    </button>
                    <div id="faq-ans-4" class="hidden px-5 pb-5 text-xs text-slate-300 font-light leading-relaxed border-t border-gold-500/10 pt-3">
                        A typical groom session takes 35 to 45 minutes, allowing ample time for fabric preparation, posture calibration, and jeweled Kalgi/Sehra attachment without rushing your big morning.
                    </div>
                </div>
            </div>
        </section>

        <section id="booking" class="py-24 max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-navy-900 border-2 border-gold-500/40 p-8 sm:p-12 shadow-2xl relative">
                
                <div class="text-center space-y-3 mb-10">
                    <span class="font-heading text-xs tracking-[0.4em] uppercase text-gold-400 font-semibold">Reserve Your Crown</span>
                    <h2 class="font-brand text-3xl sm:text-4xl text-slate-100 font-bold">Royal Reservation Form</h2>
                    <p class="text-slate-300 text-xs sm:text-sm font-light">
                        Submit your event details to request calendar availability and confirm your crown reservation.
                    </p>
                </div>

                <form id="royal-reservation-form" onsubmit="handleReservationSubmit(event)" class="space-y-6">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Full Name *</label>
                            <input type="text" required placeholder="e.g. Amarpreet Singh" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                        </div>
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Phone / WhatsApp *</label>
                            <input type="tel" required placeholder="+1 (555) 000-0000" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Email Address *</label>
                            <input type="email" required placeholder="royal.client@example.com" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                        </div>
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Event Date *</label>
                            <input type="date" required class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Venue Location / City</label>
                            <input type="text" placeholder="e.g. Surrey, BC / Grand Palace Hotel" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                        </div>
                        <div>
                            <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Preferred Tying Style</label>
                            <select id="form-style" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300">
                                <option value="Royal Patiala Shahi">Royal Patiala Shahi</option>
                                <option value="Modern Wattan Wali">Modern Wattan Wali</option>
                                <option value="Executive Amritsari">Executive Amritsari</option>
                                <option value="Classic Royal Pochvi">Classic Royal Pochvi</option>
                                <option value="Wedding Groom Crown">Wedding Groom Crown</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <label class="block font-heading text-xs text-gold-300 uppercase tracking-wider mb-2">Selected Package or Custom Notes</label>
                        <textarea id="form-details" rows="3" class="w-full bg-navy-950 border border-gold-500/40 p-3 text-xs text-slate-100 focus:outline-none focus:border-gold-300" placeholder="Specify color theme, accessory requirements, or estimator summary..."></textarea>
                    </div>

                    <div class="text-center pt-4">
                        <button type="submit" class="w-full sm:w-auto shimmer-btn text-navy-950 font-heading font-bold text-xs uppercase tracking-widest px-12 py-4 border border-gold-200 royal-glow-hover transition">
                            Submit Royal Request
                        </button>
                    </div>
                </form>

            </div>
        </section>
    </main>

    <div id="booking-modal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-navy-950/90 backdrop-blur-md hidden">
        <div class="bg-navy-900 border-2 border-gold-400 p-8 sm:p-10 max-w-md w-full text-center relative shadow-2xl royal-glow">
            <i class="fa-solid fa-crown text-gold-400 text-5xl mb-4 block"></i>
            <h3 class="font-brand text-2xl font-bold text-slate-100 mb-2">Request Transmitted</h3>
            <p class="text-xs text-slate-300 leading-relaxed font-light mb-6">
                Your reservation details have been delivered to Tej Singh. You will receive a personal phone call and WhatsApp confirmation within 24 hours.
            </p>
            <button onclick="closeModal()" class="w-full shimmer-btn text-navy-950 font-heading font-bold text-xs uppercase tracking-widest py-3 border border-gold-200">
                Return To Palace
            </button>
        </div>
    </div>

    <footer class="bg-navy-950 border-t border-gold-500/30 py-16 text-slate-400 text-xs relative z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-10">
            
            <div class="space-y-4">
                <span class="font-brand font-bold text-xl text-gold-metallic tracking-wider block">
                    CROWNED BY TEJ
                </span>
                <p class="text-slate-400 font-light leading-relaxed">
                    Honoring and preserving the sacred tradition of Punjabi crown styling through unmatched precision, luxury fabrics, and monarchical elegance.
                </p>
            </div>

            <div>
                <h4 class="font-heading text-xs text-gold-300 uppercase tracking-widest mb-4">Navigation</h4>
                <ul class="space-y-2 font-heading text-[11px]">
                    <li><a href="#about" class="hover:text-gold-400">Heritage & Craftsmanship</a></li>
                    <li><a href="#styles" class="hover:text-gold-400">Interactive Style Showcase</a></li>
                    <li><a href="#estimator" class="hover:text-gold-400">Crown Estimator</a></li>
                    <li><a href="#packages" class="hover:text-gold-400">Royal Service Packages</a></li>
                </ul>
            </div>

            <div>
                <h4 class="font-heading text-xs text-gold-300 uppercase tracking-widest mb-4">Service Concierge</h4>
                <ul class="space-y-2">
                    <li>Greater Vancouver & Fraser Valley</li>
                    <li>Surrey • Abbotsford • Vancouver</li>
                    <li>Destination Weddings Worldwide</li>
                </ul>
            </div>

            <div>
                <h4 class="font-heading text-xs text-gold-300 uppercase tracking-widest mb-4">Direct Communication</h4>
                <ul class="space-y-2">
                    <li class="flex items-center"><i class="fa-solid fa-phone text-gold-400 mr-2"></i> +1 (604) 555-PAGG</li>
                    <li class="flex items-center"><i class="fa-solid fa-envelope text-gold-400 mr-2"></i> concierge@crownedbytej.com</li>
                    <li class="flex items-center"><i class="fa-brands fa-instagram text-gold-400 mr-2"></i> @CrownedByTej</li>
                </ul>
            </div>

        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-8 border-t border-gold-500/10 flex flex-col sm:flex-row items-center justify-between text-slate-500">
            <p>© 2026 Crowned By Tej. All Rights Reserved. The Royal Art of Crown Creation.</p>
            <p class="mt-2 sm:mt-0 font-heading text-[10px] tracking-widest text-gold-400/80">ROYAL DIGNITY • PERFECTION IN EVERY PECH</p>
        </div>
    </footer>

    <script>
        // Dynamic Pagg Styles Data Array
        const paggStylesData = [
            {
                id: 'patiala',
                category: 'groom',
                name: 'Royal Patiala Shahi',
                tagline: 'Deep symmetrical side curves with monarchical volume',
                time: '25 - 30 Mins',
                occasion: 'Anand Karaj & Grand Receptions',
                description: 'Defined by broad symmetrical side flares, an elevated front peak, and crisp diagonal layers. The gold standard for Punjabi grooms.',
                badge: 'Classic Royalty'
            },
            {
                id: 'wattan',
                category: 'modern',
                name: 'Modern Wattan Wali',
                tagline: 'Soft textured ridge layers with dynamic depth',
                time: '20 - 25 Mins',
                occasion: 'Sangeet, Parties & Groomsmen',
                description: 'Features artistic soft waves and ridges across the side profile. Blends modern elegance with traditional stature.',
                badge: 'Highly Popular'
            },
            {
                id: 'amritsari',
                category: 'classic',
                name: 'Executive Amritsari',
                tagline: 'Razor-sharp straight diagonal layers',
                time: '20 Mins',
                occasion: 'Formal Galas & Executive Events',
                description: 'Renowned for its clean straight lines, balanced symmetry, and sleek posture. Exudes discipline and sophistication.',
                badge: 'Sharp Precision'
            },
            {
                id: 'pochvi',
                category: 'classic',
                name: 'Classic Royal Pochvi',
                tagline: 'Ultra-crisp folded layers with neat contours',
                time: '25 Mins',
                occasion: 'Formal Ceremonies & Religious Events',
                description: 'Traditional fine-folded style emphasizing flat, neatly tucked layers that frame the face with understated nobility.',
                badge: 'Heritage Style'
            },
            {
                id: 'groom-crown',
                category: 'groom',
                name: 'Wedding Groom Crown',
                tagline: 'Reinforced crown for Kalgi & Sehra integration',
                time: '35 - 40 Mins',
                occasion: 'Anand Karaj Wedding Ceremony',
                description: 'Specially constructed with extended height and solid internal tension to support heavy jeweled Kalgis, pearl strings, and Sehras.',
                badge: 'Groom Special'
            },
            {
                id: 'uk-sharp',
                category: 'modern',
                name: 'Modern UK Sharp Style',
                tagline: 'High angled peak with narrow streamlined profile',
                time: '20 Mins',
                occasion: 'Contemporary Pre-Wedding Functions',
                description: 'Popularized in modern UK Punjabi fashion, featuring a distinct sharp peak and sleek sides for an athletic stance.',
                badge: 'Modern Trend'
            }
        ];

        let currentBasePrice = 180;
        let headCount = 1;

        document.addEventListener('DOMContentLoaded', () => {
            renderStyles('all');
            updateEstimator();
            initParticles();

            // Mobile Menu Toggle
            const menuBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            if (menuBtn) {
                menuBtn.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                });
            }

            document.querySelectorAll('.mobile-link').forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                });
            });
        });

        // Filter and Render Style Cards
        function filterStyles(cat) {
            document.querySelectorAll('#style-filters .filter-btn').forEach(btn => {
                btn.classList.remove('border-gold-400', 'bg-burgundy-900/80', 'text-gold-200');
                btn.classList.add('border-slate-700', 'bg-navy-900/60', 'text-slate-300');
            });
            event.currentTarget.classList.remove('border-slate-700', 'bg-navy-900/60', 'text-slate-300');
            event.currentTarget.classList.add('border-gold-400', 'bg-burgundy-900/80', 'text-gold-200');

            renderStyles(cat);
        }

        function renderStyles(filterCategory) {
            const container = document.getElementById('styles-container');
            const filtered = filterCategory === 'all' 
                ? paggStylesData 
                : paggStylesData.filter(s => s.category === filterCategory);

            container.innerHTML = filtered.map(style => `
                <div class="bg-navy-900/80 border border-gold-500/30 p-6 flex flex-col justify-between hover:border-gold-400 transition group royal-glow-hover">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="bg-burgundy-950 text-gold-300 text-[10px] font-heading font-semibold uppercase tracking-widest px-3 py-1 border border-gold-500/30">
                                ${style.badge}
                            </span>
                            <span class="text-xs text-slate-400 flex items-center">
                                <i class="fa-regular fa-clock text-gold-400 mr-1.5"></i> ${style.time}
                            </span>
                        </div>

                        <h3 class="font-heading text-xl font-bold text-slate-100 group-hover:text-gold-300 transition-colors">
                            ${style.name}
                        </h3>
                        <p class="font-serif italic text-xs text-gold-400/90 mt-1 mb-4">"${style.tagline}"</p>

                        <p class="text-xs text-slate-300 font-light leading-relaxed mb-6">
                            ${style.description}
                        </p>
                    </div>

                    <div class="border-t border-gold-500/20 pt-4 mt-auto">
                        <div class="text-[11px] text-slate-400 mb-3">
                            <strong class="text-slate-300 uppercase tracking-wider font-heading">Occasion:</strong> ${style.occasion}
                        </div>
                        <a href="#booking" onclick="selectStyleForForm('${style.name}')" class="inline-block w-full text-center py-2.5 bg-navy-950 border border-gold-500/40 text-gold-300 font-heading text-xs uppercase tracking-widest hover:bg-gold-500/20 transition">
                            Select Style
                        </a>
                    </div>
                </div>
            `).join('');
        }

        // Estimator Calculation Logic
        function selectOccasion(type, price) {
            currentBasePrice = price;
            document.querySelectorAll('.occasion-btn').forEach(btn => {
                btn.classList.remove('border-gold-500', 'bg-burgundy-900/60', 'active', 'text-slate-100');
                btn.classList.add('border-slate-700', 'bg-navy-900/60', 'text-slate-300');
            });
            event.currentTarget.classList.remove('border-slate-700', 'bg-navy-900/60', 'text-slate-300');
            event.currentTarget.classList.add('border-gold-500', 'bg-burgundy-900/60', 'active', 'text-slate-100');
            
            updateEstimator();
        }

        function adjustHeadCount(delta) {
            headCount = Math.max(1, headCount + delta);
            document.getElementById('head-count').innerText = headCount;
            updateEstimator();
        }

        function updateEstimator() {
            // Fabric
            const fabricRadios = document.getElementsByName('fabric');
            let fabricPrice = 0;
            let fabricName = 'Full Voile';
            for (let radio of fabricRadios) {
                if (radio.checked) {
                    fabricName = radio.value;
                    if (radio.value === 'Rubia Heavy') fabricPrice = 15;
                    if (radio.value === 'Malmal Soft Royal') fabricPrice = 20;
                }
            }

            // Color
            const colorSelect = document.getElementById('color-palette');
            const selectedColor = colorSelect.value;
            let colorExtra = selectedColor.includes('Custom Bespoke') ? 30 : 0;

            // Add-ons
            let addonsTotal = 0;
            if (document.getElementById('acc-kalgi').checked) addonsTotal += 25;
            if (document.getElementById('acc-sehra').checked) addonsTotal += 20;
            if (document.getElementById('acc-reception').checked) addonsTotal += 90;

            const grandTotal = ((currentBasePrice + fabricPrice) * headCount) + colorExtra + addonsTotal;

            // Occasion Name Label
            let occasionLabel = 'Royal Groom';
            if (currentBasePrice === 75) occasionLabel = 'Barat / Family';
            if (currentBasePrice === 85) occasionLabel = 'Executive Formal';
            if (currentBasePrice === 220) occasionLabel = 'Gala VIP Concierge';

            document.getElementById('total-price').innerText = `$${grandTotal}`;
            document.getElementById('summary-occasion').innerText = occasionLabel;
            document.getElementById('summary-fabric').innerText = fabricName;
            document.getElementById('summary-color').innerText = selectedColor.split(' (')[0];
            document.getElementById('summary-count').innerText = `${headCount} Person(s)`;
            document.getElementById('summary-addons').innerText = `$${addonsTotal + colorExtra}`;

            let estTime = (30 * headCount) + ' - ' + (45 * headCount) + ' mins';
            if (headCount === 1) estTime = '45 - 60 mins';
            document.getElementById('summary-time').innerText = estTime;
        }

        function selectStyleForForm(styleName) {
            const formStyle = document.getElementById('form-style');
            if (formStyle) formStyle.value = styleName;
        }

        function transferEstimateToBooking() {
            const occasion = document.getElementById('summary-occasion').innerText;
            const fabric = document.getElementById('summary-fabric').innerText;
            const color = document.getElementById('summary-color').innerText;
            const count = document.getElementById('summary-count').innerText;
            const total = document.getElementById('total-price').innerText;

            const textarea = document.getElementById('form-details');
            if (textarea) {
                textarea.value = `[Estimator Package Summary]\nStature: ${occasion}\nFabric: ${fabric}\nColor Theme: ${color}\nHead Count: ${count}\nEstimated Total: ${total}`;
            }
        }

        function handleReservationSubmit(e) {
            e.preventDefault();
            document.getElementById('booking-modal').classList.remove('hidden');
            document.getElementById('royal-reservation-form').reset();
        }

        function closeModal() {
            document.getElementById('booking-modal').classList.add('hidden');
        }

        function toggleFaq(id) {
            const ans = document.getElementById(`faq-ans-${id}`);
            const icon = document.getElementById(`faq-icon-${id}`);
            if (ans.classList.contains('hidden')) {
                ans.classList.remove('hidden');
                icon.classList.add('rotate-180');
            } else {
                ans.classList.add('hidden');
                icon.classList.remove('rotate-180');
            }
        }

        // Animated Gold Floating Particles Canvas
        function initParticles() {
            const canvas = document.getElementById('particles-canvas');
            const ctx = canvas.getContext('2d');
            
            let width = canvas.width = window.innerWidth;
            let height = canvas.height = window.innerHeight;

            window.addEventListener('resize', () => {
                width = canvas.width = window.innerWidth;
                height = canvas.height = window.innerHeight;
            });

            const particles = Array.from({ length: 40 }, () => ({
                x: Math.random() * width,
                y: Math.random() * height,
                radius: Math.random() * 1.5 + 0.5,
                alpha: Math.random() * 0.5 + 0.2,
                speedY: -(Math.random() * 0.3 + 0.1),
                speedX: (Math.random() - 0.5) * 0.2
            }));

            function animate() {
                ctx.clearRect(0, 0, width, height);

                particles.forEach(p => {
                    p.y += p.speedY;
                    p.x += p.speedX;

                    if (p.y < 0) p.y = height;
                    if (p.x < 0) p.x = width;
                    if (p.x > width) p.x = 0;

                    ctx.beginPath();
                    ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(212, 175, 55, ${p.alpha})`;
                    ctx.fill();
                });

                requestAnimationFrame(animate);
            }

            animate();
        }
    </script>
</body>
</html>
