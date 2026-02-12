<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reii Cafe - Premium Coffee & Pastry</title>
    
    <!-- Menggunakan Tailwind CSS untuk Desain -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome untuk Ikon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts: Playfair Display (Elegan) & Lato (Modern) -->
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        coffee: {
                            50: '#fdf8f6',
                            100: '#f2e8e5',
                            200: '#eaddd7',
                            500: '#b79891',
                            800: '#5d4037',
                            900: '#3e2723',
                        },
                        gold: '#d4af37'
                    },
                    fontFamily: {
                        sans: ['Lato', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Styles */
        body {
            background-color: #fdf8f6;
        }
        .glass-effect {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
        }
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
        }
        /* Hide scrollbar for category selector */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="text-coffee-900 antialiased">

    <!-- NAVIGATION -->
    <nav class="fixed w-full z-50 glass-effect border-b border-coffee-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center gap-2 cursor-pointer" onclick="window.scrollTo(0,0)">
                    <i class="fas fa-coffee text-2xl text-coffee-800"></i>
                    <span class="font-serif font-bold text-xl tracking-wide text-coffee-900">Reii Cafe</span>
                </div>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#menu" class="text-coffee-800 hover:text-gold transition">Menu</a>
                    <a href="#scan" class="text-coffee-800 hover:text-gold transition">Scan QR</a>
                    <a href="#guestbook" class="text-coffee-800 hover:text-gold transition">Buku Tamu</a>
                    <a href="https://www.reiicafe.com" target="_blank" class="px-4 py-2 bg-coffee-800 text-white rounded-full hover:bg-coffee-900 transition text-sm">
                        www.reiicafe.com
                    </a>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button onclick="toggleMobileMenu()" class="text-coffee-800 focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Panel -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t border-coffee-100 absolute w-full shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#menu" class="block px-3 py-2 rounded-md text-base font-medium text-coffee-800 hover:bg-coffee-50">Menu</a>
                <a href="#scan" class="block px-3 py-2 rounded-md text-base font-medium text-coffee-800 hover:bg-coffee-50">Scan QR</a>
                <a href="#guestbook" class="block px-3 py-2 rounded-md text-base font-medium text-coffee-800 hover:bg-coffee-50">Buku Tamu</a>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <header class="relative pt-24 pb-12 lg:pt-32 lg:pb-24 flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0 z-0 opacity-20">
            <img src="https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80" alt="Cafe Background" class="w-full h-full object-cover">
        </div>
        <div class="relative z-10 text-center px-4 max-w-4xl mx-auto">
            <span class="text-gold font-bold tracking-widest uppercase text-sm mb-2 block">Premium Coffee & Roastery</span>
            <h1 class="font-serif text-5xl md:text-6xl font-bold text-coffee-900 mb-6 leading-tight">
                Nikmati Momen Terbaik<br>di <span class="text-coffee-800 italic">Reii Cafe</span>
            </h1>
            <p class="text-lg text-coffee-800 mb-8 max-w-2xl mx-auto">
                Kopi pilihan terbaik dan hidangan lezat yang disajikan dengan penuh cinta. Pesan sekarang melalui website kami.
            </p>
            <a href="#menu" class="inline-block bg-coffee-800 text-white px-8 py-3 rounded-full font-semibold shadow-lg hover:bg-coffee-900 transition transform hover:-translate-y-1">
                Lihat Menu & Pesan
            </a>
            <p class="mt-4 text-sm text-coffee-500 font-semibold">www.reiicafe.com</p>
        </div>
    </header>

    <!-- MENU SECTION -->
    <section id="menu" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="font-serif text-3xl font-bold text-coffee-900">Menu Favorit Kami</h2>
                <div class="w-24 h-1 bg-gold mx-auto mt-4 rounded-full"></div>
            </div>

            <!-- Category Filter -->
            <div class="flex justify-center space-x-2 md:space-x-4 mb-10 overflow-x-auto no-scrollbar py-2">
                <button onclick="filterMenu('all')" class="category-btn active px-6 py-2 rounded-full border border-coffee-800 text-coffee-800 hover:bg-coffee-800 hover:text-white transition whitespace-nowrap bg-coffee-800 text-white">Semua</button>
                <button onclick="filterMenu('coffee')" class="category-btn px-6 py-2 rounded-full border border-coffee-800 text-coffee-800 hover:bg-coffee-800 hover:text-white transition whitespace-nowrap">Kopi</button>
                <button onclick="filterMenu('non-coffee')" class="category-btn px-6 py-2 rounded-full border border-coffee-800 text-coffee-800 hover:bg-coffee-800 hover:text-white transition whitespace-nowrap">Non-Kopi</button>
                <button onclick="filterMenu('food')" class="category-btn px-6 py-2 rounded-full border border-coffee-800 text-coffee-800 hover:bg-coffee-800 hover:text-white transition whitespace-nowrap">Makanan</button>
            </div>

            <!-- Menu Grid -->
            <div id="menu-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Menu Items will be injected here by JS -->
            </div>
        </div>
    </section>

    <!-- QR CODE & BARCODE SECTION -->
    <section id="scan" class="py-16 bg-coffee-50 border-t border-b border-coffee-200">
        <div class="max-w-4xl mx-auto px-4 text-center">
            <h2 class="font-serif text-3xl font-bold text-coffee-900 mb-4">Scan untuk Mengunjungi</h2>
            <p class="text-coffee-800 mb-8">Pindai kode di bawah ini untuk langsung membuka aplikasi web kami di perangkat lain.</p>
            
            <div class="bg-white p-8 rounded-2xl shadow-xl inline-block max-w-sm w-full relative">
                <div class="absolute -top-4 -left-4 w-12 h-12 border-t-4 border-l-4 border-gold rounded-tl-xl"></div>
                <div class="absolute -bottom-4 -right-4 w-12 h-12 border-b-4 border-r-4 border-gold rounded-br-xl"></div>
                
                <!-- QR Code (Generated via API) -->
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://www.reiicafe.com" alt="QR Code Reii Cafe" class="mx-auto mb-4 w-48 h-48">
                
                <!-- Mock Barcode -->
                <div class="h-12 bg-gray-800 mt-4 mb-2 w-full" style="background-image: repeating-linear-gradient(90deg, black, black 1px, white 1px, white 3px);"></div>
                
                <p class="font-mono text-sm tracking-widest text-gray-500 mt-2">WWW.REIICAFE.COM</p>
                <a href="https://www.reiicafe.com" target="_blank" class="mt-4 block w-full py-2 bg-gray-100 text-coffee-800 rounded-lg text-sm hover:bg-gray-200 transition">Buka Website</a>
            </div>
        </div>
    </section>

    <!-- GUESTBOOK SECTION -->
    <section id="guestbook" class="py-16 bg-white">
        <div class="max-w-3xl mx-auto px-4">
            <div class="text-center mb-10">
                <h2 class="font-serif text-3xl font-bold text-coffee-900">Buku Tamu</h2>
                <p class="text-gray-500 mt-2">Ceritakan pengalaman Anda di Reii Cafe</p>
            </div>

            <div class="bg-coffee-50 p-6 md:p-8 rounded-2xl shadow-sm border border-coffee-100">
                <form id="guestbook-form" class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-coffee-800 mb-1">Nama</label>
                        <input type="text" id="guest-name" required class="w-full px-4 py-2 rounded-lg border border-coffee-200 focus:outline-none focus:ring-2 focus:ring-coffee-500 bg-white" placeholder="Nama Anda">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-coffee-800 mb-1">Pesan / Kesan</label>
                        <textarea id="guest-message" rows="3" required class="w-full px-4 py-2 rounded-lg border border-coffee-200 focus:outline-none focus:ring-2 focus:ring-coffee-500 bg-white" placeholder="Tulis sesuatu..."></textarea>
                    </div>
                    <button type="submit" class="w-full bg-coffee-800 text-white py-2 rounded-lg hover:bg-coffee-900 transition font-semibold shadow-md">
                        Kirim Pesan
                    </button>
                </form>
            </div>

            <!-- List of Messages -->
            <div class="mt-10 space-y-4" id="messages-list">
                <!-- Example Entry -->
                <div class="p-4 rounded-xl border border-gray-100 bg-white shadow-sm flex gap-4">
                    <div class="w-10 h-10 rounded-full bg-coffee-100 flex items-center justify-center text-coffee-800 font-bold">R</div>
                    <div>
                        <h4 class="font-bold text-coffee-900 text-sm">Reii Admin</h4>
                        <p class="text-gray-600 text-sm mt-1">Selamat datang di Reii Cafe! Silakan tinggalkan pesan Anda di sini.</p>
                        <span class="text-xs text-gray-400 mt-2 block">Baru saja</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-coffee-900 text-white py-10">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <h2 class="font-serif text-2xl font-bold mb-2">Reii Cafe</h2>
            <p class="text-coffee-200 mb-6">Serving Happiness in Every Cup</p>
            <div class="flex justify-center space-x-6 mb-8">
                <a href="#" class="text-white hover:text-gold transition"><i class="fab fa-instagram text-xl"></i></a>
                <a href="#" class="text-white hover:text-gold transition"><i class="fab fa-whatsapp text-xl"></i></a>
                <a href="#" class="text-white hover:text-gold transition"><i class="fab fa-twitter text-xl"></i></a>
            </div>
            <p class="text-sm text-coffee-500">&copy; 2024 Reii Cafe. All rights reserved.</p>
            <p class="text-xs text-coffee-500 mt-1 font-mono">www.reiicafe.com</p>
        </div>
    </footer>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // 1. DATA MENU
        const menuItems = [
            {
                id: 1,
                name: "Americano",
                category: "coffee",
                price: "Rp 25.000",
                desc: "Espresso murni dengan tambahan air panas.",
                image: "https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 2,
                name: "Caffe Latte",
                category: "coffee",
                price: "Rp 32.000",
                desc: "Espresso lembut dengan susu steam yang creamy.",
                image: "https://images.unsplash.com/photo-1570968992193-6e5c96978d6c?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 3,
                name: "Caramel Macchiato",
                category: "coffee",
                price: "Rp 38.000",
                desc: "Perpaduan vanilla, espresso, susu dan saus karamel.",
                image: "https://images.unsplash.com/photo-1485808191679-5f8c7c83563e?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 4,
                name: "Matcha Latte",
                category: "non-coffee",
                price: "Rp 35.000",
                desc: "Bubuk matcha premium Jepang dengan susu segar.",
                image: "https://images.unsplash.com/photo-1515823064-d6e0c04616a7?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 5,
                name: "Chocolate Delight",
                category: "non-coffee",
                price: "Rp 30.000",
                desc: "Coklat Belgia panas atau dingin yang kaya rasa.",
                image: "https://images.unsplash.com/photo-1542990253-0d0f5be5f0ed?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 6,
                name: "Croissant Butter",
                category: "food",
                price: "Rp 22.000",
                desc: "Pastry renyah dengan aroma butter yang kuat.",
                image: "https://images.unsplash.com/photo-1555507036-ab1f40388085?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 7,
                name: "Nasi Goreng Reii",
                category: "food",
                price: "Rp 45.000",
                desc: "Nasi goreng spesial dengan sate ayam dan telur.",
                image: "https://images.unsplash.com/photo-1603133872878-684f208fb74b?auto=format&fit=crop&w=400&q=80"
            },
            {
                id: 8,
                name: "Beef Burger",
                category: "food",
                price: "Rp 55.000",
                desc: "Burger daging sapi premium dengan keju leleh.",
                image: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=400&q=80"
            },
             {
                id: 9,
                name: "Strawberry Cheesecake",
                category: "food",
                price: "Rp 35.000",
                desc: "Cheesecake lembut dengan topping selai strawberry.",
                image: "https://images.unsplash.com/photo-1565958011703-44f9829ba187?auto=format&fit=crop&w=400&q=80"
            }
        ];

        // 2. RENDER MENU
        const menuContainer = document.getElementById('menu-container');

        function displayMenu(items) {
            menuContainer.innerHTML = items.map(item => `
                <div class="bg-white rounded-xl shadow-sm border border-gray-100 overflow-hidden card-hover flex flex-col h-full">
                    <div class="h-48 overflow-hidden relative">
                        <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover transition duration-500 hover:scale-110">
                        <div class="absolute top-3 right-3 bg-white px-3 py-1 rounded-full text-xs font-bold text-coffee-800 shadow-md">
                            ${item.category.toUpperCase()}
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-grow">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-serif font-bold text-coffee-900">${item.name}</h3>
                            <span class="text-gold font-bold">${item.price}</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-6 flex-grow">${item.desc}</p>
                        
                        <!-- TOMBOL PESAN OTOMATIS -->
                        <button onclick="orderItem('${item.name}')" class="w-full bg-coffee-800 text-white py-3 rounded-lg hover:bg-gold hover:text-white transition flex items-center justify-center gap-2 group">
                            <span>Pesan Sekarang</span>
                            <i class="fab fa-whatsapp text-lg group-hover:rotate-12 transition"></i>
                        </button>
                    </div>
                </div>
            `).join('');
        }

        // 3. FITUR FILTER
        function filterMenu(category) {
            // Update tombol active
            const buttons = document.querySelectorAll('.category-btn');
            buttons.forEach(btn => {
                if(btn.getAttribute('onclick').includes(category)) {
                    btn.classList.add('bg-coffee-800', 'text-white');
                    btn.classList.remove('text-coffee-800');
                } else {
                    btn.classList.remove('bg-coffee-800', 'text-white');
                    btn.classList.add('text-coffee-800');
                }
            });

            if (category === 'all') {
                displayMenu(menuItems);
            } else {
                const filtered = menuItems.filter(item => item.category === category);
                displayMenu(filtered);
            }
        }

        // 4. LOGIKA PEMESANAN WHATSAPP
        function orderItem(itemName) {
            // Nomor HP Tujuan (Ganti dengan nomor cafe Anda)
            const phoneNumber = "6281234567890"; 
            
            // Format Pesan: "halo saya ingin memesan minuman americano"
            const message = `halo saya ingin memesan menu ${itemName}`;
            
            // Encode URL
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            
            // Buka di tab baru
            window.open(url, '_blank');
        }

        // 5. LOGIKA BUKU TAMU
        const guestForm = document.getElementById('guestbook-form');
        const messagesList = document.getElementById('messages-list');

        guestForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('guest-name').value;
            const msg = document.getElementById('guest-message').value;

            // Buat elemen baru
            const newEntry = document.createElement('div');
            newEntry.className = "p-4 rounded-xl border border-gray-100 bg-white shadow-sm flex gap-4 animate-fade-in";
            newEntry.innerHTML = `
                <div class="w-10 h-10 rounded-full bg-gold text-white flex items-center justify-center font-bold">
                    ${name.charAt(0).toUpperCase()}
                </div>
                <div>
                    <h4 class="font-bold text-coffee-900 text-sm">${name}</h4>
                    <p class="text-gray-600 text-sm mt-1">${msg}</p>
                    <span class="text-xs text-gray-400 mt-2 block">Baru saja</span>
                </div>
            `;

            // Tambahkan ke atas list
            messagesList.prepend(newEntry);

            // Reset form
            guestForm.reset();
            alert("Terima kasih telah mengisi buku tamu Reii Cafe!");
        });

        // 6. UTILS (Mobile Menu)
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // Initialize
        displayMenu(menuItems);
    </script>
</body>
</html>
