<template>
  <!-- Hero Section - Minimaliste avec focus produits -->
  <div class="mb-6">
    
    <!-- Section texte + image côte à côte -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-12">
      
      <!-- Partie texte -->
      <div class="px-4">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">
          <span class="text-white">Boutique</span>
          <span class="text-red-600"> Otaku</span>
          <br>
          <span class="text-gray-300 text-2xl md:text-3xl mt-2 block">
            Produits Anime & Manga
          </span>
        </h1>
        
        <p class="text-gray-400 text-lg mb-8 leading-relaxed">
          Spécialistes des produits dérivés anime et manga. Nous proposons une sélection 
          rigoureuse de figurines, vêtements et accessoires pour les collectionneurs et passionnés.
        </p>
      </div>
      
      <!-- Partie image -->
      <div class="relative">
        <div class="rounded-xl  from-gray-900 to-black border border-gray-800  overflow-hidden">
          <img 
            src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" 
            alt="Collection produits anime" 
            class="w-full h-full object-cover"
          >
        </div>
        <div class="absolute -bottom-4 -right-4 w-32 h-32 bg-red-600/20 rounded-xl rotate-12 border border-red-600/30"></div>
      </div>
      
    </div>
    <h1 class="text-center p-6 text-2xl md:text-4xl font-bold text-red-600">Nos Atous</h1>
    
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto px-4">
        
        <!-- Figurines -->
        <div class="bg-gray-900/80 backdrop-blur-sm border border-gray-800 rounded-xl p-8 text-center hover:border-red-500/50 transition-all duration-300 group hover:transform hover:-translate-y-1">
          
          <h3 class="text-2xl font-bold mb-3 text-white group-hover:text-red-400 transition-colors">
            Figurines
          </h3>
          <p class="text-gray-400 mb-4">
            Collection de figurines détaillées de vos personnages préférés
          </p>
          <div class="text-red-400 text-sm font-medium">
            
            Éditions limitées disponibles
          </div>
        </div>
        
        <!-- Vêtements -->
        <div class="bg-gray-900/80 backdrop-blur-sm border border-gray-800 rounded-xl p-8 text-center hover:border-red-500/50 transition-all duration-300 group hover:transform hover:-translate-y-1">
          
          <h3 class="text-2xl font-bold mb-3 text-white group-hover:text-red-400 transition-colors">
            Vêtements
          </h3>
          <p class="text-gray-400 mb-4">
            T-shirts, hoodies et accessoires aux designs exclusifs
          </p>
          <div class="text-red-400 text-sm font-medium">
           
            Matières premium
          </div>
        </div>
        
        <!-- Accessoires -->
        <div class="bg-gray-900/80 backdrop-blur-sm border border-gray-800 rounded-xl p-8 text-center hover:border-red-500/50 transition-all duration-300 group hover:transform hover:-translate-y-1">
          
          <h3 class="text-2xl font-bold mb-3 text-white group-hover:text-red-400 transition-colors">
            Accessoires
          </h3>
          <p class="text-gray-400 mb-4">
            Bijoux, goodies et objets de collection uniques
          </p>
          <div class="text-red-400 text-sm font-medium">
                       Pièces authentiques
          </div>
        </div>
        
      </div>
    
  </div>
</template>