<template>
  <div>
    <!-- Header Component -->
 <HeaderUser />
 <main>
   <!-- slider Area Start-->
   <div class="slider-area ">
          <div class="single-slider hero-overly slider-height2 d-flex align-items-center" style="background-image: url('assets/img/hero/about.jpg');">
              <div class="container">
                  <div class="row">
                      <div class="col-xl-12">
                          <div class="hero-cap pt-100">
                              <h2>Bienvenue Dans Notre Monde !</h2>
                              
                              <nav aria-label="breadcrumb ">
                                  <ol class="breadcrumb">
                                  <li class="breadcrumb-item"><a href="/">Home</a></li>
                                  <li class="breadcrumb-item"><a href="#">Project</a></li> 
                                  </ol>
                              </nav>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
      <!-- slider Area End-->
        <!-- Services Area Start -->
        <div class="services-area1 section-padding30">
            <div class="container">
                <!-- section tittle -->
                <div class="row">
                    <div class="col-lg-12">
                        <div class="section-tittle mb-55">
                            <div class="front-text">
                                <h2 class="">Aide</h2>
                            </div>
                            <span class="back-text">Services</span>
                        </div>
                    </div>
                </div>
  

<section class="bg-white dark:bg-gray-900">
    <div class="flex flex-col items-center">
  <div class="flex items-center">
    <h1 class="text-3xl font-bold mb-8 text-black">Bienvenue sur</h1>
    <h1 class="text-3xl font-bold mb-8 text-blue-600 ml-2">EstimaPro</h1>
  </div>
  
  <div class="w-3/4">
    <div v-for="(section, index) in sections" :key="index" @click="toggleSection(index)" class="cursor-pointer mb-4">
      <div class="flex items-center">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
        </svg>
        <h2 class="text-2xl font-bold text-gray-800">{{ section.title }}</h2>
      </div>
      <p v-if="section.active" class="text-lg ml-8">{{ section.description }}</p>
    </div>
  </div>
</div>
    <div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md">
        <h2 class="mb-4 text-3xl tracking-tight font-extrabold text-center text-gray-900 dark:text-white">Need Help ?</h2>
        <p class="mb-8 lg:mb-16 font-light text-center text-gray-500 dark:text-gray-400 sm:text-xl">Got a technical issue? Want to ask us about EstimaPro? Need details about our website? Let us know.</p>
        <form action="#" class="space-y-8">
            <div>
                <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300 text-left">Your email</label>
                <input type="email" id="email" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="name@gmail.com" required>
            </div>
            <div>
                <label for="subject" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300 text-left">Subject</label>
                <input type="text" id="subject" class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="Let us know how we can help you" required>
            </div>
            <div class="sm:col-span-2">
                <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400 text-left">Your message</label>
                <textarea id="message" rows="6" class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg shadow-sm border border-gray-300 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500" placeholder="Leave a comment..."></textarea>
            </div>
            <button type="submit" class="py-3 px-5 text-sm font-medium text-center text-white rounded-lg bg-blue-500 sm:w-fit hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800">Send message</button>
        </form>
    </div>
  </section>
</div>
          </div>
      
        <!-- Services Area End -->
      
    </main>
       <!-- Footer Component -->
   <FooterUser />
    </div>
  </template>
  <script>
  import HeaderUser from '../components/HeaderUser.vue'
import FooterUser from '../components/FooterUser.vue'
export default {
  components: {
    HeaderUser,
    FooterUser
  },
  data() {
    return {
      sections: [
        {
          title: 'Estimer sans plan',
          description: "Option 1 : Remplissage du Formulaire\nCliquez sur 'Créer un Nouveau Plan' et remplissez le formulaire interactif avec les détails de votre projet. Notre chatbot générera un plan architectural de base basé sur vos informations. Prévisualisez le plan généré, apportez des ajustements si nécessaire, puis validez.",
          active: false
        },
        {
          title: 'Estimation Global',
          description: "Optez pour l'estimation globale si vous souhaitez une vue d'ensemble des coûts du projet. Remplissez le formulaire sur les matériaux généraux, comprenant des détails tels que le type de construction, les matériaux de construction, la surface au sol, etc.",
          active: false
        },
        {
          title: 'Estimation par Étape',
          description: "Choisissez l'estimation par étape pour une précision accrue. Sélectionnez les étapes spécifiques de votre projet. Remplissez un formulaire détaillé sur les matériaux pour chaque étape choisie.",
          active: false
        },
        {
          title: 'Formulaire des Matériaux (Global ou par Étape)',
          description: "Complétez les formulaires détaillés en fournissant des informations. Consultez les conseils fournis pour prendre des décisions éclairées.",
          active: false
        },
        {
          title: 'Exportation',
          description: "Exportez votre estimation au format PDF pour une référence future.",
          active: false
        },
        {
          title: 'Support et Assistance',
          description: "Si vous avez des questions ou des préoccupations, n'hésitez pas à nous contacter.",
          active: false
        }
      ]
    }
  },
  methods: {
    toggleSection(index) {
      this.sections[index].active = !this.sections[index].active;
    }
  }
}
</script>

<style>
/* Ajoutez vos styles Tailwind CSS personnalisés ici si nécessaire */
</style>