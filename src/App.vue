
<template>
  <div id="app" class="min-h-screen bg-black text-white">
    
    <!-- Header -->
    <Header/>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-10">
      
      <Hero/>

      <!-- Filters Section -->
      <div class="mb-10">
        
      <h1 class="text-center p-6 text-2xl md:text-4xl font-bold text-red-600">Nos Articles</h1>
        <div class="flex flex-col lg:flex-row items-start lg:items-center justify-between space-y-6 lg:space-y-0">
          
          <!-- Categories Tabs -->
          <div class="flex flex-wrap gap-3">
            <button  @click="selectedCategory(category.name)"
              v-for="category in categories" 
              :key="category.id"
              class="px-6 py-3 bg-gray-900 rounded-xl hover:bg-gray-800  text-gray-300 hover:text-white border border-gray-800" :class="category.name === selectCategory ? 'border-red-500 text-white bg-gray-800' : ''"
            >

              {{ category.name }}
            </button>
          </div>
          
         <!-- Tri & Filtres -->
<div class="flex items-center space-x-4">
  <select class="px-4 py-3 bg-gray-900 border border-gray-800 rounded-xl text-white">
    <option>Trier par : Prix</option>
    <option>Moins de 5 000</option>
    <option>Moins de 10 000</option>
    <option>Moins de 20 000</option>
    <option>Moins de 50 000</option>
    <option>Moins de 100 000</option>
  </select>
</div>

          
        </div>
      </div>

      <!-- Products Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
        
        <!-- Product Card -->
        <div 
          v-for="product in productsFiltered" 
          :key="product.id"
          class="group bg-gray-900 border border-gray-800 rounded-2xl overflow-hidden hover:border-red-700 transition-all duration-300"
        >
          
          <!-- Image Container -->
          <div class="relative overflow-hidden">
            <img 
              :src="product.image" 
              :alt="product.name" 
              class="w-full h-64 object-cover group-hover:scale-105 transition-transform duration-500"
            >
            
            <!-- Badge -->
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 bg-black/80 backdrop-blur-sm text-white text-sm rounded-lg">
                {{ product.category }}
              </span>
            </div>
            
           
            
           
            
          </div>
          
          <!-- Product Info -->
          <div class="p-6">
            
            <!-- Category & Rating -->
            <div class="flex items-center justify-between mb-3">
              <span class="text-gray-500 text-sm">
                {{ product.series }}
              </span>
              <div class="flex items-center space-x-1">
               <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-4 text-yellow-500">
  <path fill-rule="evenodd" d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z" clip-rule="evenodd" />
</svg>


                <span class="text-white text-sm">{{ product.rating }}</span>
              </div>
            </div>
            
            <!-- Title -->
            <h3 class="text-xl font-semibold mb-3 group-hover:text-red-500 ">
              {{ product.name }}
            </h3>
            
            <!-- Description -->
            <p class="text-gray-400 text-sm mb-6 leading-relaxed">
              {{ product.description }}
            </p>
            
            <!-- Price & CTA -->
            <div class="flex items-center justify-between pt-6 border-t border-gray-800">
              <div>
                <div class="text-2xl font-bold">{{ product.price }}XAF</div>
                
              </div>
              
              <a :href='getWhatsappLink(product)' target="_blank" class="w-10 h-10 cursor-pointer hover:bg-gray-700 rounded-xl flex items-center justify-center ">
                <img src="/whatsapp.png" alt="" class="w-6 h-6 object-cover"/>
              </a>
            </div>
            
          </div>
          
        </div>
        
      </div>
      
      <!-- View More -->
      <div class="mt-16 text-center">
        <button class="px-8 py-4 bg-gray-900 border border-gray-800 rounded-xl hover:bg-gray-800 ">
          View More Products
          <i class="fas fa-arrow-right ml-2"></i>
        </button>
      </div>

    </main>
    <NewLetter/>

   <Footer/>

  </div>
</template>

<script>
  import Hero from './components/Hero.vue'
  import Footer from './components/Footer.vue';
  import Header from './components/Header.vue'
  import NewLetter from './components/NewLetter.vue';
export default {
   components: {
    Header,
    Hero,
    Footer,
    NewLetter
  },
  name: 'App',
  data() {
    return {
      searchQuery: '',
      selectCategory: 'Tous',
      productFiltered: [],
      
 products: [
  {
    id: 1,
    name: "Sweat Naruto Uzumaki",
    series: "Naruto",
    description: "Sweat noir avec broderie Naruto. Coton premium.",
    category: "Vêtements",
    price: 59.99,
    deliveryPrice: 4.99,
    delivery: "standard",
    rating: 4.8,
    image: "https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 2,
    name: "T-shirt Attack on Titan",
    series: "Attack on Titan",
    description: "T-shirt blanc premium Attack on Titan.",
    category: "Vêtements",
    price: 29.99,
    deliveryPrice: 0,
    delivery: "free",
    rating: 4.9,
    image: "https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 3,
    name: "Sneakers One Piece",
    series: "One Piece",
    description: "Baskets blanches logo Mugiwara. Confortables.",
    category: "Chaussures",
    price: 89.99,
    deliveryPrice: 5.99,
    delivery: "standard",
    rating: 4.7,
    image: "https://images.unsplash.com/photo-1549298916-b41d501d3772?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 4,
    name: "Veste Dragon Ball Z",
    series: "Dragon Ball",
    description: "Veste bomber noire logo Saiyan. Nylon léger.",
    category: "Vêtements",
    price: 79.99,
    deliveryPrice: 0,
    delivery: "free",
    rating: 4.9,
    image: "https://images.unsplash.com/photo-1591047139829-d91aecb6caea?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 5,
    name: "Collier Demon Slayer",
    series: "Demon Slayer",
    description: "Collier argent symbole Hashira. Style élégant.",
    category: "Bijoux",
    price: 45.99,
    deliveryPrice: 2.99,
    delivery: "standard",
    rating: 4.8,
    image: "https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 6,
    name: "Pull Jujutsu Kaisen",
    series: "Jujutsu Kaisen",
    description: "Pull gris brodé JJK. Parfait pour l’hiver.",
    category: "Vêtements",
    price: 49.99,
    deliveryPrice: 0,
    delivery: "free",
    rating: 4.7,
    image: "https://images.unsplash.com/photo-1576566588028-4147f3842f27?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 7,
    name: "Casquette My Hero Academia",
    series: "My Hero Academia",
    description: "Casquette noire logo UA. Ajustable.",
    category: "Accessoires",
    price: 24.99,
    deliveryPrice: 2.99,
    delivery: "standard",
    rating: 4.6,
    image: "https://images.unsplash.com/photo-1588850561407-ed78c282e89b?auto=format&fit=crop&w=600&q=80"
  },
  {
    id: 8,
    name: "Montre Bleach",
    series: "Bleach",
    description: "Montre minimaliste symbole Soul Reaper.",
    category: "Bijoux",
    price: 129.99,
    deliveryPrice: 0,
    delivery: "free",
    rating: 4.9,
    image: "https://images.unsplash.com/photo-1523170335258-f5ed11844a49?auto=format&fit=crop&w=600&q=80"
  }
],


categories: [
  { id: 1, name: 'Tous' },
  { id: 2, name: 'Vêtements' },
  { id: 3, name: 'Chaussures' },
  { id: 4, name: 'Accessoires' },
  { id: 5, name: 'Bijoux' },
]


    }
  },
  computed: {
   productsFiltered(){
    if(this.selectCategory === 'Tous'){
      return this.products;
    } else {
      return this.products.filter(product => product.category === this.selectCategory);
    }
   }
  },
  methods: {
    // Méthodes vides à implémenter
    selectedCategory(category){
      this.selectCategory = category;
      console.log("Catégorie sélectionnée :", category);
    },
    handleSearchUpdate() {},
    toggleCategoryFilter() {},
    updatePriceFilter() {},
    toggleDeliveryFilter() {},
    resetFilters() {},
    sortProducts() {},
     getWhatsappLink(product) {
    const phone = "237653228070"; // Numéro du vendeur

    const message = `
Bonjour, je suis intéressé par cet article :

 *${product.name}*
 Prix : ${product.price} XAF
 Livraison : ${product.delivery}
 Note : ${product.rating}
 Image : ${product.image}

Pouvez-vous m’en dire plus s’il vous plaît ?
    `;

    const encodedMessage = encodeURIComponent(message);

    return `https://wa.me/${phone}?text=${encodedMessage}`;
  }
  }
}
</script>

<style>
/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #111111;
}

::-webkit-scrollbar-thumb {
  background: #333333;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #444444;
}

/* Smooth transitions */
* {
  transition: background-color 0.3s ease, border-color 0.3s ease;
}
</style>