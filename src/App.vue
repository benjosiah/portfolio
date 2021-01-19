<template>
  <div id="app" class=" w-full"> 
    <!-- landing -->
    <div class="flex flex-wrap w-full container h-screen m-auto items-center justify-around">
      
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
    <div class="flex text-black font-black flex-wrap lg:justify-between justify-around h-full w-full">
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">   Programing Languages :</h3>
          <ul>
            <li v-for="language in Skills.languages"  :key="language" class=" inline pr-6">
               <i :class="`${language.icon} text-blue-darker`"></i> 
                {{language.language}}
            </li>
          </ul>
        </div>
        <div class="  sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">  Frameworks :</h3>
          <ul>
            <li v-for="framework in Skills.Frameworks"  :key="framework" class=" inline pr-6">
               <i :class="`${framework.icon} text-blue-darker`"></i> 
               {{framework.Framework}}
            </li>
          </ul>
        </div>
        <div class="md:w-2/5 sm:w-4/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">   Vue :</h3>
          <ul>
            <li v-for="vue in Skills.vue"  :key="vue" class=" inline pr-6">
               <i :class="`${vue.icon} text-green-darker `"></i> 
               {{vue.vue}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Laravel :</h3>
          <ul>
            <li v-for="laravel in Skills.laravel"  :key="laravel" class=" inline pr-6">
               <i :class="`${laravel.icon} text-red-darker`"></i> 
               {{laravel.laravel}}
            </li>
          </ul>
        </div>
         <div class="sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Tools :</h3>
          <ul>
            <li v-for="tool in Skills.tools"  :key="tool" class=" inline pr-6">
               <i :class="`${tool.icon} text-blue-darker`"></i> 
               {{tool.tool}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker"> Storage/Database :</h3>
          <ul>
            <li v-for="storage in Skills.Storage"  :key="storage" class=" inline pr-6">
               <i :class="`${storage.icon} text-blue-darker`"></i> 
               {{storage.name}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
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
      <h1 class=" text-white font-bold">
        Projects :
      </h1>
      <div class="flex flex-wrap justify-center  w-full pb-10">
        
        <div v-for="Project in Projects"  :key="Project"  class="  h-auto bg-black text-blue-lightest  w-pop lg:w-2/5 m-1 py-4 px-2">
            <h3 class=" font-bold">{{Project.name}}</h3>
            <p v-html="Project.description" class="border-solid border-grey  h-24 border-0  border-b-2"></p>
            <ul class="p-0">
              <li class=" inline pr-3" v-if="Project.code">
               <i class="fas fa-code text-yellow-dark"></i> 
               Code
              </li>
               <li class="inline pr-3 cursor-pointer">
               <i class="fas fa-chart-line text-green-dark"></i> 
               Live URL
              </li> 
               <li class="inline pr-3">
               <i class="fas fa-file-word text-blue-dark"></i> 
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
    <div class=" hidden">
      <div id="ball1" class="ball"></div>
      <div id="ball2" class="ball"></div>
      <div id="ball3" class="ball"></div>
      <div id="ball4" class="ball"></div>
      <div id="ball5" class="ball"></div>
      <div id="ball6" class="ball"></div>
      <div id="ball7" class="ball"></div>
      <div id="ball8" class="ball"></div>
      <div id="ball9" class="ball"></div>
      <div id="ball10" class="ball"></div>
      <div id="ball11" class="ball"></div>
      <div id="ball12" class="ball"></div>
      <div id="ball13" class="ball"></div>
      <div id="ball14" class="ball"></div>
      <div id="ball15" class="ball"></div>
      <div id="ball16" class="ball"></div>
      <div id="ball17" class="ball"></div>
      <div id="ball23" class="ball"></div>
      <div id="ball24" class="ball"></div>
      <div id="ball18" class="ball"></div>
      <div id="ball19" class="ball"></div>
      <div id="ball20" class="ball"></div>
      <div id="ball121" class="ball"></div>
      <div id="ball22" class="ball"></div>
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

        {name:"Twitter-UI-clone", description:"A clone of the <a href=''> Twitter</a> UI", code:"", Url:"", tools:["Vue", "Tailwindcss"]},
        {name:"Todo App", description:"A regular todo Application with user Authentication", code:"", back:"", Url:"", tools:["Vue","vuex", "laravel", "axios", "pasport", "guzzle"]},
        {name:"Social Network", description:"A social Network replical. with likes, comments follow and messaging functionalities", code:"", tools:["laravel", "bootstrap"], docs:""},
        {name:"flexit", description:"An Online Store with ", code:"", tools:["laravel", "bootstrap", "guzzle"]},
        {name:"Real Calculator", description:"A basic business calculator,", code:"", Url:"", tools:["vue"]},
        {name:"PHP framwork", description:"A PHP MVC framworkwork project for web development with templating engine, costome routing database migrations and a command line experience", code:"", tools:["PHP"], docs:""},
        {name:"Todo UI", description:"A regular javaScript todo project", code:"", Url:"", tools:["vanilla Javascript"]},
        {name:"CUR VER", description:"A currency converter", code:"", tools:["vue", "Vue-recource","Rapid Api" ]},
        {name:"Banker PHP", description:"A PHP parckage that aids online payment integration using flutterwave's rave api", code:"", Url:"", tools:["PHP", "cURL", "Rave Api"], docs:""},
        {name:"MyDiary", description:"A diary application. with user Authenticatin", code:"", tools:["Vue", "Vue-resource", "fire Authentication", "fire Store"]},
      ],
      socials:{
        facebook:"https://",
        twitter:"https://twitter.com/josiahben_",
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
