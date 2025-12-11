<template>
  <footer class="bg-black py-16">
    <div class="container mx-auto ">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-12">
        
        <!-- Brand Column -->
        <div class="lg:col-span-2">
          <div class="flex items-center space-x-4 mb-6">
            <div class="w-12 h-12 bg-red-600 rounded-xl flex items-center justify-center">
              <i class="fas fa-dragon text-xl"></i>
            </div>
            <div>
              <div class="text-2xl font-bold text-white">OTAKU<span class="text-red-500">.</span>STORE</div>
              <div class="text-gray-400 text-sm">Premium Anime Merchandise</div>
            </div>
          </div>
          <p class="text-gray-500 text-sm leading-relaxed mb-8 max-w-md">
            La référence des produits anime et manga au Cameroun. 
            Qualité, authenticité et passion dans chaque pièce.
          </p>
        </div>
        
        <!-- Quick Links -->
        <div>
          <h4 class="font-bold text-white mb-6 text-lg">Boutique</h4>
          <ul class="space-y-4">
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Tous les produits</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Nouveautés</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Meilleures ventes</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Promotions</a></li>
          </ul>
        </div>
        
        <!-- Support -->
        <div>
          <h4 class="font-bold text-white mb-6 text-lg">Support</h4>
          <ul class="space-y-4">
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Contactez-nous</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Livraison</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">Retours & Échanges</a></li>
            <li><a href="#" class="text-gray-500 hover:text-red-400 transition-colors text-sm">FAQ</a></li>
          </ul>
        </div>
        
        <!-- Contact -->
        <div class="lg:col-span-1">
          <h4 class="font-bold text-white mb-6 text-lg">Contact</h4>
          <div class="space-y-6">
            <!-- WhatsApp -->
            <div class="flex items-center space-x-3 group">
              <div class="w-10 h-10 bg-green-600/20 rounded-lg flex items-center justify-center">
                     <img src="/whatsapp.png" alt="" class="w-6 h-6 object-cover"/>
              </div>
              <div>
                <div class="text-white font-medium text-sm">WhatsApp</div>
                <a href="https://wa.me/237653228070" class="text-gray-400 text-sm hover:text-green-400 transition-colors">
                  +237 6 53 22 80 70
                </a>
              </div>
            </div>
            
            <!-- Email -->
            <div class="flex items-center space-x-3 group">
              <div class="w-10 h-10 bg-red-600/20 rounded-lg flex items-center justify-center">
               <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
  <path d="M1.5 8.67v8.58a3 3 0 0 0 3 3h15a3 3 0 0 0 3-3V8.67l-8.928 5.493a3 3 0 0 1-3.144 0L1.5 8.67Z" />
  <path d="M22.5 6.908V6.75a3 3 0 0 0-3-3h-15a3 3 0 0 0-3 3v.158l9.714 5.978a1.5 1.5 0 0 0 1.572 0L22.5 6.908Z" />
</svg>

              </div>
              <div>
                <div class="text-white font-medium text-sm">Email</div>
                <a href="mailto:kennedylight05@gmail.com" class="text-gray-400 text-sm hover:text-red-400 transition-colors">
                  kennedylight05@gmail.com
                </a>
              </div>
            </div>
          </div>
          
          <!-- Social Links -->
          <div class="flex space-x-3 mt-8">
            <a href="#" class="w-8 h-8 bg-gray-900 rounded-lg flex items-center justify-center hover:bg-red-600 transition-colors">
              <i class="fab fa-instagram text-gray-400 hover:text-white text-sm"></i>
            </a>
            <a href="#" class="w-8 h-8 bg-gray-900 rounded-lg flex items-center justify-center hover:bg-red-600 transition-colors">
              <i class="fab fa-facebook-f text-gray-400 hover:text-white text-sm"></i>
            </a>
            <a href="#" class="w-8 h-8 bg-gray-900 rounded-lg flex items-center justify-center hover:bg-red-600 transition-colors">
              <i class="fab fa-tiktok text-gray-400 hover:text-white text-sm"></i>
            </a>
          </div>
        </div>
        
      </div>
      
      <!-- Bottom Footer -->
      <div class="border-t border-gray-900 mt-12 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0">
          <div class="text-gray-500 text-sm">
            &copy; 2024 OTAKU.STORE - Tous droits réservés
          </div>
          <div class="text-gray-500 text-sm">
            Conçu avec <i class="fas fa-heart text-red-500 mx-1"></i> au Cameroun
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>