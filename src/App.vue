<template>
  <div id="app" class=" w-full"> 
    <!-- landing -->
    <div class="flex flex-wrap w-full m-auto items-center justify-around">
      
      <div class="text-white text-center text-2xl w-9/20 border-solid">
        <h1 class="py-0 my-0">I am Ben Josiah</h1>
        <h3 class="py-0 my-1">Full-Stack Developer</h3>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eveniet, voluptatibus.
      </div>
      <div class="w-9/20 pr-16 text-center border-solid">
        <img src="./assets/logo.png" alt="">
      </div>
    </div>
    <!-- Skills -->
    <div class="pb-10 w-4/5 md:w-full m-auto ">
    <h1 class=" text-grey-light">Skills :</h1>
    <div class="flex flex-wrap lg:justify-between justify-around h-full w-full">
        <div class=" sm:w-4/5 md:w-2/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">   Programing Languages :</h3>
          <ul>
            <li v-for="language in Skills.languages"  :key="language" class=" inline pr-6">
               <i :class="`${language.icon} text-blue-darker`"></i> 
                {{language.language}}
            </li>
          </ul>
        </div>
        <div class="  sm:w-4/5 md:w-2/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">  Frameworks :</h3>
          <ul>
            <li v-for="framework in Skills.Frameworks"  :key="framework" class=" inline pr-6">
               <i :class="`${framework.icon} text-blue-darker`"></i> 
               {{framework.Framework}}
            </li>
          </ul>
        </div>
        <div class="md:w-2/5 sm:w-4/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">   Vue :</h3>
          <ul>
            <li v-for="vue in Skills.vue"  :key="vue" class=" inline pr-6">
               <i :class="`${vue.icon} text-blue-darker `"></i> 
               {{vue.vue}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Laravel :</h3>
          <ul>
            <li v-for="laravel in Skills.laravel"  :key="laravel" class=" inline pr-6">
               <i :class="`${laravel.icon} text-blue-darker`"></i> 
               {{laravel.laravel}}
            </li>
          </ul>
        </div>
         <div class="sm:w-4/5 md:w-2/5 bg-grey-dark opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Tools :</h3>
          <ul>
            <li v-for="tool in Skills.tools"  :key="tool" class=" inline pr-6">
               <i :class="`${tool.icon} text-blue-darker`"></i> 
               {{tool.tool}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker"> Storage/Database :</h3>
          <ul>
            <li v-for="storage in Skills.Storage"  :key="storage" class=" inline pr-6">
               <i :class="`${storage.icon} text-blue-darker`"></i> 
               {{storage.name}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-white opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker"> Cloud/Hosting :</h3>
          <ul>
            <li v-for="storage in Skills.Cloud"  :key="storage" class=" inline pr-6">
               <i :class="`${storage.icon} text-blue-darker`"></i> 
               {{storage.name}}
            </li>
          </ul>
        </div>
    </div>
    </div>
    <!-- Projects -->
    <div class=" container m-auto">
      <div class="flex flex-wrap justify-center w-full pb-10">
        
        <div v-for="Project in Projects"  :key="Project"  class="bg-black text-blue-lightest h-auto sm:w-pop lg:w-2/5 m-1 py-4 px-2">
            <h3>{{Project.name}}</h3>
            <p v-html="Project.description" class="border-solid border-grey border-0  border-b-2 h-16"></p>
            <ul class="p-0">
              <li class=" inline pr-3">
               <i class="fas fa-code text-blue-darker"></i> 
               Code
              </li>
               <li class="inline pr-3">
               <i class="fas fa-chart-line text-blue-darker"></i> 
               Live URL
              </li> 
               <li class="inline pr-3">
               <i class="fas fa-file-word text-blue-darker"></i> 
               Docs
              </li>
            </ul>
            <h5 class="text-sm m-0 p-1">
              Technologies:
            </h5>
            <div class="m-0 flex flex-wrap items-center justify-start"> 
            <div class=" w-auto py- px-1 bg-red-darkest m-1 rounded-lg text-center " v-for="tech in Project.tools" :key="tech">
              {{tech}}
            </div>
          </div>
          
        </div>
      </div>
    </div> 

  </div>
</template>

<script>


export default {
  name: 'App',
  components: {
    
  },
  data(){
    return{
      Skills:{
        "languages":[
          {language:"JavaScript", icon:" fab fa-js" },
          { language:"PHP", icon:" fab fa-php" },
          {language:"Python", icon:"fab fa-python" }
         ],
        "Frameworks":[
          {Framework:"Bootstrap", icon:"fab fa-css3" },
          {Framework:"Tailwind", icon:"fab fa-css3" },
          {Framework:"Vue", icon:"fab fa-vuejs" },
          {Framework:"Laravel", icon:"fab fa-laravel" },
          {Framework:"Symfony", icon:"fab fa-symfony" },
        ],
        "tools":[
          {tool:"Git", icon:"fab fa-git" },
          {tool:"Github", icon:"fab fa-github" },
          {tool:"Firebase", icon:"fas fa-fire" },
        ],
        "vue":[
              {vue:"Vuex", icon:"fab fa-vuejs" },
              {vue:"Vue-Recouurce", icon:"fab fa-vuejs" },
              {vue:"vue-Router", icon:"fab fa-vuejs" }
          
        ],
        "laravel":[
          {laravel:"Passport", icon:"fab fa-laravel" },
          {laravel:"Socialite", icon:"fab fa-socialite" },
          {laravel:"Guzzle", icon:"fab fa-guzzle" }
        ],
        "Storage":[
          {name:"SQL", icon:"fas fa-database" },
          {name:"Posstgress", icon:"fas fa-elephant" },
          {name:"MongoDB", icon:"fas fa-leaf" },
          {name:"FireStore", icon:"fas fa-globe-africa" }

        ],
        "Cloud":[
          {name:"Heroku", icon:"fab fa-heroku" },
          {name:"Fire Hosting", icon:"fas fa-globe-africa" },
          {name:"Netlify", icon:"fab fa-netlify" },
          
        ],
        "professional":[
          {name:"Heroku", icon:"fab fa-heroku" },
          {name:"Fire Hosting", icon:"fas fa-globe-africa" },
          {name:"Netlify", icon:"fab fa-netlify" },
          
        ],
      },
      Projects:[

        {name:"Twitter-UI-clone", description:"A clone of the <a href=''> Twitter</a> UI", code:"", back:"", Url:"", tools:["Vue", "Tailwindcss"], docs:""},
        {name:"Todo App", description:"A regular todo Application with user Authentication", code:"", Url:"", tools:["Vue","vuex", "laravel", "axios", "pasport", "guzzle"], docs:""},
        {name:"Social Network", description:"A social Network replical. with likes, comments follow and messaging functionalities", code:"", Url:"", tools:["laravel", "bootstrap"], docs:""},
        {name:"flexit", description:"An Online Store with ", code:"", Url:"", tools:["laravel", "bootstrap", "guzzle"], docs:""},
        {name:"Real Calculator", description:"", code:"", Url:"", tools:["vue"], docs:""},
        {name:"PHP framwork", description:"", code:"", Url:"", tools:["PHP"], docs:""},
        {name:"Todo UI", description:"", code:"", Url:"", tools:["vanilla Javascript"], docs:""},
        {name:"CUR VER", description:"", code:"", Url:"", tools:["vue", "Vue-recource","Rapid Api" ], docs:""},
        {name:"Banker PHP", description:"", code:"", Url:"", tools:["PHP", "cURL", "Rave Api"], docs:""},
        {name:"MyDiary", description:"", code:"", Url:"", tools:["Vue", "Vue-resource", "fire Authentication", "fire Store"], docs:""},
      ],
      socials:{
        facebook:"",
        twitter:"",
        instagram:"",
        whatsapp:"",
        linklnd:"",
        github:"",
        midium:"",
        hashnode:""
      }
    }
  }
}
</script>

<style>

</style>
