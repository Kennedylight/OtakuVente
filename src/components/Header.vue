<template>
    <header class="sticky top-0 z-50 bg-black/90 backdrop-blur-md border-b border-gray-900">
        <div class="container mx-auto px-6 py-5">
            <div class="flex items-center justify-between">

                <!-- Logo -->
                <div class="flex items-center">
                    <div class="w-9 h-9 bg-red-600 rounded-lg mr-3"></div>
                    <div>
                        <div class="text-xl font-bold text-white">OTAKU<span class="text-red-500">.</span></div>
                        <div class="text-gray-500 text-xs">store</div>
                    </div>
                </div>

                <!-- Navigation -->
            <nav class="hidden md:flex items-center justify-center space-x-10 ">
                <a href="#"
                    class="text-gray-400 hover:text-white transition-colors pb-2 border-b-2 border-transparent hover:border-red-500">Accueil</a>
                <a href="#"
                    class="text-gray-400 hover:text-white transition-colors pb-2 border-b-2 border-transparent hover:border-red-500">Collections</a>
                <a href="#"
                    class="text-gray-400 hover:text-white transition-colors pb-2 border-b-2 border-transparent hover:border-red-500">Nouveautés</a>
                <a href="#"
                    class="text-gray-400 hover:text-white transition-colors pb-2 border-b-2 border-transparent hover:border-red-500">Promotions</a>
                <a href="#"
                    class="text-gray-400 hover:text-white transition-colors pb-2 border-b-2 border-transparent hover:border-red-500">Contact</a>
            </nav>

                
                <div class="flex items-center space-x-4">

                    <!-- Desktop Search -->
                    <div class="hidden md:block relative">
                        <input v-model="searchQuery" type="text" placeholder="Rechercher..."
                            class="w-80 pl-4 pr-10 py-2.5 bg-gray-900 border border-gray-800 rounded-lg text-white placeholder-gray-500 focus:outline-none focus:border-red-500 transition-colors">
                        <div class="absolute right-3 top-2.5 text-gray-500">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                class="size-6">
                                <path fill-rule="evenodd"
                                    d="M10.5 3.75a6.75 6.75 0 1 0 0 13.5 6.75 6.75 0 0 0 0-13.5ZM2.25 10.5a8.25 8.25 0 1 1 14.59 5.28l4.69 4.69a.75.75 0 1 1-1.06 1.06l-4.69-4.69A8.25 8.25 0 0 1 2.25 10.5Z"
                                    clip-rule="evenodd" />
                            </svg>

                        </div>
                    </div>


                </div>

            </div>

            

        </div>
    </header>
</template>