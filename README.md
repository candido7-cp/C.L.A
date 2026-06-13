<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo de Produtos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .bg-gym {
                background-image: url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
                position: relative;
            }
            .bg-overlay {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background-color: rgba(0, 0, 0, 0.85);
                z-index: 1;
            }
            .content-wrapper {
                position: relative;
                z-index: 2;
            }
            .category-card {
                @apply bg-white/10 backdrop-blur-md rounded-2xl border border-white/20 overflow-hidden transition-all duration-500;
            }
            .product-item {
                @apply flex justify-between items-center py-4 px-4 bg-white/90 rounded-lg shadow-sm hover:bg-white transition-colors;
            }
            .qty-btn {
                @apply w-8 h-8 flex items-center justify-center rounded-full font-bold text-white transition-colors;
            }
            .info-item {
                @apply border-b border-gray-200 pb-4 last:border-0;
            }
            .info-btn {
                @apply w-full text-left flex justify-between items-center py-3 text-xl font-bold text-gray-800 hover:text-green-600 transition-colors;
            }
            .info-content {
                @apply mt-2 text-gray-700 leading-relaxed text-base pl-2 whitespace-pre-line;
            }
        }
    </style>
</head>
<body class="font-inter bg-gym">

    <div class="bg-overlay"></div>

    <div class="content-wrapper">
        <!-- Cabeçalho -->
        <header class="bg-transparent py-8">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h1 class="text-5xl font-bold text-white mb-2">Catálogo de Produtos</h1>
                <p class="text-gray-300 text-lg">Adicione os itens que deseja e finalize o pedido</p>
            </div>
        </header>

        <!-- Conteúdo Principal -->
        <main class="max-w-4xl mx-auto px-4 pb-16 sm:px-6 lg:px-8">
            
            <!-- Categoria 1: Landerlan -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('landerlan')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Landerlan</h2>
                    <span id="icon-landerlan" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="landerlan" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-landerlan">
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enan 220</span>
                                <span class="text-green-600 font-bold mt-1">$ 220,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Dura 220</span>
                                <span class="text-green-600 font-bold mt-1">$ 220,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Deca 220</span>
                                <span class="text-green-600 font-bold mt-1">$ 220,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Master 220</span>
                                <span class="text-green-600 font-bold mt-1">$ 220,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enantato de trembo 220</span>
                                <span class="text-green-600 font-bold mt-1">$ 220,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Hemogenin</span>
                                <span class="text-green-600 font-bold mt-1">$ 170,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Oxan 5mg</span>
                                <span class="text-green-600 font-bold mt-1">$ 260,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Categoria 2: Neopharma -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('neopharma')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Neopharma</h2>
                    <span id="icon-neopharma" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="neopharma" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-neopharma">
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">durateston 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enantato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Deca 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Cipionato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Próprionato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Trenbolona acetato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enantato de trenbolona 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Stanozolol 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Emoginin 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 170,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Stanasolol 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Categoria 3: Max -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('max')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Max</h2>
                    <span id="icon-max" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="max" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-3" id="list-max">
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">durateston 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Stanozolol 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enantato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Deca 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Cipionato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Próprionato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Trenbolona acetato 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Enantato de trenbolona 💉</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Emoginin 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Stanasolol 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 180,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Oxan 10mg 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 170,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="flex flex-col">
                                <span class="text-lg font-medium text-gray-800">Oxan 20mg 💊</span>
                                <span class="text-green-600 font-bold mt-1">$ 200,00</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <button onclick="changeQty(this, -1)" class="qty-btn bg-red-500 hover:bg-red-600">-</button>
                                <span class="qty font-bold w-6 text-center">0</span>
                                <button onclick="changeQty(this, 1)" class="qty-btn bg-green-500 hover:bg-green-600">+</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Categoria: INFORMATIVO -->
            <div class="category-card mb-8">
                <button onclick="toggleCategory('informativo')" class="w-full px-6 py-5 flex justify-between items-center text-white hover:bg-white/5 transition-colors">
                    <h2 class="text-3xl font-bold">Informativo</h2>
                    <span id="icon-informativo" class="text-2xl transition-transform duration-500">+</span>
                </button>
                <div id="informativo" class="hidden bg-white/95 rounded-b-2xl p-6">
                    <div class="space-y-4">
                        
                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Durateston
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Aumento significativo da massa muscular magra
• Melhora da força e resistência física
• Aceleração da recuperação muscular
• Aumento da libido e disposição
• Combate o catabolismo (perda de músculo)
• Efeito rápido e de longa duração
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Enantato
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ganho de massa muscular de forma consistente
• Aumento da força e performance nos treinos
• Maior volume e vascularização muscular
• Melhora da densidade óssea
• Ação prolongada no organismo
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Stanozolol
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Definição muscular avançada, aspecto seco e denso
• Reduz a retenção de líquidos e gordura
• Aumento da força e resistência
• Melhora da vascularização
• Não aromatiza
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Deca
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ganho de massa muscular sólida
• Aumento da força e resistência
• Excelente proteção das articulações
• Estimula produção de colágeno
• Baixa atividade estrogênica
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Cipionato
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ganho de massa magra gradual
• Aumento de força e resistência
• Ação prolongada, níveis estáveis
• Menor frequência de aplicações
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Propionato
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ação rápida, resultados visíveis rápido
• Ganho de massa magra e qualidade
• Menor retenção de líquidos
• Ideal para ciclos curtos
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Trembolona Acetato
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ação anabólica extremamente potente
• Aumento explosivo da força
• Definição máxima, seco e duro
• Queima de gordura acelerada
• Não aromatiza
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Enantato de Trembolona
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Potente ação anabólica
• Aumento de força e resistência
• Definição muscular superior
• Reduz gordura corporal
• Efeito prolongado
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Hemogenin / Emoginin
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Ação anabólica extremamente potente
• Aumento rápido de força e peso
• Estimula glóbulos vermelhos
• Resultados rápidos
                            </div>
                        </div>

                        <div class="info-item">
                            <button onclick="toggleInfo(this)" class="info-btn">
                                Oxandrolona (Oxan)
                                <span class="text-sm transition-transform duration-300">▼</span>
                            </button>
                            <div class="info-content hidden">
• Definição muscular de alta qualidade
• Preserva massa magra em déficit calórico
• Aumento de força sem volume excessivo
• Baixa retenção de líquidos
                            </div>
                        </div>

                    </div>
                </div>
            </div>

            <!-- Botão Finalizar -->
            <div class="text-center mt-10">
                <button onclick="finalizarPedido()" class="bg-green-500 hover:bg-green-600 text-white font-bold py-4 px-10 rounded-full text-xl shadow-lg transform hover:scale-105 transition-all">
                    ✅ FINALIZAR PEDIDO
                </button>
            </div>

        </main>
    </div>

    <script>
        function toggleCategory(id) {
            const content = document.getElementById(id);
            const icon = document.getElementById('icon-' + id);
            
            content.classList.toggle('hidden');
            
            if(content.classList.contains('hidden')) {
                icon.innerHTML = '+';
                icon.style.transform = 'rotate(0deg)';
            } else {
                icon.innerHTML = '−';
                icon.style.transform = 'rotate(180deg)';
            }
        }

        function changeQty(button, delta) {
            const item = button.parentElement;
            const qtySpan = item.querySelector('.qty');
            let qty = parseInt(qtySpan.innerText);
            
            qty += delta;
            if(qty < 0) qty = 0;
            
            qtySpan.innerText = qty;
        }

        function toggleInfo(button) {
            const content = button.nextElementSibling;
            const icon = button.querySelector('span:last-child');
            
            content.classList.toggle('hidden');
            
            if(content.classList.contains('hidden')) {
                icon.style.transform = 'rotate(0deg)';
            } else {
                icon.style.transform = 'rotate(180deg)';
            }
        }

        function finalizarPedido() {
            let mensagem = "*🛒 PEDIDO REALIZADO*\n\n";
            let totalGeral = 0;
            let totalItens = 0;

            function lerCategoria(nome, id) {
                const lista = document.getElementById(id);
                const items = lista.querySelectorAll('.product-item');
                let temItem = false;
                let categoriaTexto = `*📦 ${nome}*\n`;

                items.forEach(item => {
                    const nomeProd = item.querySelector('.flex-col span:first-child').innerText;
                    const precoTexto = item.querySelector('.text-green-600').innerText;
                    const qty = parseInt(item.querySelector('.qty').innerText);
                    
                    if(qty > 0) {
                        temItem = true;
                        totalItens += qty;
                        const preco = parseFloat(precoTexto.replace('$ ', '').replace('.', '').replace(',', '.'));
                        const totalItem = preco * qty;
                        totalGeral += totalItem;
                        
                        categoriaTexto += `${qty}x - ${nomeProd} - ${precoTexto}\n`;
                    }
                });

                if(temItem) {
                    mensagem += categoriaTexto + "\n";
                }
            }

            lerCategoria('Landerlan', 'list-landerlan');
            lerCategoria('Neopharma', 'list-neopharma');
            lerCategoria('Max', 'list-max');

            if(totalGeral === 0) {
                alert('Adicione pelo menos um item antes de finalizar!');
                return;
            }

            mensagem += `*🧾 Total de Itens: ${totalItens}*\n`;
            mensagem += `*💵 Valor Total: $ ${totalGeral.toFixed(2).replace('.', ',')}*\n\n`;
            mensagem += `📲 *Pagamento via PIX*\n`;
            mensagem += `Chave PIX: 85996640269\n`;
            mensagem += `Nome: Maria Edileuda Cândido Cosmo\n\n`;
            mensagem += `Favor enviar o comprovante! ✅`;

            const mensagemCodificada = encodeURIComponent(mensagem);
            const numeroWhatsapp = "5585920076331";
            const link = `https://wa.me/${numeroWhatsapp}?text=${mensagemCodificada}`;

            window.open(link, '_blank');
        }
    </script>

</body>
</html>
