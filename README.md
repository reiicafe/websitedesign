<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reii Cafe | Premium Coffee & Resto</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; background-color: #0f172a; color: #f8fafc; }
        .serif { font-family: 'Playfair Display', serif; }
        .glass { background: rgba(255, 255, 255, 0.05); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.1); }
        .card-zoom:hover img { transform: scale(1.1); }
    </style>
</head>
<body>

    <nav class="p-6 flex justify-between items-center sticky top-0 z-50 glass">
        <h1 class="text-2xl font-bold tracking-widest text-amber-500 serif">REII CAFE</h1>
        <div class="space-x-6 hidden md:flex">
            <a href="#menu" class="hover:text-amber-500 transition">Menu</a>
            <a href="#qr" class="hover:text-amber-500 transition">Scan QR</a>
            <span class="text-gray-400">www.reiicafe.com</span>
        </div>
    </nav>

    <header class="py-20 text-center">
        <h2 class="text-5xl md:text-7xl serif mb-4">Savor Every Sip</h2>
        <p class="text-gray-400 max-w-lg mx-auto">Menyajikan kopi pilihan dan hidangan autentik dalam suasana yang tenang dan elegan.</p>
    </header>

    <section id="menu" class="max-w-6xl mx-auto px-6 py-12">
        <h3 class="text-3xl serif mb-10 border-b border-amber-500 inline-block">Signature Menu</h3>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="glass rounded-2xl overflow-hidden card-zoom">
                <div class="h-64 overflow-hidden">
                    <img src="https://images.unsplash.com/photo-1551028150-64b9f398f678?auto=format&fit=crop&w=800&q=80" alt="Americano" class="w-full h-full object-cover transition duration-500">
                </div>
                <div class="p-6">
                    <h4 class="text-xl font-semibold mb-2">Americano Heritage</h4>
                    <p class="text-sm text-gray-400 mb-4">Espresso murni dengan air pegunungan yang segar.</p>
                    <div class="flex justify-between items-center">
                        <span class="text-amber-500 font-bold text-lg">Rp 25.000</span>
                        <a href="https://wa.me/628123456789?text=halo%20saya%20ingin%20memesan%20minuman%20americano" class="bg-amber-600 hover:bg-amber-700 px-4 py-2 rounded-full text-sm font-semibold transition">Pesan Sekarang</a>
                    </div>
                </div>
            </div>

            <div class="glass rounded-2xl overflow-hidden card-zoom">
                <div class="h-64 overflow-hidden">
                    <img src="https://images.unsplash.com/photo-1515823064-d6e0c04616a7?auto=format&fit=crop&w=800&q=80" alt="Matcha" class="w-full h-full object-cover transition duration-500">
                </div>
                <div class="p-6">
                    <h4 class="text-xl font-semibold mb-2">Kyoto Matcha Latte</h4>
                    <p class="text-sm text-gray-400 mb-4">Matcha autentik Jepang dengan susu lembut.</p>
                    <div class="flex justify-between items-center">
                        <span class="text-amber-500 font-bold text-lg">Rp 32.000</span>
                        <button class="bg-amber-600 hover:bg-amber-700 px-4 py-2 rounded-full text-sm font-semibold transition cursor-not-allowed opacity-50">Tersedia</button>
                    </div>
                </div>
            </div>

            <div class="glass rounded-2xl overflow-hidden card-zoom">
                <div class="h-64 overflow-hidden">
                    <img src="https://images.unsplash.com/photo-1555507036-ab1f4038808a?auto=format&fit=crop&w=800&q=80" alt="Croissant" class="w-full h-full object-cover transition duration-500">
                </div>
                <div class="p-6">
                    <h4 class="text-xl font-semibold mb-2">Butter Croissant</h4>
                    <p class="text-sm text-gray-400 mb-4">Pastry berlapis yang renyah dan kaya akan mentega.</p>
                    <div class="flex justify-between items-center">
                        <span class="text-amber-500 font-bold text-lg">Rp 28.000</span>
                        <button class="bg-amber-600 hover:bg-amber-700 px-4 py-2 rounded-full text-sm font-semibold transition cursor-not-allowed opacity-50">Tersedia</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="qr" class="max-w-4xl mx-auto px-6 py-20 text-center">
        <div class="glass p-10 rounded-3xl border-2 border-dashed border-amber-500/50">
            <h3 class="text-3xl serif mb-6">Scan to Order Online</h3>
            <p class="text-gray-400 mb-8">Akses menu lengkap kami langsung dari smartphone Anda melalui URL www.reiicafe.com</p>
            
            <div class="flex flex-col md:flex-row justify-center items-center gap-10">
                <div class="bg-white p-4 rounded-xl shadow-xl">
                    <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://www.reiicafe.com" alt="QR Code Reii Cafe" class="w-48 h-48">
                    <p class="text-black text-xs mt-2 font-bold uppercase tracking-widest">QR CODE MENU</p>
                </div>

                <div class="bg-white p-4 rounded-xl shadow-xl flex flex-col items-center">
                    <img src="https://bwipjs-api.metafloor.com/?bcid=code128&text=REIICAFE2024&scale=3&rotate=N&includetext" alt="Barcode" class="h-24 w-64 object-contain">
                    <p class="text-black text-[10px] mt-2 font-mono">REII-CAFE-ONLINE-MEMBER</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-10 text-center text-gray-500 text-sm border-t border-white/5">
        <p>&copy; 2024 Reii Cafe. All Rights Reserved. <br> Visit us at <span class="text-amber-500">www.reiicafe.com</span></p>
    </footer>

</body>
</html>
