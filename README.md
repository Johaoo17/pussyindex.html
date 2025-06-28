
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Explorando el Mundo de los Celulares</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Estilos personalizados */
        .phone-card {
            transition: all 0.3s ease;
            transform-style: preserve-3d;
        }
        .phone-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .info-panel {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out;
        }
        .specs-table {
            display: none;
            animation: fadeIn 0.5s;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .comparison-mode .phone-card {
            width: 45%;
            margin: 0 2.5%;
        }
    </style>
</head>
<body class="bg-gray-100 font-sans">
    <header class="bg-gradient-to-r from-blue-600 to-purple-600 text-white py-8 px-4">
        <div class="container mx-auto">
            <h1 class="text-4xl font-bold mb-4">Evolución de los Dispositivos Celulares</h1>
            <p class="text-xl max-w-2xl">Descubre la fascinante historia, tecnología y características de los smartphones modernos</p>
        </div>
    </header>

    <main class="container mx-auto py-8 px-4">
        <!-- Filtros y controles -->
        <section class="mb-12 bg-white rounded-lg shadow-md p-6">
            <div class="flex flex-wrap justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h2 class="text-xl font-semibold mb-2">Filtrar por:</h2>
                    <div class="flex flex-wrap gap-2">
                        <button class="filter-btn bg-blue-100 text-blue-800 px-4 py-2 rounded-full hover:bg-blue-200 transition" data-filter="all">Todos</button>
                        <button class="filter-btn bg-green-100 text-green-800 px-4 py-2 rounded-full hover:bg-green-200 transition" data-filter="gama-alta">Gama Alta</button>
                        <button class="filter-btn bg-yellow-100 text-yellow-800 px-4 py-2 rounded-full hover:bg-yellow-200 transition" data-filter="gama-media">Gama Media</button>
                        <button class="filter-btn bg-purple-100 text-purple-800 px-4 py-2 rounded-full hover:bg-purple-200 transition" data-filter="plegables">Plegables</button>
                    </div>
                </div>
                <button id="comparison-toggle" class="bg-gray-800 text-white px-6 py-2 rounded-lg hover:bg-gray-700 transition">
                    Modo Comparación
                </button>
            </div>
        </section>

        <!-- Sección de celulares -->
        <section id="phones-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Celular 1 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="gama-alta">
                <div class="relative">
                    <img src="https://placehold.co/600x400/3b82f6/ffffff?text=iPhone+15+Pro" alt="iPhone 15 Pro en Space Black mostrando su diseño premium de bordes rectos y cámara triple" class="w-full h-64 object-contain" />
                    <div class="absolute top-2 right-2 bg-red-500 text-white text-xs font-bold px-2 py-1 rounded">NUEVO</div>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">iPhone 15 Pro</h3>
                    <p class="text-gray-600 mb-4">La culminación de la innovación de Apple con titanio aerospace-grade</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">El iPhone 15 Pro presenta el revolucionario chip A17 Pro, el primer procesador de 3nm en un smartphone, ofreciendo un rendimiento gráfico comparable a consolas portátiles.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <span class="text-gray-500">Pantalla:</span>
                                <span>6.1" Super Retina XDR, 120Hz</span>
                                <span class="text-gray-500">Procesador:</span>
                                <span>A17 Pro (6 núcleos)</span>
                                <span class="text-gray-500">Memoria:</span>
                                <span>8GB RAM</span>
                                <span class="text-gray-500">Almacenamiento:</span>
                                <span>128GB-1TB</span>
                                <span class="text-gray-500">Cámaras:</span>
                                <span>Triple 48MP+12MP+12MP</span>
                                <span class="text-gray-500">Batería:</span>
                                <span>3274 mAh</span>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold">$999</span>
                            <button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700 transition">
                                Comprar Ahora
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celular 2 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="gama-alta">
                <div class="relative">
                    <img src="https://placehold.co/600x400/4285f4/ffffff?text=Galaxy+S23+Ultra" alt="Samsung Galaxy S23 Ultra en Phantom Black mostrando su pantalla curva y cámara de 200MP" class="w-full h-64 object-contain" />
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">Galaxy S23 Ultra</h3>
                    <p class="text-gray-600 mb-4">El poder definitivo con cámara de 200MP y S Pen integrado</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">El buque insignia de Samsung destaca por su sensor de cámara de 200MP, pantalla Dynamic AMOLED 2X de 120Hz adaptable y el exclusivo S Pen que lo convierte en un híbrido perfecto entre smartphone y tableta.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <span class="text-gray-500">Pantalla:</span>
                                <span>6.8" Dynamic AMOLED 2X, 120Hz</span>
                                <span class="text-gray-500">Procesador:</span>
                                <span>Snapdragon 8 Gen 2</span>
                                <span class="text-gray-500">Memoria:</span>
                                <span>12GB RAM</span>
                                <span class="text-gray-500">Almacenamiento:</span>
                                <span>256GB-1TB</span>
                                <span class="text-gray-500">Cámaras:</span>
                                <span>200MP+12MP+10MP+10MP</span>
                                <span class="text-gray-500">Batería:</span>
                                <span>5000 mAh</span>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold">$1,199</span>
                            <button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700 transition">
                                Comprar Ahora
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celular 3 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="plegables">
                <div class="relative">
                    <img src="https://placehold.co/600x400/ea4335/ffffff?text=Galaxy+Z+Fold+5" alt="Samsung Galaxy Z Fold 5 abierto mostrando su pantalla interior de tablet y bisagra sin gap" class="w-full h-64 object-contain" />
                    <div class="absolute top-2 right-2 bg-yellow-500 text-white text-xs font-bold px-2 py-1 rounded">INNOVACIÓN</div>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">Galaxy Z Fold 5</h3>
                    <p class="text-gray-600 mb-4">El futuro plegable con bisagra sin espacio y doble pantalla</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">Este dispositivo revolucionario combina un smartphone convencional de 6.2" con una tableta de 7.6" gracias a su innovadora bisagra sin espacio, ofreciendo una experiencia multitarea incomparable.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <span class="text-gray-500">Pantalla exterior:</span>
                                <span>6.2" Dynamic AMOLED 2X, 120Hz</span>
                                <span class="text-gray-500">Pantalla interior:</span>
                                <span>7.6" Dynamic AMOLED 2X, 120Hz</span>
                                <span class="text-gray-500">Procesador:</span>
                                <span>Snapdragon 8 Gen 2</span>
                                <span class="text-gray-500">Memoria:</span>
                                <span>12GB RAM</span>
                                <span class="text-gray-500">Almacenamiento:</span>
                                <span>256GB-1TB</span>
                                <span class="text-gray-500">Cámaras:</span>
                                <span>50MP+12MP+10MP</span>
                                <span class="text-gray-500">Batería:</span>
                                <span>4400 mAh</span>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold">$1,799</span>
                            <button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700 transition">
                                Comprar Ahora
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celular 4 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="gama-media">
                <div class="relative">
                    <img src="https://placehold.co/600x400/34a853/ffffff?text=Pixel+7a" alt="Google Pixel 7a en Coral mostrando su diseño limpio y cámara en barra" class="w-full h-64 object-contain" />
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">Pixel 7a</h3>
                    <p class="text-gray-600 mb-4">La mejor cámara en gama media con Tensor G2</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">El Pixel 7a ofrece calidad de fotografía profesional gracias a su software de procesamiento avanzado y el chip Tensor G2, todo en un paquete de gama media con construcción premium.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <span class="text-gray-500">Pantalla:</span>
                                <span>6.1" OLED, 90Hz</span>
                                <span class="text-gray-500">Procesador:</span>
                                <span>Google Tensor G2</span>
                                <span class="text-gray-500">Memoria:</span>
                                <span>8GB RAM</span>
                                <span class="text-gray-500">Almacenamiento:</span>
                                <span>128GB</span>
                                <span class="text-gray-500">Cámaras:</span>
                                <span>64MP+12MP</span>
                                <span class="text-gray-500">Batería:</span>
                                <span>4385 mAh</span>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold">$499</span>
                            <button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700 transition">
                                Comprar Ahora
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celular 5 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="gama-media">
                <div class="relative">
                    <img src="https://placehold.co/600x400/fbbc04/ffffff?text=Redmi+Note+12+Pro+" alt="Xiaomi Redmi Note 12 Pro+ en Onyx Gray mostrando su pantalla AMOLED y cámara de 200MP" class="w-full h-64 object-contain" />
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">Redmi Note 12 Pro+</h3>
                    <p class="text-gray-600 mb-4">Potencia y valor con carga rápida de 120W</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">Xiaomi rompe barreras en la gama media con este dispositivo que incluye carga ultrarrápida de 120W, pantalla AMOLED de 120Hz y una cámara principal de 200MP con OIS.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <span class="text-gray-500">Pantalla:</span>
                                <span>6.67" AMOLED, 120Hz</span>
                                <span class="text-gray-500">Procesador:</span>
                                <span>Dimensity 1080</span>
                                <span class="text-gray-500">Memoria:</span>
                                <span>8GB RAM</span>
                                <span class="text-gray-500">Almacenamiento:</span>
                                <span>256GB</span>
                                <span class="text-gray-500">Cámaras:</span>
                                <span>200MP+8MP+2MP</span>
                                <span class="text-gray-500">Batería:</span>
                                <span>5000 mAh</span>
                            </div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold">$399</span>
                            <button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700 transition">
                                Comprar Ahora
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Celular 6 -->
            <div class="phone-card bg-white rounded-xl shadow-md overflow-hidden" data-category="plegables">
                <div class="relative">
                    <img src="https://placehold.co/600x400/ff6d01/ffffff?text=Oppo+Find+N2+Flip" alt="Oppo Find N2 Flip en negro mostrando su pantalla plegable vertical y gran display externo" class="w-full h-64 object-contain" />
                    <div class="absolute top-2 right-2 bg-purple-500 text-white text-xs font-bold px-2 py-1 rounded">TENDENCIA</div>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold mb-2">Oppo Find N2 Flip</h3>
                    <p class="text-gray-600 mb-4">El clamshell plegable con pantalla exterior más útil</p>
                    
                    <button class="toggle-info-btn bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition w-full mb-3">
                        Mostrar Detalles
                    </button>
                    
                    <div class="info-panel">
                        <p class="text-gray-700 mb-3">Oppo reinventa el formato flip con una enorme pantalla exterior de 3.26" que permite interactuar completamente con el dispositivo sin necesidad de abrirlo, junto con una bisagra que resiste más de 400,000 pliegues.</p>
                        
                        <button class="toggle-specs-btn text-blue-600 text-sm font-medium mb-3">
                            Ver Especificaciones Técnicas ↓
                        </button>
                        
                        <div class="specs-table text-sm">
                            <div class="grid grid-cols-2 gap-2 mb-3">
