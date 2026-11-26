```html
<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Studio Gabriele Machado — Nail Designer & Estética | Altamira - PA</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Cormorant Garamond & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400;1,600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        serif: ['"Cormorant Garamond"', 'Georgia', 'serif'],
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                    },
                    colors: {
                        cream: {
                            50: '#FDFBF9',
                            100: '#F9F5F0',
                            200: '#F2EAE0',
                            300: '#E6D8C8',
                        },
                        rosegold: {
                            300: '#DFB6AC',
                            400: '#CE9688',
                            500: '#B87A6B',
                            600: '#9E6153',
                            700: '#7D4B40',
                        },
                        charcoal: {
                            800: '#3D3532',
                            900: '#2A2421',
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Estilos Base e Micro-interações */
        body {
            background-color: #FDFBF9;
            color: #2A2421;
            font-family: 'Plus Jakarta Sans', sans-serif;
            -webkit-font-smoothing: antialiased;
        }

        .font-display {
            font-family: 'Cormorant Garamond', Georgia, serif;
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(223, 182, 172, 0.35);
        }

        .service-card {
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        .service-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 24px -8px rgba(184, 122, 107, 0.18);
            border-color: #CE9688;
        }

        /* Estilo de input editável sutil para preços */
        .editable-price {
            border-bottom: 1px dashed rgba(184, 122, 107, 0.5);
            transition: all 0.2s ease;
        }
        .editable-price:focus {
            outline: none;
            background-color: #F9F5F0;
            border-bottom: 1px solid #B87A6B;
            padding: 0 4px;
            border-radius: 4px;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #F9F5F0;
        }
        ::-webkit-scrollbar-thumb {
            background: #DFB6AC;
            border-radius: 9999px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #B87A6B;
        }

        /* =========================================================
           OTIMIZAÇÃO EXCLUSIVA PARA IMPRESSÃO / EXPORTAÇÃO EM PDF
           ========================================================= */
        @media print {
            @page {
                size: A4 portrait;
                margin: 12mm 14mm;
            }

            body {
                background-color: #FFFFFF !important;
                color: #2A2421 !important;
                font-size: 10.5pt !important;
                -webkit-print-color-adjust: exact !important;
                print-color-adjust: exact !important;
            }

            /* Ocultar elementos estritamente interativos de navegação/web */
            .no-print {
                display: none !important;
            }

            /* Exibir elementos exclusivos para impressão se necessário */
            .print-only {
                display: block !important;
            }

            /* Ajustes de espaçamento para caber perfeitamente em páginas limpas */
            header {
                padding-top: 10px !important;
                padding-bottom: 16px !important;
                background: #FDFBF9 !important;
                border-bottom: 1.5px solid #DFB6AC !important;
            }

            section {
                padding-top: 14px !important;
                padding-bottom: 14px !important;
            }

            /* Evitar quebras de página no meio de cards e blocos */
            .service-card, .rule-block, .print-avoid-break {
                break-inside: avoid !important;
                page-break-inside: avoid !important;
                box-shadow: none !important;
                border: 1px solid #E6D8C8 !important;
                background-color: #FFFFFF !important;
            }

            .editable-price {
                border-bottom: none !important;
            }

            /* Ajustar grids para 2 colunas no A4 */
            .print-grid-2 {
                display: grid !important;
                grid-template-columns: repeat(2, minmax(0, 1fr)) !important;
                gap: 10px !important;
            }

            /* Mostrar resumo de agendamento apenas se o cliente preencheu algo */
            #booking-section.empty-booking {
                display: none !important;
            }
        }
    </style>
</head>
<body class="selection:bg-rosegold-300 selection:text-charcoal-900">

    <!-- Barra Superior Flutuante (Ações Rápidas & PDF) -->
    <nav class="no-print sticky top-0 z-50 bg-cream-50/90 backdrop-blur-md border-b border-cream-200 transition-all">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between gap-2">
            <!-- Marca -->
            <a href="#" class="flex items-center gap-2.5 group">
                <span class="w-9 h-9 rounded-full bg-gradient-to-br from-rosegold-400 to-rosegold-600 text-white flex items-center justify-center font-display text-lg font-bold shadow-sm group-hover:scale-105 transition-transform">
                    GM
                </span>
                <div class="leading-tight">
                    <span class="font-display text-lg sm:text-xl font-bold tracking-wide text-charcoal-900 block">Gabriele Machado</span>
                    <span class="text-[10px] uppercase tracking-[0.2em] text-rosegold-600 font-medium block">Nail Designer & Estética</span>
                </div>
            </a>

            <!-- Links de Navegação Desktop -->
            <div class="hidden md:flex items-center gap-6 text-sm font-medium text-charcoal-800">
                <a href="#catalogo" class="hover:text-rosegold-600 transition-colors">Catálogo de Serviços</a>
                <a href="#agendamento" class="hover:text-rosegold-600 transition-colors">Simular Agendamento</a>
                <a href="#cuidados" class="hover:text-rosegold-600 transition-colors">Regras & Cuidados</a>
            </div>

            <!-- Botões de Ação -->
            <div class="flex items-center gap-2">
                <button onclick="exportarPDF()" title="Baixar catálogo e ficha em PDF" class="inline-flex items-center gap-2 px-3.5 py-2 rounded-full text-xs sm:text-sm font-medium bg-cream-200/80 hover:bg-cream-300 text-charcoal-900 border border-rosegold-300/60 transition-all cursor-pointer">
                    <i class="fa-solid fa-file-pdf text-rosegold-600"></i>
                    <span class="hidden sm:inline">Salvar / Baixar PDF</span>
                    <span class="sm:hidden">PDF</span>
                </button>
                <a href="#agendamento" class="inline-flex items-center gap-2 px-4 py-2 rounded-full text-xs sm:text-sm font-semibold bg-gradient-to-r from-rosegold-500 to-rosegold-600 hover:from-rosegold-600 hover:to-rosegold-700 text-white shadow-sm hover:shadow transition-all">
                    <i class="fa-regular fa-calendar-check"></i>
                    <span>Agendar</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- 1. CABEÇALHO / HERO SECTION -->
    <header class="relative overflow-hidden bg-gradient-to-b from-cream-100 via-cream-50 to-cream-50 pt-10 pb-14 sm:pt-16 sm:pb-20 border-b border-cream-200/70">
        <!-- Elementos decorativos sutis -->
        <div class="no-print absolute -top-24 -right-24 w-80 h-80 rounded-full bg-rosegold-300/15 blur-3xl pointer-events-none"></div>
        <div class="no-print absolute top-40 -left-20 w-72 h-72 rounded-full bg-cream-300/30 blur-3xl pointer-events-none"></div>

        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
            <!-- Selo de Localização -->
            <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-white border border-rosegold-300/50 shadow-xs mb-6">
                <i class="fa-solid fa-location-dot text-rosegold-500 text-xs"></i>
                <span class="text-xs font-medium tracking-wide text-charcoal-800">
                    Altamira - PA • Atendimento no Studio & em Domicílio
                </span>
            </div>

            <!-- Título Principal -->
            <h1 class="font-display text-4xl sm:text-5xl md:text-6xl font-bold text-charcoal-900 tracking-tight leading-[1.12] mb-4">
                Studio Gabriele Machado
                <span class="block text-2xl sm:text-3xl md:text-4xl font-normal italic text-rosegold-600 mt-1">
                    Nail Designer & Estética
                </span>
            </h1>

            <!-- Subtítulo Convidativo -->
            <p class="max-w-2xl mx-auto text-sm sm:text-base md:text-lg text-charcoal-800/85 font-light leading-relaxed mb-8">
                Realçando a beleza natural das suas mãos, pés e olhar com técnicas modernas, biossegurança rigorosa e atendimento acolhedor pensado exclusivamente para você.
            </p>

            <!-- Botões de Ação Rápida (Ocultos na impressão) -->
            <div class="no-print flex flex-col sm:flex-row items-center justify-center gap-3.5">
                <a href="#agendamento" class="w-full sm:w-auto inline-flex items-center justify-center gap-2.5 px-7 py-3.5 rounded-full bg-charcoal-900 hover:bg-charcoal-800 text-cream-50 text-sm font-semibold shadow-md hover:shadow-lg transition-all">
                    <i class="fa-brands fa-whatsapp text-lg text-rosegold-300"></i>
                    <span>Agendar Horário Agora</span>
                </a>
                <a href="#catalogo" class="w-full sm:w-auto inline-flex items-center justify-center gap-2 px-7 py-3.5 rounded-full bg-white hover:bg-cream-100 text-charcoal-900 border border-rosegold-300 text-sm font-medium transition-all">
                    <span>Explorar Catálogo de Serviços</span>
                    <i class="fa-solid fa-arrow-down text-xs text-rosegold-500"></i>
                </a>
            </div>

            <!-- Destaques Rápidos -->
            <div class="grid grid-cols-3 gap-3 sm:gap-6 max-w-2xl mx-auto mt-10 pt-8 border-t border-cream-200">
                <div class="text-center">
                    <span class="block font-display text-xl sm:text-2xl font-bold text-rosegold-600">100%</span>
                    <span class="text-[11px] sm:text-xs text-charcoal-800/75">Biossegurança & Cuidado</span>
                </div>
                <div class="text-center border-x border-cream-200 px-2">
                    <span class="block font-display text-xl sm:text-2xl font-bold text-rosegold-600">Personalizado</span>
                    <span class="text-[11px] sm:text-xs text-charcoal-800/75">Studio ou Domicílio</span>
                </div>
                <div class="text-center">
                    <span class="block font-display text-xl sm:text-2xl font-bold text-rosegold-600">Alta Durabilidade</span>
                    <span class="text-[11px] sm:text-xs text-charcoal-800/75">Produtos Premium</span>
                </div>
            </div>
        </div>
    </header>

    <!-- 2. CATÁLOGO COMPLETO DE SERVIÇOS -->
    <section id="catalogo" class="py-14 sm:py-20 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Cabeçalho da Seção -->
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-4">
            <div>
                <span class="text-xs uppercase tracking-[0.22em] text-rosegold-600 font-semibold block mb-1.5">Menu de Procedimentos</span>
                <h2 class="font-display text-3xl sm:text-4xl font-bold text-charcoal-900">Catálogo de Serviços</h2>
            </div>
            <div class="no-print flex items-center gap-2 text-xs text-charcoal-800/75 bg-cream-100 px-3.5 py-2 rounded-xl border border-cream-200">
                <i class="fa-solid fa-pen-to-square text-rosegold-500"></i>
                <span>Dica: Clique nos valores para editar antes de gerar o PDF ou marque os serviços para simular.</span>
            </div>
        </div>

        <!-- Filtros de Categoria (Apenas Web) -->
        <div class="no-print flex flex-wrap gap-2 mb-8" id="category-filters">
            <button onclick="filtrarCategoria('todos')" data-filter="todos" class="filter-btn active px-4 py-2 rounded-full text-xs sm:text-sm font-medium bg-charcoal-900 text-white transition-all cursor-pointer">
                Todos os Serviços
            </button>
            <button onclick="filtrarCategoria('naturais')" data-filter="naturais" class="filter-btn px-4 py-2 rounded-full text-xs sm:text-sm font-medium bg-white text-charcoal-800 border border-cream-300 hover:border-rosegold-400 transition-all cursor-pointer">
                Unhas Naturais & Cutilagem
            </button>
            <button onclick="filtrarCategoria('alongamentos')" data-filter="alongamentos" class="filter-btn px-4 py-2 rounded-full text-xs sm:text-sm font-medium bg-white text-charcoal-800 border border-cream-300 hover:border-rosegold-400 transition-all cursor-pointer">
                Alongamentos & Nail Art
            </button>
            <button onclick="filtrarCategoria('especiais')" data-filter="especiais" class="filter-btn px-4 py-2 rounded-full text-xs sm:text-sm font-medium bg-white text-charcoal-800 border border-cream-300 hover:border-rosegold-400 transition-all cursor-pointer">
                SPA & Cuidados Especiais
            </button>
            <button onclick="filtrarCategoria('olhar')" data-filter="olhar" class="filter-btn px-4 py-2 rounded-full text-xs sm:text-sm font-medium bg-white text-charcoal-800 border border-cream-300 hover:border-rosegold-400 transition-all cursor-pointer">
                Sobrancelhas & Cílios
            </button>
        </div>

        <!-- Container das Categorias -->
        <div class="space-y-12" id="services-container">
            
            <!-- CATEGORIA 1: Unhas Naturais & Cutilagem -->
            <div class="category-group" data-category="naturais">
                <div class="flex items-center gap-3 mb-5 border-b border-cream-200 pb-2.5">
                    <span class="w-8 h-8 rounded-full bg-cream-200 text-rosegold-600 flex items-center justify-center text-sm">
                        <i class="fa-solid fa-hand-sparkles"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Unhas Naturais & Cutilagem</h3>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 print-grid-2">
                    <!-- Serviço 1.1 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Manicure & Pedicure Tradicional</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="manicure-pedicure">60,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Corte, lixamento técnico, hidratação, cutilagem clássica cuidadosa e esmaltação impecável (opção avulsa ou combo mãos e pés).
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h30</span>
                            <button onclick="toggleServico(this, 'Manicure & Pedicure Tradicional', 'manicure-pedicure')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 1.2 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Cutilagem Russa (Combinada)</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="cutilagem-russa">75,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Técnica a seco com brocas diamantadas de alta precisão que proporciona acabamento limpo, seguro e retarda o crescimento da cutícula.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h15</span>
                            <button onclick="toggleServico(this, 'Cutilagem Russa', 'cutilagem-russa')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 1.3 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Blindagem em Acrigel</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="blindagem">85,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Camada protetora resistente aplicada sobre o comprimento natural para evitar quebras, descamações e garantir brilho prolongado.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h30</span>
                            <button onclick="toggleServico(this, 'Blindagem em Acrigel', 'blindagem')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 1.4 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Banho em Gel</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="banho-gel">95,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Estruturação em gel diretamente sobre a unha natural, oferecendo resistência superior e nivelamento perfeito sem aumentar o tamanho.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h45</span>
                            <button onclick="toggleServico(this, 'Banho em Gel', 'banho-gel')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- CATEGORIA 2: Alongamentos -->
            <div class="category-group" data-category="alongamentos">
                <div class="flex items-center gap-3 mb-5 border-b border-cream-200 pb-2.5">
                    <span class="w-8 h-8 rounded-full bg-cream-200 text-rosegold-600 flex items-center justify-center text-sm">
                        <i class="fa-solid fa-wand-magic-sparkles"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Alongamentos & Nail Art</h3>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 print-grid-2">
                    <!-- Serviço 2.1 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Alongamento em Gel (Molde F1)</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="molde-f1">130,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Curvatura simétrica, acabamento espelhado e rapidez na aplicação com moldes anatômicos que garantem leveza e naturalidade.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~2h00</span>
                            <button onclick="toggleServico(this, 'Alongamento em Gel (Molde F1)', 'molde-f1')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 2.2 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Alongamento em Fibra de Vidro</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="fibra-vidro">150,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Filamentos de fibra moldados fio a fio para alta resistência, aspecto ultra natural, espessura fina e durabilidade superior.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~2h30</span>
                            <button onclick="toggleServico(this, 'Alongamento em Fibra de Vidro', 'fibra-vidro')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 2.3 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Soft Gel (Postiça Realista)</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="soft-gel">110,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Cápsulas 100% em gel flexível aderidas com base em gel. Conforto imediato, formato impecável e excelente fixação.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h30</span>
                            <button onclick="toggleServico(this, 'Soft Gel (Postiça Realista)', 'soft-gel')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 2.4 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Nail Art & Estilo Coreano</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">A partir de R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="nail-art">25,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Decorações personalizadas: estilo coreano (aurora, relevo 3D, charm, blush nails), francesinha reversa, baby boomer, encapsuladas e pedrarias.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-solid fa-palette mr-1"></i> Adicional personalizado</span>
                            <button onclick="toggleServico(this, 'Nail Art / Estilo Coreano', 'nail-art')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- CATEGORIA 3: Cuidados Especiais -->
            <div class="category-group" data-category="especiais">
                <div class="flex items-center gap-3 mb-5 border-b border-cream-200 pb-2.5">
                    <span class="w-8 h-8 rounded-full bg-cream-200 text-rosegold-600 flex items-center justify-center text-sm">
                        <i class="fa-solid fa-spa"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Cuidados Especiais</h3>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 print-grid-2">
                    <!-- Serviço 3.1 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">SPA dos Pés</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="spa-pes">70,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Ritual relaxante com escalda-pés aromático, esfoliação revitalizante, hidratação profunda e massagem para alívio de tensões e maciez.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~50min</span>
                            <button onclick="toggleServico(this, 'SPA dos Pés', 'spa-pes')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 3.2 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Plástica dos Pés</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="plastica-pes">90,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Tratamento intensivo para remoção segura de calosidades, asperezas e fissuras plantares, devolvendo toque aveludado desde a 1ª sessão.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~1h10</span>
                            <button onclick="toggleServico(this, 'Plástica dos Pés', 'plastica-pes')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- CATEGORIA 4: Sobrancelhas & Cílios -->
            <div class="category-group" data-category="olhar">
                <div class="flex items-center gap-3 mb-5 border-b border-cream-200 pb-2.5">
                    <span class="w-8 h-8 rounded-full bg-cream-200 text-rosegold-600 flex items-center justify-center text-sm">
                        <i class="fa-solid fa-eye"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Sobrancelhas & Cílios</h3>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 print-grid-2">
                    <!-- Serviço 4.1 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Design de Sobrancelhas (Simples)</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="design-simples">35,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Mapeamento facial estratégico conforme a simetria do seu rosto, alinhamento dos fios e epilação precisa para valorizar sua expressão.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~30min</span>
                            <button onclick="toggleServico(this, 'Design de Sobrancelhas Simples', 'design-simples')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 4.2 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Design com Henna La Benig</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="design-henna">50,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Mapeamento personalizado + aplicação de Henna La Benig com efeito ombré natural, cobertura de falhas e excelente fixação na pele.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~45min</span>
                            <button onclick="toggleServico(this, 'Design com Henna La Benig', 'design-henna')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>

                    <!-- Serviço 4.3 -->
                    <div class="service-card bg-white rounded-2xl p-5 border border-cream-200 flex flex-col justify-between md:col-span-2">
                        <div>
                            <div class="flex justify-between items-start gap-3 mb-2">
                                <h4 class="font-semibold text-base text-charcoal-900">Cílios Tufinho</h4>
                                <div class="text-right shrink-0">
                                    <span class="text-xs text-rosegold-600 font-medium">R$</span>
                                    <span contenteditable="true" class="editable-price font-display text-xl font-bold text-charcoal-900" data-price-id="cilios-tufinho">65,00</span>
                                </div>
                            </div>
                            <p class="text-xs sm:text-sm text-charcoal-800/75 leading-relaxed mb-4">
                                Aplicação leve e rápida que proporciona volume delicado, curvatura marcante e olhar realçado ideal para eventos ou praticidade no dia a dia.
                            </p>
                        </div>
                        <div class="no-print flex items-center justify-between pt-3 border-t border-cream-100">
                            <span class="text-[11px] text-charcoal-800/60"><i class="fa-regular fa-clock mr-1"></i> ~40min</span>
                            <button onclick="toggleServico(this, 'Cílios Tufinho', 'cilios-tufinho')" class="select-service-btn inline-flex items-center gap-1.5 px-3.5 py-1.5 rounded-full text-xs font-medium bg-cream-100 hover:bg-rosegold-500 hover:text-white text-charcoal-900 transition-colors cursor-pointer">
                                <i class="fa-solid fa-plus text-[10px]"></i>
                                <span>Selecionar</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- 3. SIMULADOR / FORMULÁRIO INTERATIVO DE AGENDAMENTO -->
    <section id="agendamento" class="empty-booking py-14 sm:py-20 bg-cream-100/80 border-y border-cream-200">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-10">
                <span class="text-xs uppercase tracking-[0.22em] text-rosegold-600 font-semibold block mb-1.5">Agendamento Online</span>
                <h2 class="font-display text-3xl sm:text-4xl font-bold text-charcoal-900 mb-3">Monte seu Atendimento</h2>
                <p class="no-print text-sm text-charcoal-800/80">
                    Selecione os procedimentos desejados acima ou abaixo, informe sua preferência e gere sua solicitação pronta para enviar via WhatsApp ou salvar em PDF.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
                <!-- Formulário de Dados (Oculto na impressão, pois o resumo à direita já traz tudo consolidado) -->
                <div class="no-print lg:col-span-7 bg-white rounded-3xl p-6 sm:p-8 border border-cream-200 shadow-xs space-y-5">
                    <h3 class="font-display text-2xl font-bold text-charcoal-900 border-b border-cream-200 pb-3">1. Seus Dados & Preferências</h3>

                    <!-- Nome e WhatsApp -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label for="client-name" class="block text-xs font-semibold text-charcoal-800 mb-1.5">Seu Nome Completo *</label>
                            <input type="text" id="client-name" oninput="atualizarResumo()" placeholder="Ex: Ana Clara Souza" class="w-full px-4 py-2.5 rounded-xl bg-cream-50 border border-cream-300 text-sm focus:outline-none focus:border-rosegold-500 transition-colors">
                        </div>
                        <div>
                            <label for="client-phone" class="block text-xs font-semibold text-charcoal-800 mb-1.5">Seu WhatsApp *</label>
                            <input type="tel" id="client-phone" oninput="atualizarResumo()" placeholder="(93) 99999-9999" class="w-full px-4 py-2.5 rounded-xl bg-cream-50 border border-cream-300 text-sm focus:outline-none focus:border-rosegold-500 transition-colors">
                        </div>
                    </div>

                    <!-- Modalidade de Atendimento -->
                    <div>
                        <label class="block text-xs font-semibold text-charcoal-800 mb-2">Modalidade de Atendimento</label>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                            <label class="relative flex items-center gap-3 p-3.5 rounded-xl border border-cream-300 bg-cream-50/60 cursor-pointer hover:border-rosegold-400 transition-all">
                                <input type="radio" name="modality" value="No Studio (Altamira - PA)" checked onchange="atualizarResumo()" class="accent-rosegold-600 w-4 h-4">
                                <div>
                                    <span class="block text-sm font-semibold text-charcoal-900">No Studio</span>
                                    <span class="block text-[11px] text-charcoal-800/70">Ambiente climatizado e aconchegante</span>
                                </div>
                            </label>
                            <label class="relative flex items-center gap-3 p-3.5 rounded-xl border border-cream-300 bg-cream-50/60 cursor-pointer hover:border-rosegold-400 transition-all">
                                <input type="radio" name="modality" value="Atendimento em Domicílio" onchange="atualizarResumo()" class="accent-rosegold-600 w-4 h-4">
                                <div>
                                    <span class="block text-sm font-semibold text-charcoal-900">Em Domicílio</span>
                                    <span class="block text-[11px] text-charcoal-800/70">Conforto no seu lar (consultar taxa)</span>
                                </div>
                            </label>
                        </div>
                    </div>

                    <!-- Data e Horário -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label for="booking-date" class="block text-xs font-semibold text-charcoal-800 mb-1.5">Data Preferida</label>
                            <input type="date" id="booking-date" onchange="atualizarResumo()" class="w-full px-4 py-2.5 rounded-xl bg-cream-50 border border-cream-300 text-sm focus:outline-none focus:border-rosegold-500 transition-colors">
                        </div>
                        <div>
                            <label for="booking-time" class="block text-xs font-semibold text-charcoal-800 mb-1.5">Horário / Turno Preferido</label>
                            <select id="booking-time" onchange="atualizarResumo()" class="w-full px-4 py-2.5 rounded-xl bg-cream-50 border border-cream-300 text-sm focus:outline-none focus:border-rosegold-500 transition-colors">
                                <option value="Manhã (08:30 - 11:30)">Manhã (08:30 às 11:30)</option>
                                <option value="Tarde (13:30 - 17:30)">Tarde (13:30 às 17:30)</option>
                                <option value="Noite / Horário Flexível (18:00 - 20:30)">Noite / Horário Flexível (18:00 às 20:30)</option>
                            </select>
                        </div>
                    </div>

                    <!-- Observações -->
                    <div>
                        <label for="booking-notes" class="block text-xs font-semibold text-charcoal-800 mb-1.5">Observações (Opcional)</label>
                        <textarea id="booking-notes" rows="2" oninput="atualizarResumo()" placeholder="Ex: Preciso de remoção de alongamento anterior, ou endereço para atendimento em domicílio..." class="w-full px-4 py-2.5 rounded-xl bg-cream-50 border border-cream-300 text-sm focus:outline-none focus:border-rosegold-500 transition-colors"></textarea>
                    </div>
                </div>

                <!-- Card de Resumo & Comprovante (Visível na Web e na Impressão se preenchido) -->
                <div class="lg:col-span-5 print-avoid-break bg-white rounded-3xl p-6 sm:p-8 border-2 border-rosegold-300/70 shadow-md">
                    <div class="flex items-center justify-between border-b border-cream-200 pb-3 mb-4">
                        <div>
                            <span class="text-[10px] uppercase tracking-widest text-rosegold-600 font-bold block">Resumo & Pré-Reserva</span>
                            <h3 class="font-display text-2xl font-bold text-charcoal-900">Ficha de Agendamento</h3>
                        </div>
                        <i class="fa-solid fa-receipt text-rosegold-400 text-xl"></i>
                    </div>

                    <!-- Lista de Serviços Selecionados -->
                    <div class="mb-5">
                        <span class="text-xs font-semibold text-charcoal-800 block mb-2">Procedimentos Selecionados:</span>
                        <ul id="selected-services-list" class="space-y-2 text-sm">
                            <li class="text-xs italic text-charcoal-800/60 py-3 px-3 bg-cream-50 rounded-xl border border-dashed border-cream-300 text-center">
                                Nenhum serviço selecionado ainda. Clique em "+ Selecionar" no catálogo acima.
                            </li>
                        </ul>
                    </div>

                    <!-- Detalhes Preenchidos -->
                    <div class="bg-cream-50 rounded-2xl p-4 space-y-2 text-xs text-charcoal-800 mb-5 border border-cream-200">
                        <div class="flex justify-between">
                            <span class="text-charcoal-800/70">Cliente:</span>
                            <span id="summary-name" class="font-semibold text-charcoal-900">Não informado</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-charcoal-800/70">WhatsApp:</span>
                            <span id="summary-phone" class="font-semibold text-charcoal-900">Não informado</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-charcoal-800/70">Local:</span>
                            <span id="summary-modality" class="font-semibold text-rosegold-700">No Studio (Altamira - PA)</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-charcoal-800/70">Data & Turno:</span>
                            <span id="summary-datetime" class="font-semibold text-charcoal-900">A combinar</span>
                        </div>
                        <div id="summary-notes-row" class="hidden pt-1 border-t border-cream-200">
                            <span class="text-charcoal-800/70 block">Observações:</span>
                            <span id="summary-notes" class="font-medium text-charcoal-900 italic"></span>
                        </div>
                    </div>

                    <!-- Estimativa de Investimento e Sinal -->
                    <div class="border-t border-cream-200 pt-4 mb-6 space-y-1.5">
                        <div class="flex items-baseline justify-between">
                            <span class="text-sm font-medium text-charcoal-800">Investimento Estimado:</span>
                            <span id="summary-total" class="font-display text-2xl font-bold text-charcoal-900">R$ 0,00</span>
                        </div>
                        <div class="flex items-center justify-between text-xs text-rosegold-700 bg-rosegold-300/15 px-3 py-1.5 rounded-lg">
                            <span>Sinal para reserva (30% a 50%):</span>
                            <span id="summary-deposit" class="font-semibold">R$ 0,00 – R$ 0,00</span>
                        </div>
                    </div>

                    <!-- Botões de Ação do Resumo (Ocultos na impressão) -->
                    <div class="no-print space-y-2.5">
                        <button onclick="enviarWhatsApp()" class="w-full py-3.5 px-5 rounded-full bg-gradient-to-r from-rosegold-500 to-rosegold-600 hover:from-rosegold-600 hover:to-rosegold-700 text-white font-semibold text-sm shadow-md hover:shadow-lg transition-all flex items-center justify-center gap-2 cursor-pointer">
                            <i class="fa-brands fa-whatsapp text-lg"></i>
                            <span>Enviar Solicitação no WhatsApp</span>
                        </button>
                        <div class="grid grid-cols-2 gap-2">
                            <button onclick="copiarMensagem()" class="py-2.5 px-3 rounded-full bg-cream-100 hover:bg-cream-200 text-charcoal-900 border border-cream-300 text-xs font-medium transition-colors flex items-center justify-center gap-1.5 cursor-pointer">
                                <i class="fa-regular fa-copy text-rosegold-600"></i>
                                <span>Copiar Texto</span>
                            </button>
                            <button onclick="exportarPDF()" class="py-2.5 px-3 rounded-full bg-charcoal-900 hover:bg-charcoal-800 text-cream-50 text-xs font-medium transition-colors flex items-center justify-center gap-1.5 cursor-pointer">
                                <i class="fa-solid fa-print text-rosegold-300"></i>
                                <span>Gerar PDF</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. REGRAS DE AGENDAMENTO E CUIDADOS PÓS-PROCEDIMENTO -->
    <section id="cuidados" class="py-14 sm:py-20 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-2xl mx-auto mb-12">
            <span class="text-xs uppercase tracking-[0.22em] text-rosegold-600 font-semibold block mb-1.5">Transparência & Durabilidade</span>
            <h2 class="font-display text-3xl sm:text-4xl font-bold text-charcoal-900">Políticas & Cuidados Pós-Procedimento</h2>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 print-grid-2">
            <!-- Bloco 1: Regras de Agendamento -->
            <div class="rule-block bg-white rounded-3xl p-6 sm:p-8 border border-cream-200 shadow-xs">
                <div class="flex items-center gap-3 mb-5">
                    <span class="w-10 h-10 rounded-2xl bg-rosegold-300/20 text-rosegold-600 flex items-center justify-center text-lg">
                        <i class="fa-regular fa-calendar-check"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Regras de Agendamento</h3>
                </div>

                <ul class="space-y-4 text-xs sm:text-sm text-charcoal-800/85 leading-relaxed">
                    <li class="flex items-start gap-3">
                        <i class="fa-solid fa-gem text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Reserva mediante Sinal (30% a 50%):</strong>
                            Para garantir a exclusividade do seu horário na agenda — especialmente em datas comemorativas, feriados e fim de ano — é necessário o pagamento antecipado de 30% a 50% do valor do procedimento (abatido no valor final).
                        </div>
                    </li>
                    <li class="flex items-start gap-3">
                        <i class="fa-regular fa-clock text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Tolerância de Atraso:</strong>
                            Pedimos pontualidade para não comprometer o atendimento da cliente seguinte. A tolerância máxima é de <strong>15 minutos</strong>; após esse período, o atendimento poderá ser reduzido ou reagendado.
                        </div>
                    </li>
                    <li class="flex items-start gap-3">
                        <i class="fa-solid fa-rotate text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Reagendamento & Cancelamento:</strong>
                            Imprevistos acontecem! Avise com no mínimo <strong>24 horas de antecedência</strong> para reagendar sem perda do sinal. Desistências no mesmo dia implicam na retenção do sinal para cobertura da agenda reservada.
                        </div>
                    </li>
                </ul>
            </div>

            <!-- Bloco 2: Cuidados Pós-Procedimento -->
            <div class="rule-block bg-white rounded-3xl p-6 sm:p-8 border border-cream-200 shadow-xs">
                <div class="flex items-center gap-3 mb-5">
                    <span class="w-10 h-10 rounded-2xl bg-rosegold-300/20 text-rosegold-600 flex items-center justify-center text-lg">
                        <i class="fa-solid fa-heart-pulse"></i>
                    </span>
                    <h3 class="font-display text-2xl font-bold text-charcoal-900">Cuidados Pós-Procedimento</h3>
                </div>

                <ul class="space-y-4 text-xs sm:text-sm text-charcoal-800/85 leading-relaxed">
                    <li class="flex items-start gap-3">
                        <i class="fa-solid fa-shield-halved text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Unhas em Gel, Fibra & Blindagem:</strong>
                            Evite o uso de <strong>acetona pura</strong> (prefira removedores sem acetona) e utilize luvas ao manusear produtos químicos fortes de limpeza. Nunca utilize as unhas como "ferramentas" para abrir latas ou raspar superfícies.
                        </div>
                    </li>
                    <li class="flex items-start gap-3">
                        <i class="fa-solid fa-calendar-days text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Manutenção Periódica:</strong>
                            Realize a manutenção dos alongamentos entre <strong>15 a 21 dias</strong> para preservar a estrutura, saúde da lâmina ungueal e evitar infiltrações. Nunca arranque o alongamento em casa.
                        </div>
                    </li>
                    <li class="flex items-start gap-3">
                        <i class="fa-solid fa-droplet-slash text-rosegold-500 mt-1 text-xs"></i>
                        <div>
                            <strong class="text-charcoal-900 block">Sobrancelhas com Henna La Benig:</strong>
                            Para máxima pigmentação e durabilidade, <strong>evite molhar as sobrancelhas nas primeiras 24h a 48h</strong> após a aplicação. Não aplique demaquilantes bifásicos, óleos ou esfoliantes diretamente sobre a região.
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- 5. RODAPÉ ELEGANTE -->
    <footer class="bg-charcoal-900 text-cream-100 py-12 sm:py-16 border-t border-charcoal-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-center pb-8 border-b border-cream-100/15">
                <!-- Identidade -->
                <div>
                    <div class="flex items-center gap-3 mb-3">
                        <span class="w-10 h-10 rounded-full bg-rosegold-500 text-white flex items-center justify-center font-display text-xl font-bold">GM</span>
                        <div>
                            <h4 class="font-display text-2xl font-bold text-white leading-none">Studio Gabriele Machado</h4>
                            <span class="text-[11px] uppercase tracking-[0.2em] text-rosegold-300">Nail Designer & Estética</span>
                        </div>
                    </div>
                    <p class="text-xs text-cream-200/75 leading-relaxed max-w-xs">
                        Cuidado artesanal, estética avançada e atendimento personalizado para realçar a sua melhor versão.
                    </p>
                </div>

                <!-- Contato e Horários -->
                <div class="space-y-2.5 text-xs sm:text-sm text-cream-200/85">
                    <div class="flex items-center gap-2.5">
                        <i class="fa-solid fa-location-dot text-rosegold-400 w-4"></i>
                        <span>Altamira - Pará (Studio & Domicílio)</span>
                    </div>
                    <div class="flex items-center gap-2.5">
                        <i class="fa-regular fa-clock text-rosegold-400 w-4"></i>
                        <span>Horários Flexíveis mediante agendamento prévio</span>
                    </div>
                    <div class="flex items-center gap-2.5">
                        <i class="fa-brands fa-instagram text-rosegold-400 w-4"></i>
                        <span>@studiogabrielemachado</span>
                    </div>
                </div>

                <!-- Botão Principal de Exportação PDF -->
                <div class="no-print flex flex-col sm:items-end justify-center gap-2">
                    <button onclick="exportarPDF()" class="w-full sm:w-auto inline-flex items-center justify-center gap-2.5 px-6 py-3.5 rounded-full bg-gradient-to-r from-rosegold-400 to-rosegold-600 hover:from-rosegold-500 hover:to-rosegold-700 text-white font-semibold text-sm shadow-lg transition-all cursor-pointer">
                        <i class="fa-solid fa-file-arrow-down text-base"></i>
                        <span>Exportar Catálogo & Agenda em PDF</span>
                    </button>
                    <span class="text-[11px] text-cream-200/60">Formato A4 otimizado para salvar ou imprimir</span>
                </div>
            </div>

            <div class="pt-6 flex flex-col sm:flex-row items-center justify-between text-xs text-cream-200/50 gap-2">
                <span>© 2026 Studio Gabriele Machado — Todos os direitos reservados.</span>
                <span>Altamira - PA • Feito com carinho e sofisticação</span>
            </div>
        </div>
    </footer>

    <!-- Toast de Notificação (Substitui alert()) -->
    <div id="toast-notification" class="no-print fixed bottom-5 right-5 z-50 transform translate-y-24 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="bg-charcoal-900 text-cream-50 px-5 py-3.5 rounded-2xl shadow-xl border border-rosegold-400/50 flex items-center gap-3 text-xs sm:text-sm max-w-sm">
            <i id="toast-icon" class="fa-solid fa-circle-check text-rosegold-400 text-base"></i>
            <span id="toast-message">Mensagem copiada com sucesso!</span>
        </div>
    </div>

    <!-- JavaScript de Interatividade, Cálculo e Exportação -->
    <script>
        // Número de WhatsApp padrão (substituir pelo número real do Studio em Altamira - DD 93)
        const STUDIO_WHATSAPP = "5593999999999";

        // Estado dos serviços selecionados
        const servicosSelecionados = new Map();

        // Exibir Toast elegante (nunca usar alert)
        function mostrarToast(mensagem, tipo = 'sucesso') {
            const toast = document.getElementById('toast-notification');
            const toastMsg = document.getElementById('toast-message');
            const toastIcon = document.getElementById('toast-icon');

            toastMsg.textContent = mensagem;
            if (tipo === 'aviso') {
                toastIcon.className = 'fa-solid fa-circle-exclamation text-amber-400 text-base';
            } else {
                toastIcon.className = 'fa-solid fa-circle-check text-rosegold-400 text-base';
            }

            toast.classList.remove('translate-y-24', 'opacity-0');
            clearTimeout(window.toastTimeout);
            window.toastTimeout = setTimeout(() => {
                toast.classList.add('translate-y-24', 'opacity-0');
            }, 3500);
        }

        // Converter string de preço (ex: "130,00") para número float
        function parsePreco(textoPreco) {
            if (!textoPreco) return 0;
            const limpo = textoPreco.replace(/[^\d,.-]/g, '').replace('.', '').replace(',', '.');
            const valor = parseFloat(limpo);
            return isNaN(valor) ? 0 : valor;
        }

        // Formatar número para Real (BRL)
        function formatarBRL(valor) {
            return valor.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        // Filtrar categorias no catálogo
        function filtrarCategoria(categoria) {
            const botoes = document.querySelectorAll('.filter-btn');
            botoes.forEach(btn => {
                if (btn.dataset.filter === categoria) {
                    btn.classList.remove('bg-white', 'text-charcoal-800', 'border', 'border-cream-300');
                    btn.classList.add('bg-charcoal-900', 'text-white');
                } else {
                    btn.classList.add('bg-white', 'text-charcoal-800', 'border', 'border-cream-300');
                    btn.classList.remove('bg-charcoal-900', 'text-white');
                }
            });

            const grupos = document.querySelectorAll('.category-group');
            grupos.forEach(grupo => {
                if (categoria === 'todos' || grupo.dataset.category === categoria) {
                    grupo.style.display = 'block';
                } else {
                    grupo.style.display = 'none';
                }
            });
        }

        // Selecionar / Remover serviço na simulação
        function toggleServico(botao, nomeServico, priceId) {
            const spanPreco = document.querySelector(`[data-price-id="${priceId}"]`);
            const valorNumerico = spanPreco ? parsePreco(spanPreco.textContent) : 0;

            if (servicosSelecionados.has(priceId)) {
                servicosSelecionados.delete(priceId);
                botao.innerHTML = '<i class="fa-solid fa-plus text-[10px]"></i><span>Selecionar</span>';
                botao.classList.remove('bg-rosegold-600', 'text-white');
                botao.classList.add('bg-cream-100', 'text-charcoal-900');
            } else {
                servicosSelecionados.set(priceId, {
                    id: priceId,
                    nome: nomeServico,
                    preco: valorNumerico
                });
                botao.innerHTML = '<i class="fa-solid fa-check text-[10px]"></i><span>Selecionado</span>';
                botao.classList.remove('bg-cream-100', 'text-charcoal-900');
                botao.classList.add('bg-rosegold-600', 'text-white');
                mostrarToast(`"${nomeServico}" adicionado à sua ficha.`);
            }

            atualizarResumo();
        }

        // Ouvir alterações nos preços editáveis para recalcular automaticamente
        document.querySelectorAll('.editable-price').forEach(el => {
            el.addEventListener('input', () => {
                const id = el.dataset.priceId;
                if (servicosSelecionados.has(id)) {
                    const item = servicosSelecionados.get(id);
                    item.preco = parsePreco(el.textContent);
                    servicosSelecionados.set(id, item);
                    atualizarResumo();
                }
            });
        });

        // Atualizar painel de resumo e ficha de agendamento
        function atualizarResumo() {
            const listaEl = document.getElementById('selected-services-list');
            const bookingSection = document.getElementById('agendamento');
            let total = 0;

            if (servicosSelecionados.size === 0) {
                listaEl.innerHTML = `
                    <li class="text-xs italic text-charcoal-800/60 py-3 px-3 bg-cream-50 rounded-xl border border-dashed border-cream-300 text-center">
                        Nenhum serviço selecionado ainda. Clique em "+ Selecionar" no catálogo acima.
                    </li>
                `;
                bookingSection.classList.add('empty-booking');
            } else {
                bookingSection.classList.remove('empty-booking');
                listaEl.innerHTML = '';
                servicosSelecionados.forEach((item) => {
                    total += item.preco;
                    const li = document.createElement('li');
                    li.className = 'flex items-center justify-between py-2 px-3 rounded-xl bg-cream-50 border border-cream-200 text-xs sm:text-sm';
                    li.innerHTML = `
                        <span class="font-medium text-charcoal-900 pr-2">${item.nome}</span>
                        <div class="flex items-center gap-2.5 shrink-0">
                            <span class="font-semibold text-rosegold-700">${formatarBRL(item.preco)}</span>
                            <button onclick="removerItemResumo('${item.id}')" title="Remover" class="no-print text-charcoal-800/40 hover:text-red-500 transition-colors cursor-pointer">
                                <i class="fa-solid fa-xmark"></i>
                            </button>
                        </div>
                    `;
                    listaEl.appendChild(li);
                });
            }

            // Atualizar totais e sinal (30% a 50%)
            document.getElementById('summary-total').textContent = formatarBRL(total);
            const sinalMin = total * 0.30;
            const sinalMax = total * 0.50;
            document.getElementById('summary-deposit').textContent = `${formatarBRL(sinalMin)} – ${formatarBRL(sinalMax)}`;

            // Atualizar dados do cliente
            const nome = document.getElementById('client-name').value.trim();
            const phone = document.getElementById('client-phone').value.trim();
            const modalityEl = document.querySelector('input[name="modality"]:checked');
            const modality = modalityEl ? modalityEl.value : 'No Studio (Altamira - PA)';
            const dateVal = document.getElementById('booking-date').value;
            const timeVal = document.getElementById('booking-time').value;
            const notes = document.getElementById('booking-notes').value.trim();

            document.getElementById('summary-name').textContent = nome || 'Não informado';
            document.getElementById('summary-phone').textContent = phone || 'Não informado';
            document.getElementById('summary-modality').textContent = modality;

            let dataFormatada = 'A combinar';
            if (dateVal) {
                const partes = dateVal.split('-');
                dataFormatada = `${partes[2]}/${partes[1]}/${partes[0]} • ${timeVal}`;
            } else if (timeVal) {
                dataFormatada = `Data a combinar • ${timeVal}`;
            }
            document.getElementById('summary-datetime').textContent = dataFormatada;

            const notesRow = document.getElementById('summary-notes-row');
            if (notes) {
                notesRow.classList.remove('hidden');
                document.getElementById('summary-notes').textContent = notes;
            } else {
                notesRow.classList.add('hidden');
            }

            // Se o usuário preencheu nome ou selecionou serviço, exibe a seção na impressão
            if (nome || servicosSelecionados.size > 0) {
                bookingSection.classList.remove('empty-booking');
            }
        }

        // Remover item diretamente pelo resumo
        function removerItemResumo(priceId) {
            const btn = document.querySelector(`button[onclick*="'${priceId}'"]`);
            if (btn) {
                btn.click();
            } else {
                servicosSelecionados.delete(priceId);
                atualizarResumo();
            }
        }

        // Construir mensagem formatada para WhatsApp / Área de Transferência
        function gerarTextoMensagem() {
            const nome = document.getElementById('client-name').value.trim() || 'Cliente';
            const phone = document.getElementById('client-phone').value.trim();
            const modality = document.querySelector('input[name="modality"]:checked')?.value || 'No Studio';
            const dateVal = document.getElementById('booking-date').value;
            const timeVal = document.getElementById('booking-time').value;
            const notes = document.getElementById('booking-notes').value.trim();

            let dataStr = 'A combinar';
            if (dateVal) {
                const [ano, mes, dia] = dateVal.split('-');
                dataStr = `${dia}/${mes}/${ano}`;
            }

            let listaServicosStr = '';
            let total = 0;
            if (servicosSelecionados.size > 0) {
                servicosSelecionados.forEach(item => {
                    listaServicosStr += `• ${item.nome} (${formatarBRL(item.preco)})\n`;
                    total += item.preco;
                });
            } else {
                listaServicosStr = '• Gostaria de consultar disponibilidade de serviços\n';
            }

            let msg = `Olá, *Studio Gabriele Machado*! ✨\nGostaria de solicitar um pré-agendamento:\n\n`;
            msg += `*Nome:* ${nome}\n`;
            if (phone) msg += `*WhatsApp:* ${phone}\n`;
            msg += `*Modalidade:* ${modality}\n`;
            msg += `*Data Preferida:* ${dataStr}\n`;
            msg += `*Turno/Horário:* ${timeVal}\n\n`;
            msg += `*Procedimentos:*\n${listaServicosStr}\n`;
            if (total > 0) {
                msg += `*Estimativa Total:* ${formatarBRL(total)}\n`;
                msg += `_(Ciente da reserva mediante sinal de 30% a 50%)_\n`;
            }
            if (notes) {
                msg += `\n*Observações:* ${notes}`;
            }

            return msg;
        }

        // Copiar texto para a área de transferência (compatível com iframes)
        function copiarMensagem() {
            const texto = gerarTextoMensagem();
            const textarea = document.createElement('textarea');
            textarea.value = texto;
            textarea.style.position = 'fixed';
            textarea.style.opacity = '0';
            document.body.appendChild(textarea);
            textarea.select();
            try {
                document.execCommand('copy');
                mostrarToast('Resumo do agendamento copiado!');
            } catch (err) {
                mostrarToast('Não foi possível copiar automaticamente.', 'aviso');
            }
            document.body.removeChild(textarea);
        }

        // Redirecionar para o WhatsApp com mensagem pronta
        function enviarWhatsApp() {
            if (servicosSelecionados.size === 0 && !document.getElementById('client-name').value.trim()) {
                mostrarToast('Selecione pelo menos um serviço ou informe seu nome antes de enviar.', 'aviso');
                return;
            }
            const texto = encodeURIComponent(gerarTextoMensagem());
            const url = `https://wa.me/${STUDIO_WHATSAPP}?text=${texto}`;
            window.open(url, '_blank');
        }

        // Acionar impressão limpa / Exportação em PDF
        function exportarPDF() {
            // Garante que todas as categorias estejam visíveis no PDF completo
            filtrarCategoria('todos');
            setTimeout(() => {
                window.print();
            }, 150);
        }

        // Definir data mínima no seletor de data como hoje
        window.addEventListener('DOMContentLoaded', () => {
            const hoje = new Date().toISOString().split('T')[0];
            const dateInput = document.getElementById('booking-date');
            if (dateInput) dateInput.min = hoje;
        });
    </script>
</body>
</html>
```
