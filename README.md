<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tchatcha Faso - Petites annonces locales au Burkina Faso</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
        }
        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .announcement-card:hover {
            transform: scale(1.02);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .active-tab {
            border-bottom: 3px solid #f59e0b;
            font-weight: 600;
        }
        #mobileMenu {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Header -->
    <header class="gradient-bg text-white shadow-md">
        <div class="container mx-auto px-4 py-3">
            <div class="flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <i class="fas fa-bullhorn text-2xl"></i>
                    <h1 class="text-xl md:text-2xl font-bold">Tchatcha Faso</h1>
                </div>
                
                <div class="hidden md:flex space-x-4 items-center">
                    <a href="#" class="hover:text-yellow-200">Accueil</a>
                    <a href="#categories" class="hover:text-yellow-200">Catégories</a>
                    <a href="#how-it-works" class="hover:text-yellow-200">Comment ça marche</a>
                    <button onclick="openLoginModal()" class="bg-white text-orange-500 px-4 py-1 rounded-full font-medium hover:bg-gray-100">Connexion</button>
                    <button onclick="openRegisterModal()" class="bg-orange-600 text-white px-4 py-1 rounded-full font-medium hover:bg-orange-700">Inscription</button>
                </div>
                
                <button id="mobileMenuButton" class="md:hidden text-2xl">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobileMenu" class="hidden md:hidden mt-4 pb-2">
                <div class="flex flex-col space-y-3">
                    <a href="#" class="hover:text-yellow-200">Accueil</a>
                    <a href="#categories" class="hover:text-yellow-200">Catégories</a>
                    <a href="#how-it-works" class="hover:text-yellow-200">Comment ça marche</a>
                    <button onclick="openLoginModal()" class="bg-white text-orange-500 px-4 py-1 rounded-full font-medium hover:bg-gray-100">Connexion</button>
                    <button onclick="openRegisterModal()" class="bg-orange-600 text-white px-4 py-1 rounded-full font-medium hover:bg-orange-700">Inscription</button>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="gradient-bg text-white py-12 md:py-20">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-3xl md:text-5xl font-bold mb-4">Trouvez tout ce dont vous avez besoin au Burkina Faso</h1>
            <p class="text-xl mb-8">La plateforme de petites annonces locales la plus simple et efficace</p>
            
            <!-- Search Bar -->
            <div class="max-w-3xl mx-auto bg-white rounded-full shadow-lg overflow-hidden">
                <div class="flex">
                    <input type="text" placeholder="Rechercher une annonce..." class="w-full px-6 py-3 text-gray-700 focus:outline-none">
                    <select class="bg-gray-100 text-gray-700 px-4 border-l border-gray-300 focus:outline-none">
                        <option>Toutes catégories</option>
                        <option>Téléphones</option>
                        <option>Vêtements</option>
                        <option>Meubles</option>
                        <option>Véhicules</option>
                        <option>Services</option>
                    </select>
                    <button class="bg-orange-500 text-white px-6 py-3 hover:bg-orange-600">
                        <i class="fas fa-search"></i> Rechercher
                    </button>
                </div>
            </div>
            
            <div class="mt-8">
                <button onclick="openAnnouncementModal()" class="bg-white text-orange-500 px-6 py-3 rounded-full font-bold shadow-lg hover:bg-gray-100">
                    <i class="fas fa-plus-circle"></i> Publier une annonce
                </button>
            </div>
        </div>
    </section>

    <!-- Categories Section -->
    <section id="categories" class="py-12 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">Catégories populaires</h2>
            
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6">
                <!-- Category 1 -->
                <div class="category-card bg-white rounded-lg shadow-md p-6 text-center transition duration-300 cursor-pointer">
                    <div class="bg-orange-100 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-3">
                        <i class="fas fa-mobile-alt text-orange-500 text-2xl"></i>
                    </div>
                    <h3 class="font-semibold">Téléphones</h3>
                    <p class="text-sm text-gray-500 mt-1">125 annonces</p>
                </div>
                
                <!-- Category 2 -->
                <div class="category-card bg-white rounded-lg shadow-md p-6 text-center transition duration-300 cursor-pointer">
                    <div class="bg-blue-100 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-3">
                        <i class="fas fa-tshirt text-blue-500 text-2xl"></i>
                    </div>
                    <h3 class="font-semibold">Vêtements</h3>
                    <p class="text-sm text-gray-500 mt-1">89 annonces</p>
                </div>
                
                <!-- Category 3 -->
                <div class="category-card bg-white rounded-lg shadow-md p-6 text-center transition duration-300 cursor-pointer">
                    <div class="bg-green-100 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-3">
                        <i class="fas fa-couch text-green-500 text-2xl"></i>
                    </div>
                    <h3 class="font-semibold">Meubles</h3>
                    <p class="text-sm text-gray-500 mt-1">76 annonces</p>
                </div>
                
                <!-- Category 4 -->
                <div class="category-card bg-white rounded-lg shadow-md p-6 text-center transition duration-300 cursor-pointer">
                    <div class="bg-red-100 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-3">
                        <i class="fas fa-car text-red-500 text-2xl"></i>
                    </div>
                    <h3 class="font-semibold">Véhicules</h3>
                    <p class="text-sm text-gray-500 mt-1">54 annonces</p>
                </div>
                
                <!-- Category 5 -->
                <div class="category-card bg-white rounded-lg shadow-md p-6 text-center transition duration-300 cursor-pointer">
                    <div class="bg-purple-100 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-3">
                        <i class="fas fa-tools text-purple-500 text-2xl"></i>
                    </div>
                    <h3 class="font-semibold">Services</h3>
                    <p class="text-sm text-gray-500 mt-1">112 annonces</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Recent Announcements -->
    <section class="py-12 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-3xl font-bold">Annonces récentes</h2>
                <div class="flex space-x-1 border-b border-gray-200">
                    <button class="px-4 py-2 active-tab">Toutes</button>
                    <button class="px-4 py-2 hover:text-orange-500">Ouagadougou</button>
                    <button class="px-4 py-2 hover:text-orange-500">Bobo-Dioulasso</button>
                    <button class="px-4 py-2 hover:text-orange-500">Autres villes</button>
                </div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Announcement 1 -->
                <div class="announcement-card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1601784551446-66c9e1e22152?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="iPhone 12" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-orange-500 text-white text-xs px-2 py-1 rounded-full">Nouveau</span>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg">iPhone 12 Pro Max 256Go</h3>
                            <span class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded">Negociable</span>
                        </div>
                        <p class="text-gray-600 text-sm mt-1">État: Comme neuf, utilisé 6 mois</p>
                        <p class="text-orange-500 font-bold text-lg mt-2">450 000 FCFA</p>
                        <div class="flex justify-between items-center mt-4">
                            <span class="text-gray-500 text-sm"><i class="fas fa-map-marker-alt"></i> Ouaga 2000</span>
                            <span class="text-gray-500 text-sm">Aujourd'hui</span>
                        </div>
                        <button class="w-full mt-4 bg-orange-500 text-white py-2 rounded hover:bg-orange-600 flex items-center justify-center space-x-2">
                            <i class="fab fa-whatsapp"></i>
                            <span>Contacter</span>
                        </button>
                    </div>
                </div>
                
                <!-- Announcement 2 -->
                <div class="announcement-card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1551232864-3f0890e580d9?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Toyota RAV4" class="w-full h-48 object-cover">
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg">Toyota RAV4 2018</h3>
                            <span class="bg-red-100 text-red-800 text-xs px-2 py-1 rounded">Urgent</span>
                        </div>
                        <p class="text-gray-600 text-sm mt-1">Kilométrage: 45 000 km, Diesel</p>
                        <p class="text-orange-500 font-bold text-lg mt-2">12 500 000 FCFA</p>
                        <div class="flex justify-between items-center mt-4">
                            <span class="text-gray-500 text-sm"><i class="fas fa-map-marker-alt"></i> Karpala</span>
                            <span class="text-gray-500 text-sm">Hier</span>
                        </div>
                        <button class="w-full mt-4 bg-orange-500 text-white py-2 rounded hover:bg-orange-600 flex items-center justify-center space-x-2">
                            <i class="fab fa-whatsapp"></i>
                            <span>Contacter</span>
                        </button>
                    </div>
                </div>
                
                <!-- Announcement 3 -->
                <div class="announcement-card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1556905055-8f358a7a10b7?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Costume homme" class="w-full h-48 object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-lg">Costume 3 pièces homme</h3>
                        <p class="text-gray-600 text-sm mt-1">Taille: L, Couleur: Bleu marine</p>
                        <p class="text-orange-500 font-bold text-lg mt-2">35 000 FCFA</p>
                        <div class="flex justify-between items-center mt-4">
                            <span class="text-gray-500 text-sm"><i class="fas fa-map-marker-alt"></i> Bobo-Dioulasso</span>
                            <span class="text-gray-500 text-sm">Il y a 2 jours</span>
                        </div>
                        <button class="w-full mt-4 bg-orange-500 text-white py-2 rounded hover:bg-orange-600 flex items-center justify-center space-x-2">
                            <i class="fab fa-whatsapp"></i>
                            <span>Contacter</span>
                        </button>
                    </div>
                </div>
                
                <!-- Announcement 4 -->
                <div class="announcement-card bg-white rounded-lg shadow-md overflow-hidden transition duration-300">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1583845112208-9b4507a7bcfa?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Service plomberie" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-blue-500 text-white text-xs px-2 py-1 rounded-full">Service</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-lg">Plombier professionnel</h3>
                        <p class="text-gray-600 text-sm mt-1">Installation et réparation de toutes installations</p>
                        <p class="text-orange-500 font-bold text-lg mt-2">À partir de 10 000 FCFA</p>
                        <div class="flex justify-between items-center mt-4">
                            <span class="text-gray-500 text-sm"><i class="fas fa-map-marker-alt"></i> Ouaga 2000</span>
                            <span class="text-gray-500 text-sm">Il y a 3 jours</span>
                        </div>
                        <button class="w-full mt-4 bg-orange-500 text-white py-2 rounded hover:bg-orange-600 flex items-center justify-center space-x-2">
                            <i class="fab fa-whatsapp"></i>
                            <span>Contacter</span>
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-8">
                <button class="border border-orange-500 text-orange-500 px-6 py-2 rounded-full hover:bg-orange-500 hover:text-white">
                    Voir plus d'annonces
                </button>
            </div>
        </div>
    </section>

    <!-- How it works -->
    <section id="how-it-works" class="py-12 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">Comment ça marche</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Step 1 -->
                <div class="text-center">
                    <div class="bg-orange-100 w-20 h-20 mx-auto rounded-full flex items-center justify-center mb-4">
                        <span class="bg-orange-500 text-white w-8 h-8 rounded-full flex items-center justify-center">1</span>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Créez un compte</h3>
                    <p class="text-gray-600">Inscrivez-vous gratuitement en quelques secondes pour commencer à publier ou répondre aux annonces.</p>
                </div>
                
                <!-- Step 2 -->
                <div class="text-center">
                    <div class="bg-orange-100 w-20 h-20 mx-auto rounded-full flex items-center justify-center mb-4">
                        <span class="bg-orange-500 text-white w-8 h-8 rounded-full flex items-center justify-center">2</span>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Publiez votre annonce</h3>
                    <p class="text-gray-600">Décrivez votre article ou service avec des photos claires et un prix juste.</p>
                </div>
                
                <!-- Step 3 -->
                <div class="text-center">
                    <div class="bg-orange-100 w-20 h-20 mx-auto rounded-full flex items-center justify-center mb-4">
                        <span class="bg-orange-500 text-white w-8 h-8 rounded-full flex items-center justify-center">3</span>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Connectez-vous</h3>
                    <p class="text-gray-600">Répondez aux messages des acheteurs et concluez la transaction en toute sécurité.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Mobile App Section -->
    <section class="py-12 gradient-bg text-white">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0">
                    <h2 class="text-3xl font-bold mb-4">Téléchargez notre application mobile</h2>
                    <p class="mb-6">Accédez à Tchatcha Faso où que vous soyez. Notre application est disponible sur Android et iOS.</p>
                    <div class="flex space-x-4">
                        <button class="bg-black text-white px-6 py-2 rounded-lg flex items-center space-x-2">
                            <i class="fab fa-apple text-2xl"></i>
                            <div class="text-left">
                                <span class="text-xs">Télécharger sur</span>
                                <div class="font-bold">App Store</div>
                            </div>
                        </button>
                        <button class="bg-black text-white px-6 py-2 rounded-lg flex items-center space-x-2">
                            <i class="fab fa-google-play text-2xl"></i>
                            <div class="text-left">
                                <span class="text-xs">Disponible sur</span>
                                <div class="font-bold">Google Play</div>
                            </div>
                        </button>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <img src="https://cdn.pixabay.com/photo/2017/01/22/12/07/imac-1999636_1280.png" alt="Mobile App" class="w-64">
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- About -->
                <div>
                    <h3 class="text-xl font-bold mb-4">Tchatcha Faso</h3>
                    <p class="text-gray-400">La plateforme de petites annonces locales la plus simple et efficace au Burkina Faso.</p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <!-- Quick Links -->
                <div>
                    <h3 class="text-xl font-bold mb-4">Liens rapides</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Accueil</a></li>
                        <li><a href="#categories" class="text-gray-400 hover:text-white">Catégories</a></li>
                        <li><a href="#how-it-works" class="text-gray-400 hover:text-white">Comment ça marche</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Publier une annonce</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Connexion</a></li>
                    </ul>
                </div>
                
                <!-- Categories -->
                <div>
                    <h3 class="text-xl font-bold mb-4">Catégories</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Téléphones</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Vêtements</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Meubles</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Véhicules</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Services</a></li>
                    </ul>
                </div>
                
                <!-- Contact -->
                <div>
                    <h3 class="text-xl font-bold mb-4">Contact</h3>
                    <ul class="space-y-2">
                        <li class="flex items-center space-x-2 text-gray-400">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Ouagadougou, Burkina Faso</span>
                        </li>
                        <li class="flex items-center space-x-2 text-gray-400">
                            <i class="fas fa-phone"></i>
                            <span>+226 70 12 34 56</span>
                        </li>
                        <li class="flex items-center space-x-2 text-gray-400">
                            <i class="fas fa-envelope"></i>
                            <span>contact@tchatchafaso.bf</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; 2023 Tchatcha Faso. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <!-- Login Modal -->
    <div id="loginModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
        <div class="bg-white rounded-lg w-full max-w-md mx-4">
            <div class="p-6">
                <div class="flex justify-between items-center mb-4">
                    <h3 class="text-2xl font-bold">Connexion</h3>
                    <button onclick="closeLoginModal()" class="text-gray-500 hover:text-gray-700">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                
                <form>
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Email ou téléphone</label>
                        <input type="text" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Mot de passe</label>
                        <input type="password" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="flex justify-between items-center mb-6">
                        <div class="flex items-center">
                            <input type="checkbox" id="remember" class="mr-2">
                            <label for="remember" class="text-gray-700">Se souvenir de moi</label>
                        </div>
                        <a href="#" class="text-orange-500 hover:underline">Mot de passe oublié?</a>
                    </div>
                    
                    <button type="button" class="w-full bg-orange-500 text-white py-2 rounded-lg hover:bg-orange-600 mb-4">
                        Se connecter
                    </button>
                    
                    <div class="text-center">
                        <p class="text-gray-700">Vous n'avez pas de compte? <button onclick="switchToRegister()" class="text-orange-500 hover:underline">S'inscrire</button></p>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Register Modal -->
    <div id="registerModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
        <div class="bg-white rounded-lg w-full max-w-md mx-4">
            <div class="p-6">
                <div class="flex justify-between items-center mb-4">
                    <h3 class="text-2xl font-bold">Inscription</h3>
                    <button onclick="closeRegisterModal()" class="text-gray-500 hover:text-gray-700">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                
                <form>
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Nom complet</label>
                        <input type="text" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Email</label>
                        <input type="email" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Numéro de téléphone</label>
                        <input type="tel" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Mot de passe</label>
                        <input type="password" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="mb-6">
                        <label class="block text-gray-700 mb-2">Confirmer le mot de passe</label>
                        <input type="password" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                    </div>
                    
                    <div class="flex items-center mb-6">
                        <input type="checkbox" id="terms" class="mr-2">
                        <label for="terms" class="text-gray-700">J'accepte les <a href="#" class="text-orange-500 hover:underline">conditions d'utilisation</a></label>
                    </div>
                    
                    <button type="button" class="w-full bg-orange-500 text-white py-2 rounded-lg hover:bg-orange-600 mb-4">
                        S'inscrire
                    </button>
                    
                    <div class="text-center">
                        <p class="text-gray-700">Vous avez déjà un compte? <button onclick="switchToLogin()" class="text-orange-500 hover:underline">Se connecter</button></p>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Announcement Modal -->
    <div id="announcementModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden overflow-y-auto">
        <div class="bg-white rounded-lg w-full max-w-2xl mx-4 my-8">
            <div class="p-6">
                <div class="flex justify-between items-center mb-4">
                    <h3 class="text-2xl font-bold">Publier une annonce</h3>
                    <button onclick="closeAnnouncementModal()" class="text-gray-500 hover:text-gray-700">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                
                <form>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                        <div>
                            <label class="block text-gray-700 mb-2">Titre de l'annonce*</label>
                            <input type="text" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500" placeholder="Ex: iPhone 12 Pro Max 256Go">
                        </div>
                        
                        <div>
                            <label class="block text-gray-700 mb-2">Catégorie*</label>
                            <select class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                                <option>Sélectionnez une catégorie</option>
                                <option>Téléphones</option>
                                <option>Vêtements</option>
                                <option>Meubles</option>
                                <option>Véhicules</option>
                                <option>Services</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="mb-4">
                        <label class="block text-gray-700 mb-2">Description*</label>
                        <textarea class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500" rows="4" placeholder="Décrivez votre article ou service en détail..."></textarea>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
                        <div>
                            <label class="block text-gray-700 mb-2">Prix (FCFA)*</label>
                            <input type="number" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500" placeholder="Ex: 450000">
                        </div>
                        
                        <div>
                            <label class="block text-gray-700 mb-2">Type de prix</label>
                            <select class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                                <option>Fixe</option>
                                <option>Négociable</option>
                                <option>À partir de (pour services)</option>
                            </select>
                        </div>
                        
                        <div>
                            <label class="block text-gray-700 mb-2">État</label>
                            <select class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                                <option>Neuf</option>
                                <option>Comme neuf</option>
                                <option>Bon état</option>
                                <option>État moyen</option>
                                <option>Pour pièces</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                        <div>
                            <label class="block text-gray-700 mb-2">Localisation*</label>
                            <select class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
                                <option>Sélectionnez une ville</option>
                                <option>Ouagadougou</option>
                                <option>Bobo-Dioulasso</option>
                                <option>Koudougou</option>
                                <option>Ouahigouya</option>
                                <option>Banfora</option>
                                <option>Autre</option>
                            </select>
                        </div>
                        
                        <div>
                            <label class="block text-gray-700 mb-2">Quartier</label>
                            <input type="text" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500" placeholder="Ex: Ouaga 2000, Karpala">
                        </div>
                    </div>
                    
                    <div class="mb-6">
                        <label class="block text-gray-700 mb-2">Photos (max 5)*</label>
                        <div class="border-2 border-dashed border-gray-300 rounded-lg p-4 text-center">
                            <div class="flex flex-wrap gap-2 mb-4" id="previewContainer">
                                <!-- Preview images will appear here -->
                            </div>
                            <label for="fileUpload" class="cursor-pointer">
                                <i class="fas fa-cloud-upload-alt text-3xl text-gray-400 mb-2"></i>
                                <p class="text-gray-500">Glissez-déposez vos photos ici ou cliquez pour sélectionner</p>
                                <p class="text-sm text-gray-400">Formats acceptés: JPG, PNG (max 2MB par photo)</p>
                            </label>
                            <input type="file" id="fileUpload" class="hidden" multiple accept="image/*">
                        </div>
                    </div>
                    
                    <div class="flex justify-between">
                        <button type="button" onclick="closeAnnouncementModal()" class="px-6 py-2 border border-gray-300 rounded-lg hover:bg-gray-100">
                            Annuler
                        </button>
                        <button type="button" class="px-6 py-2 bg-orange-500 text-white rounded-lg hover:bg-orange-600">
                            Publier l'annonce
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- User Dashboard (hidden by default) -->
    <div id="userDashboard" class="fixed inset-0 bg-gray-100 z-50 hidden overflow-y-auto">
        <div class="container mx-auto px-4 py-8">
            <div class="flex justify-between items-center mb-8">
                <h2 class="text-2xl font-bold">Mon compte</h2>
                <button onclick="closeUserDashboard()" class="text-gray-500 hover:text-gray-700">
                    <i class="fas fa-times text-2xl"></i>
                </button>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
                <!-- Sidebar -->
                <div class="md:col-span-1 bg-white rounded-lg shadow p-4">
                    <div class="text-center mb-6">
                        <div class="w-20 h-20 mx-auto rounded-full bg-gray-200 mb-2 overflow-hidden">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Profile" class="w-full h-full object-cover">
                        </div>
                        <h3 class="font-bold">Amadou Diallo</h3>
                        <p class="text-sm text-gray-500">Ouagadougou</p>
                    </div>
                    
                    <ul class="space-y-2">
                        <li>
                            <button onclick="showDashboardTab('myAnnouncements')" class="w-full text-left px-4 py-2 rounded-lg bg-orange-100 text-orange-700">
                                <i class="fas fa-bullhorn mr-2"></i> Mes annonces
                            </button>
                        </li>
                        <li>
                            <button onclick="showDashboardTab('messages')" class="w-full text-left px-4 py-2 rounded-lg hover:bg-gray-100">
                                <i class="fas fa-envelope mr-2"></i> Messages
                            </button>
                        </li>
                        <li>
                            <button onclick="showDashboardTab('favorites')" class="w-full text-left px-4 py-2 rounded-lg hover:bg-gray-100">
                                <i class="fas fa-heart mr-2"></i> Favoris
                            </button>
                        </li>
                        <li>
                            <button onclick="showDashboardTab('settings')" class="w-full text-left px-4 py-2 rounded-lg hover:bg-gray-100">
                                <i class="fas fa-cog mr-2"></i> Paramètres
                            </button>
                        </li>
                        <li>
                            <button class="w-full text-left px-4 py-2 rounded-lg hover:bg-gray-100 text-red-500">
                                <i class="fas fa-sign-out-alt mr-2"></i> Déconnexion
                            </button>
                        </li>
                    </ul>
                </div>
                
                <!-- Main Content -->
                <div class="md:col-span-3">
                    <!-- My Announcements Tab -->
                    <div id="myAnnouncementsTab" class="bg-white rounded-lg shadow p-6">
                        <div class="flex justify-between items-center mb-6">
                            <h3 class="text-xl font-bold">Mes annonces</h3>
                            <button onclick="openAnnouncementModal()" class="bg-orange-500 text-white px-4 py-2 rounded-lg hover:bg-orange-600 flex items-center">
                                <i class="fas fa-plus mr-2"></i> Nouvelle annonce
                            </button>
                        </div>
                        
                        <div class="overflow-x-auto">
                            <table class="w-full">
                                <thead>
                                    <tr class="border-b">
                                        <th class="text-left py-3 px-4">Annonce</th>
                                        <th class="text-left py-3 px-4">Prix</th>
                                        <th class="text-left py-3 px-4">Statut</th>
                                        <th class="text-left py-3 px-4">Actions</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr class="border-b hover:bg-gray-50">
                                        <td class="py-3 px-4">
                                            <div class="flex items-center">
                                                <div class="w-16 h-16 bg-gray-200 rounded mr-3 overflow-hidden">
                                                    <img src="https://images.unsplash.com/photo-1601784551446-66c9e1e22152?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="iPhone" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">iPhone 12 Pro Max 256Go</h4>
                                                    <p class="text-sm text-gray-500">Publié le 12/06/2023</p>
                                                </div>
                                            </div>
                                        </td>
                                        <td class="py-3 px-4 font-medium">450 000 FCFA</td>
                                        <td class="py-3 px-4">
                                            <span class="bg-green-100 text-green-800 px-2 py-1 rounded-full text-xs">Active</span>
                                        </td>
                                        <td class="py-3 px-4">
                                            <div class="flex space-x-2">
                                                <button class="text-blue-500 hover:text-blue-700">
                                                    <i class="fas fa-edit"></i>
                                                </button>
                                                <button class="text-red-500 hover:text-red-700">
                                                    <i class="fas fa-trash"></i>
                                                </button>
                                            </div>
                                        </td>
                                    </tr>
                                    
                                    <tr class="border-b hover:bg-gray-50">
                                        <td class="py-3 px-4">
                                            <div class="flex items-center">
                                                <div class="w-16 h-16 bg-gray-200 rounded mr-3 overflow-hidden">
                                                    <img src="https://images.unsplash.com/photo-1551232864-3f0890e580d9?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Toyota" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">Toyota RAV4 2018</h4>
                                                    <p class="text-sm text-gray-500">Publié le 05/06/2023</p>
                                                </div>
                                            </div>
                                        </td>
                                        <td class="py-3 px-4 font-medium">12 500 000 FCFA</td>
                                        <td class="py-3 px-4">
                                            <span class="bg-yellow-100 text-yellow-800 px-2 py-1 rounded-full text-xs">En attente</span>
                                        </td>
                                        <td class="py-3 px-4">
                                            <div class="flex space-x-2">
                                                <button class="text-blue-500 hover:text-blue-700">
                                                    <i class="fas fa-edit"></i>
                                                </button>
                                                <button class="text-red-500 hover:text-red-700">
                                                    <i class="fas fa-trash"></i>
                                                </button>
                                            </div>
                                        </td>
                                    </tr>
                                    
                                    <tr class="border-b hover:bg-gray-50">
                                        <td class="py-3 px-4">
                                            <div class="flex items-center">
                                                <div class="w-16 h-16 bg-gray-200 rounded mr-3 overflow-hidden">
                                                    <img src="https://images.unsplash.com/photo-1583845112208-9b4507a7bcfa?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Plomberie" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">Service de plomberie</h4>
                                                    <p class="text-sm text-gray-500">Publié le 28/05/2023</p>
                                                </div>
                                            </div>
                                        </td>
                                        <td class="py-3 px-4 font-medium">À partir de 10 000 FCFA</td>
                                        <td class="py-3 px-4">
                                            <span class="bg-red-100 text-red-800 px-2 py-1 rounded-full text-xs">Expiré</span>
                                        </td>
                                        <td class="py-3 px-4">
                                            <div class="flex space-x-2">
                                                <button class="text-blue-500 hover:text-blue-700">
                                                    <i class="fas fa-edit"></i>
                                                </button>
                                                <button class="text-red-500 hover:text-red-700">
                                                    <i class="fas fa-trash"></i>
                                                </button>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                    
                    <!-- Messages Tab -->
                    <div id="messagesTab" class="bg-white rounded-lg shadow p-6 hidden">
                        <h3 class="text-xl font-bold mb-6">Messages</h3>
                        <div class="border rounded-lg overflow-hidden">
                            <div class="flex border-b">
                                <div class="w-1/3 border-r">
                                    <div class="p-4 bg-gray-50">
                                        <input type="text" placeholder="Rechercher un message..." class="w-full px-4 py-2 border rounded-lg">
                                    </div>
                                    <div class="overflow-y-auto" style="max-height: 500px;">
                                        <div class="border-b p-4 hover:bg-gray-50 cursor-pointer">
                                            <div class="flex items-center">
                                                <div class="w-12 h-12 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                    <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Profile" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">Aïcha Traoré</h4>
                                                    <p class="text-sm text-gray-500 truncate">Bonjour, le téléphone est-il toujours disponible?</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="border-b p-4 hover:bg-gray-50 cursor-pointer bg-blue-50">
                                            <div class="flex items-center">
                                                <div class="w-12 h-12 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                    <img src="https://randomuser.me/api/portraits/men/22.jpg" alt="Profile" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">Boubacar Sanou</h4>
                                                    <p class="text-sm text-gray-500 truncate">Je suis intéressé par votre voiture, pouvez-vous me donner plus de détails?</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="border-b p-4 hover:bg-gray-50 cursor-pointer">
                                            <div class="flex items-center">
                                                <div class="w-12 h-12 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                    <img src="https://randomuser.me/api/portraits/women/33.jpg" alt="Profile" class="w-full h-full object-cover">
                                                </div>
                                                <div>
                                                    <h4 class="font-medium">Fatou Nikiéma</h4>
                                                    <p class="text-sm text-gray-500 truncate">Merci pour le service, tout s'est bien passé!</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="w-2/3">
                                    <div class="p-4 border-b flex justify-between items-center">
                                        <div class="flex items-center">
                                            <div class="w-12 h-12 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                <img src="https://randomuser.me/api/portraits/men/22.jpg" alt="Profile" class="w-full h-full object-cover">
                                            </div>
                                            <div>
                                                <h4 class="font-medium">Boubacar Sanou</h4>
                                                <p class="text-sm text-gray-500">En ligne</p>
                                            </div>
                                        </div>
                                        <button class="text-orange-500 hover:text-orange-700">
                                            <i class="fab fa-whatsapp text-2xl"></i>
                                        </button>
                                    </div>
                                    <div class="p-4 overflow-y-auto" style="max-height: 400px;">
                                        <div class="flex mb-4">
                                            <div class="w-10 h-10 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                <img src="https://randomuser.me/api/portraits/men/22.jpg" alt="Profile" class="w-full h-full object-cover">
                                            </div>
                                            <div class="bg-gray-100 rounded-lg p-3 max-w-xs">
                                                <p>Je suis intéressé par votre voiture, pouvez-vous me donner plus de détails?</p>
                                                <p class="text-xs text-gray-500 mt-1">10:23 AM</p>
                                            </div>
                                        </div>
                                        <div class="flex justify-end mb-4">
                                            <div class="bg-orange-100 rounded-lg p-3 max-w-xs">
                                                <p>Bonjour Boubacar, la voiture est en excellent état avec seulement 45 000 km au compteur. Elle a toujours été entretenue chez Toyota.</p>
                                                <p class="text-xs text-gray-500 mt-1 text-right">10:30 AM</p>
                                            </div>
                                            <div class="w-10 h-10 rounded-full bg-gray-200 ml-3 overflow-hidden">
                                                <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Profile" class="w-full h-full object-cover">
                                            </div>
                                        </div>
                                        <div class="flex mb-4">
                                            <div class="w-10 h-10 rounded-full bg-gray-200 mr-3 overflow-hidden">
                                                <img src="https://randomuser.me/api/portraits/men/22.jpg" alt="Profile" class="w-full h-full object-cover">
                                            </div>
                                            <div class="bg-gray-100 rounded-lg p-3 max-w-xs">
                                                <p>Merci pour ces informations. Est-ce que le prix est négociable?</p>
                                                <p class="text-xs text-gray-500 mt-1">10:32 AM</p>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="p-4 border-t">
                                        <div class="flex">
                                            <input type="text" placeholder="Tapez votre message..." class="flex-grow px-4 py-2 border rounded-l-lg focus:outline-none">
                                            <button class="bg-orange-500 text-white px-4 py-2 rounded-r-lg hover:bg-orange-600">
                                                <i class="fas fa-paper-plane"></i>
                                            </button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Favorites Tab -->
                    <div id="favoritesTab" class="bg-white rounded-lg shadow p-6 hidden">
                        <h3 class="text-xl font-bold mb-6">Mes favoris</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div class="flex border rounded-lg p-3 hover:bg-gray-50">
                                <div class="w-24 h-24 bg-gray-200 rounded mr-3 overflow-hidden">
                                    <img src="https://images.unsplash.com/photo-1556905055-8f358a7a10b7?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Costume" class="w-full h-full object-cover">
                                </div>
                                <div class="flex-grow">
                                    <h4 class="font-medium">Costume 3 pièces homme</h4>
                                    <p class="text-orange-500 font-bold">35 000 FCFA</p>
                                    <p class="text-sm text-gray-500">Bobo-Dioulasso</p>
                                </div>
                                <button class="text-red-500 hover:text-red-700 self-start">
                                    <i class="fas fa-heart"></i>
                                </button>
                            </div>
                            
                            <div class="flex border rounded-lg p-3 hover:bg-gray-50">
                                <div class="w-24 h-24 bg-gray-200 rounded mr-3 overflow-hidden">
                                    <img src="https://images.unsplash.com/photo-1601784551446-66c9e1e22152?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="iPhone" class="w-full h-full object-cover">
                                </div>
                                <div class="flex-grow">
                                    <h4 class="font-medium">iPhone 12 Pro Max 256Go</h4>
                                    <p class="text-orange-500 font-bold">450 000 FCFA</p>
                                    <p class="text-sm text-gray-500">Ouaga 2000</p>
                                </div>
                                <button class="text-red-500 hover:text-red-700 self-start">
                                    <i class="fas fa-heart"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Settings Tab -->
                    <div id="settingsTab" class="bg-white rounded-lg shadow p-6 hidden">
                        <h3 class="text-xl font-bold mb-6">Paramètres du compte</h3>
                        
                        <form>
                            <div class="mb-6">
                                <h4 class="font-medium mb-4">Informations personnelles</h4>
                                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                                    <div>
                                        <label class="block text-gray-700 mb-2">Nom</label>
                                        <input type="text" value="Amadou" class="w-full px-4 py-2 border rounded-lg">
                                    </div>
                                    <div>
                                        <label class="block text-gray-700 mb-2">Prénom</label>
                                        <input type="text" value="Diallo" class="w-full px-4 py-2 border rounded-lg">
                                    </div>
                                </div>
                                
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Email</label>
                                    <input type="email" value="amadou.diallo@example.com" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                                
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Téléphone</label>
                                    <input type="tel" value="+226 70 12 34 56" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                                
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Ville</label>
                                    <select class="w-full px-4 py-2 border rounded-lg">
                                        <option>Ouagadougou</option>
                                        <option>Bobo-Dioulasso</option>
                                        <option>Koudougou</option>
                                        <option>Ouahigouya</option>
                                        <option>Autre</option>
                                    </select>
                                </div>
                                
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Quartier</label>
                                    <input type="text" value="Karpala" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                            </div>
                            
                            <div class="mb-6">
                                <h4 class="font-medium mb-4">Photo de profil</h4>
                                <div class="flex items-center">
                                    <div class="w-20 h-20 rounded-full bg-gray-200 mr-4 overflow-hidden">
                                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Profile" class="w-full h-full object-cover">
                                    </div>
                                    <div>
                                        <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg hover:bg-gray-300 mr-2">
                                            Changer
                                        </button>
                                        <button class="text-red-500 hover:text-red-700">
                                            Supprimer
                                        </button>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="mb-6">
                                <h4 class="font-medium mb-4">Changer le mot de passe</h4>
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Mot de passe actuel</label>
                                    <input type="password" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Nouveau mot de passe</label>
                                    <input type="password" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                                <div class="mb-4">
                                    <label class="block text-gray-700 mb-2">Confirmer le nouveau mot de passe</label>
                                    <input type="password" class="w-full px-4 py-2 border rounded-lg">
                                </div>
                            </div>
                            
                            <div class="flex justify-end">
                                <button type="button" class="px-6 py-2 border border-gray-300 rounded-lg hover:bg-gray-100 mr-4">
                                    Annuler
                                </button>
                                <button type="button" class="px-6 py-2 bg-orange-500 text-white rounded-lg hover:bg-orange-600">
                                    Enregistrer les modifications
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Mobile menu toggle
        document.getElementById('mobileMenuButton').addEventListener('click', function() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        });

        // Modal functions
        function openLoginModal() {
            document.getElementById('loginModal').classList.remove('hidden');
        }

        function closeLoginModal() {
            document.getElementById('loginModal').classList.add('hidden');
        }

        function openRegisterModal() {
            document.getElementById('registerModal').classList.remove('hidden');
        }

        function closeRegisterModal() {
            document.getElementById('registerModal').classList.add('hidden');
        }

        function switchToRegister() {
            closeLoginModal();
            openRegisterModal();
        }

        function switchToLogin() {
            closeRegisterModal();
            openLoginModal();
        }

        function openAnnouncementModal() {
            document.getElementById('announcementModal').classList.remove('hidden');
        }

        function closeAnnouncementModal() {
            document.getElementById('announcementModal').classList.add('hidden');
        }

        function openUserDashboard() {
            document.getElementById('userDashboard').classList.remove('hidden');
            showDashboardTab('myAnnouncements');
        }

        function closeUserDashboard() {
            document.getElementById('userDashboard').classList.add('hidden');
        }

        function showDashboardTab(tabName) {
            // Hide all tabs
            document.getElementById('myAnnouncementsTab').classList.add('hidden');
            document.getElementById('messagesTab').classList.add('hidden');
            document.getElementById('favoritesTab').classList.add('hidden');
            document.getElementById('settingsTab').classList.add('hidden');
            
            // Show selected tab
            document.getElementById(tabName + 'Tab').classList.remove('hidden');
            
            // Update active tab style in sidebar
            const tabButtons = document.querySelectorAll('#userDashboard ul li button');
            tabButtons.forEach(button => {
                button.classList.remove('bg-orange-100', 'text-orange-700');
                if (button.getAttribute('onclick').includes(tabName)) {
                    button.classList.add('bg-orange-100', 'text-orange-700');
                }
            });
        }

        // Image preview for announcement form
        document.getElementById('fileUpload').addEventListener('change', function(e) {
            const previewContainer = document.getElementById('previewContainer');
            previewContainer.innerHTML = '';
            
            const files = e.target.files;
            for (let i = 0; i < files.length; i++) {
                if (i >= 5) break; // Limit to 5 images
                
                const reader = new FileReader();
                reader.onload = function(event) {
                    const imgDiv = document.createElement('div');
                    imgDiv.className = 'relative w-20 h-20 rounded overflow-hidden';
                    
                    const img = document.createElement('img');
                    img.src = event.target.result;
                    img.className = 'w-full h-full object-cover';
                    
                    const removeBtn = document.createElement('button');
                    removeBtn.className = 'absolute top-1 right-1 bg-red-500 text-white rounded-full w-5 h-5 flex items-center justify-center text-xs';
                    removeBtn.innerHTML = '&times;';
                    removeBtn.onclick = function() {
                        imgDiv.remove();
                    };
                    
                    imgDiv.appendChild(img);
                    imgDiv.appendChild(removeBtn);
                    previewContainer.appendChild(imgDiv);
                }
                reader.readAsDataURL(files[i]);
            }
        });

        // Simulate login for demo purposes
        document.querySelector('#loginModal button[type="button"]').addEventListener('click', function() {
            closeLoginModal();
            setTimeout(openUserDashboard, 300);
        });

        // Simulate register for demo purposes
        document.querySelector('#registerModal button[type="button"]').addEventListener('click', function() {
            closeRegisterModal();
            setTimeout(openUserDashboard, 300);
        });

        // Tab switching for announcements
        const tabButtons = document.querySelectorAll('.active-tab').parentElement.querySelectorAll('button');
        tabButtons.forEach(button => {
            button.addEventListener('click', function() {
                tabButtons.forEach(btn => btn.classList.remove('active-tab'));
                this.classList.add('active-tab');
            });
        });
    </script>
</body>
</html>
