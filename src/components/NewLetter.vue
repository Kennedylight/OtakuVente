<template>
  <section class="py-20 bg-gray-900/50 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute top-0 right-0 w-64 h-64 bg-red-600/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-0 left-0 w-64 h-64 bg-red-600/10 rounded-full blur-3xl"></div>
    
    <div class="container mx-auto px-6 relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 items-center max-w-6xl mx-auto">
        
        <!-- Left Content -->
        <div>
          <h3 class="text-4xl font-bold text-white mb-6">
            <span class="block">Les Nouveautés</span>
            <span class="text-red-500">Directement Dans Votre Boîte Mail</span>
          </h3>
          
          <p class="text-gray-400 text-lg mb-8">
            Rejoignez notre communauté de passionnés et recevez chaque semaine
          </p>
          
          
        </div>
        
        <!-- Right Form -->
        <div class="bg-black border border-gray-800 rounded-2xl p-8">
          <div class="mb-8">
           
            <h4 class="text-2xl font-bold text-center text-white mb-2">Newsletter Premium</h4>
            
          </div>
          
          <div class="space-y-6">
            <div>
              <input 
                type="email" 
                placeholder="votre@email.com" 
                class="w-full px-5 py-4 bg-gray-900 border border-gray-800 rounded-xl text-white placeholder-gray-500 focus:outline-none focus:border-red-500 transition-colors"
              >
            </div>
            
            <button class="w-full px-6 py-4 cursor-pointer  bg-red-500  text-white font-semibold rounded-xl hover:from-red-700 hover:to-red-800 transition-all duration-300 shadow-lg">
              
              Rejoindre la communauté
            </button>
            
            <p class="text-gray-500 text-xs text-center">
              En vous inscrivant, vous acceptez de recevoir nos emails.
              <a href="#" class="text-red-400 hover:text-red-300">Politique de confidentialité</a>
            </p>
          </div>
        </div>
        
      </div>
    </div>
  </section>
</template>