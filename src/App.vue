<template>
  <div id="app" class=" w-full h-screen overflow-y-scroll overflow-x-hidden"> 
    <div id="pp"></div>
    <div id="ppp"></div>
        <span @click="open" v-if="menue" class="menue">
       <i class="fas fa-bars font-bold text-2xl mt-2 ml-2 text-white"></i>
     </span>
     <div class="header">
       <ul class=" font-serif pl-12">
         <li>
          
           <a href="/" >
             <!-- <i class="fas fa-code text-white text-2xl pr-2"></i> -->
             <img src="./assets/file-code-icon.png" class="w-8 absolute h-8 pin-t mt-3"  alt="">
            <span class="text-blue text-2xl font-sans p-0 m-0 pl-8">Code</span> <span class="text-purple-lighter font-mono p-0 m-0">Master</span>
           </a> 
           
         </li>
         <li>
          <a href="/#skills" >Skills</a> 
         </li>
         <li>
            <a href="/#projects" >Projects</a> 
           
         </li>
         <li>
            <a href="/#contact" >Contact</a> 
           
         </li>
       </ul>
     </div>

     <div id="side" class="fade-in absolute ">
       <span @click="close" class="close absolute"><i class="fas fa-times text-2xl text-black"></i></span>
       <a href="/" @click="close" >
             <!-- <i class="fas fa-code text-black text-2xl"></i>
              -->
               <img src="./assets/file-code-icon.png" class="w-8 absolute h-8 pin-t mt-3"  alt="">
            <span class="text-blue-dark text-2xl font-sans p-0 m-0">Code</span> <span class="text-purple-dark font-mono p-0 m-0">Master</span>
          </a> 
      <ul class=" font-serif text-xl font-bold">
         <li>
          <a href="/#skills" @click="close" >Skills</a> 
         </li>
         <li>
            <a href="/#projects" @click="close" >Projects</a> 
           
         </li>
         <li>
            <a href="/#contact" @click="close" >Contact</a> 
           
         </li>
         <li>
           <a href="/#socials" >Socials</a> 
           
         </li>
         <li>
           
         </li>
       </ul>
     </div>
    <!-- landing -->
    <div class=" w-full container h-screen m-auto justify-around  mb-2 head">
      <div class=" text-center rounded-full logo">
        <img src="./assets/gMFLZ1cD_400x400.jpg" alt="" class="w-2/3 m-auto">
      </div>

      <div class="text-white text-center text-2xl text">
        <h1 class="py-0 my-0">I am Ben Josiah</h1>
        <h3 class="py-0 my-1">Full-Stack Web Developer</h3>
        <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eveniet, voluptatibus.
        </p>
      </div>
    </div>
    
    <!-- Skills -->
     
    <div class="pb-10 w-4/5 md:w-full m-auto mt-10 " id="skills">
    <h1 class=" text-grey-light">Skills :</h1>
    <div class="flex text-black font-black flex-wrap lg:justify-between justify-around h-full w-full">
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">   Programing Languages :</h3>
          <ul>
            <li v-for="(language, lan) in Skills.languages"  :key="lan" class=" inline pr-6">
               <i :class="`${language.icon} text-blue-darker`"></i> 
                {{language.language}}
            </li>
          </ul>
        </div>
        <div class="  sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">  Frameworks :</h3>
          <ul>
            <li v-for="(framework, frame) in Skills.Frameworks"  :key="frame" class=" inline pr-6">
               <i :class="`${framework.icon} text-blue-darker`"></i> 
               {{framework.Framework}}
            </li>
          </ul>
        </div>
        <div class="md:w-2/5 sm:w-4/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker ">   Vue :</h3>
          <ul>
            <li v-for="(vue, v) in Skills.vue"  :key="v" class=" inline pr-6">
               <i :class="`${vue.icon} text-green-darker `"></i> 
               {{vue.vue}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Laravel :</h3>
          <ul>
            <li v-for="(laravel, l) in Skills.laravel"  :key="l" class=" inline pr-6">
               <i :class="`${laravel.icon} text-red-darker`"></i> 
               {{laravel.laravel}}
            </li>
          </ul>
        </div>
         <div class="sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker">  Tools :</h3>
          <ul>
            <li v-for="(tool, t) in Skills.tools"  :key="t" class=" inline pr-6">
               <i :class="`${tool.icon} text-blue-darker`"></i> 
               {{tool.tool}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker"> Storage/Database :</h3>
          <ul>
            <li v-for="(storage, Sk) in Skills.Storage"  :key="Sk" class=" inline pr-6">
               <i :class="`${storage.icon} text-blue-darker`"></i> 
               {{storage.name}}
            </li>
          </ul>
        </div>
        <div class=" sm:w-4/5 md:w-2/5 bg-grey-light opacity-100 mt-4 px-8 py-2 rounded-lg">
          <h3 class="text-semibold text-blue-darker"> Cloud/Hosting :</h3>
          <ul>
            <li v-for="(storage, s) in Skills.Cloud"  :key="s" class=" inline pr-6">
               <i :class="`${storage.icon} text-blue-darker`"></i> 
               {{storage.name}}
            </li>
          </ul>
        </div>
    </div>
    </div>
    <!-- Projects -->
    <div class=" container m-auto" id="projects" >
      <h1 class=" text-white font-bold">
        Projects :
      </h1>
      <div class="flex flex-wrap justify-center  w-full pb-10">
        
        <div v-for="(Project, p) in Projects"  :key="p"  class="pro h-auto bg-black text-blue-lightest m-1 py-4 px-2">
            <h3 class=" font-bold">{{Project.name}}</h3>
            <p v-html="Project.description" class="border-solid border-grey hi border-0  border-b-2"></p>
            <ul class="p-0">
              <li class=" inline pr-3" v-if="Project.code">
                <a :href="Project.code" class=" text-yellow-dark no-underline">
               <i class="fas fa-code text-yellow-dark"></i> 
               Code
               </a>
              </li>
              <li class=" inline pr-3" v-if="Project.back">
                <a :href="Project.back" class=" text-orange no-underline">
               <i class="fab fa-git-alt "></i> 
                  Backend
               </a>
              </li>
               <li v-if="Project.Url" class="inline pr-3 cursor-pointer text-green-dark ">
                <a :href="Project.Url" class=" text-green-dark no-underline">
                  <i class="fas fa-chart-line "></i> 
                  Live URL
                </a>
              </li> 
              
               <li  v-if="Project.docs" class="inline pr-3 ">
                <a :href="Project.docs" class=" text-blue no-underline">
                  <i class="fas fa-file-word "></i> 
                  Docs
                </a>
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
    <!-- contact -->
   
    <div id="contact" class=" container m-auto w-full my-32">
      <h1 class=" text-white font-bold">
        Contact Me :
      </h1>
      <form action="" class="text-center w-2/3 m-auto">
        <div class="py-1">
           <input type="email" name="" id="" placeholder="Email Address" class=" px-2 m-auto text-lg text-left  h-10 rounded-lg focus:outline-none con">
        </div>
       <div class="py-1"> 
           <input type="text" name="" id="" placeholder="Full Name" class="px-2 m-auto con text-lg h-10 rounded-lg focus:outline-none" >
        </div>
        <div class="py-1">
          <textarea name="" placeholder="Text" class="px-2 con h-24 rounded-lg text-lg focus:outline-none" ></textarea>
        </div>
         <div class="py-1">
           <input type="submit" name="" id="" class="px-8 py-4 text-lg font-semibold rounded-full shadow-none outline-none bg-blue-dark"> 
        </div>
     
      </form>
    </div>
    <div class="w-full text-center text-grey pb-4"> @Copyright Codemaster 2021</div>
    <div class=" ">
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
      <!-- <div id="ball11" class="ball"></div>
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
      <div id="ball22" class="ball"></div> -->
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

        {name:"Twitter-UI-clone", description:"A clone of the <a href='https://twitter.com'> Twitter</a> UI", code:"https://github.com/benjosiah/twitter-clone", Url:"https://vuetwitter.netlify.app/", tools:["Vue", "Tailwindcss"]},
        {name:"Todo App", description:"A regular todo Application with user Authentication", code:"https://github.com/benjosiah/todo-app-vue-frontend", back:"https://github.com/benjosiah/todo_app_laravel_api", Url:"https://wonderful-carson-956137.netlify.app/", tools:["Vue","vuex", "laravel", "axios", "pasport", "guzzle"]},
        {name:"Social Network", description:"A social Network replical. with likes, comments follow and messaging functionalities", code:"https://github.com/benjosiah/social-network", tools:["laravel", "bootstrap"], docs:""},
        {name:"flexit", description:"An Online Store with ", code:"https://github.com/benjosiah/flexit", tools:["laravel", "bootstrap", "guzzle"]},
        {name:"Real Calculator", description:"A basic business calculator,", code:"https://github.com/benjosiah/real-calculator", Url:"https://calsmart1234.web.app/", tools:["vue"]},
        {name:"PHP framwork", description:"A PHP MVC framworkwork project for web development with templating engine, costome routing database migrations and a command line experience", code:"https://github.com/benjosiah/php-framework", tools:["PHP"], docs:""},
        {name:"Todo UI", description:"A regular javaScript todo project", code:"https://github.com/benjosiah/todo-app-javascript", Url:"https://todo-ui.netlify.app/", tools:["vanilla Javascript"]},
        {name:"CUR VER", description:"A currency converter", code:"https://github.com/benjosiah/CUR-VER", tools:["vue", "Vue-recource","Rapid Api" ]},
        {name:"Banker PHP", description:"A PHP parckage that aids online payment integration using flutterwave's rave api", code:"https://github.com/benjosiah/ben-banker_php", Url:"", tools:["PHP", "cURL", "Rave Api"], docs:"https://master.hashnode.dev/ben-bankerphp"},
        {name:"MyDiary", description:"A diary application. with user Authentication", code:"https://github.com/benjosiah/myDiary", tools:["Vue", "Vue-resource", "fire Authentication", "fire Store"]},
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
      },
      show:false,
      menue: true
    }
  },
  methods : {
    open(){
        document.getElementById('side').style.width="200px"
    },

    close(){
        document.getElementById('side').style.width="0px";
       
    }
  }
}
</script>

<style>
 
.pro{
  width: 23%;
  
}

.header{
  display: block;
  width: 100%;
  height: 70px;
  position: fixed;
  background: rgba(0, 0, 0, 0.938);
}
.header ul{
  width: 100%;
  height: 100%;
  margin: 15px 0;
  vertical-align: middle;
}

.header ul li{
  display:inline;
  padding-right: 25px;
  margin: 5px 0px;
  font-size: 20px;
  color: azure;
}
.header ul li a{
  color: azure;
  text-decoration: black;
}
.header ul li a:hover{
  color: rgb(178, 184, 189);
}
.fade-in{
  display: none;
}

.menue{
  position: absolute;
  top: 0%;
  left: 0;
  display:none;
}

.head{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.text{
  order: 1;
  width: 45%;
}

.logo{
  width: 45%;
  order: 2;
}

.con{
  width:80%;
   }

 @media screen and (max-width: 997px){
   .pro{
     width:30%;
   }

   .hi{
     min-height: 100px;
   }

   .con{
  width:80%;
   }
}

 

@media screen and (max-width: 770px){
.pro{
  width:45%;
}
  .header{
    display: none;
  }
 .fade-in{
    width: 0px;
   height: 100vh;
  display: block;
  overflow: hidden;
   background-color: white;
   transition: .7s;
   padding-top:60px;
  }
  .fade-in ul{
    height: 100%;
    margin: 0%;
  }

  .fade-in ul li{
    list-style: none;
    padding:30px 5px;
  }
  a{
    padding: 10px;
    text-decoration: none;
  }
  .fade-in ul li a{
  
    text-decoration: none;
    color: black;
  }
 

.menue{
  position: absolute;
  top: 0%;
  left: 0;
  display:block;
}

.close{
  position: absolute;
  top: 0;
  right:3px;
  
}

.head{
  display: block;
}
.logo{
  width: 60%;
  margin: auto;
  text-align: center;
  margin-top: 45%;
}
.logo img{
  margin: auto;
}
.text{
  width: 100%;
  margin-top: 0%;
    order: 2;
}

.con{
  width:90%;

}
}



@media screen and (max-width: 480px){
.pro{
  width:90%;
}
.con{
  width:100%;
}
.balls{
  display: none;
}

}






</style>
