# CSS "Coding" animation

This is continuing on my odd fascination with animation in the browser, building on my previous attempt at an [animated SVG graphic](http://chrisdermody.com/animated-svg-loader-mydevportfol-io/) that would illustrate that an app was "coding" a website, originally built for my side project [MyDevPortfolio](https://mydevportfol.io)

[view the animation](https://chippd.github.io/css_loading_animation/)


## Tutorial
If you'd like to see how easy this can be done, I'll be creating a tutorial in an upcoming post. Get notifified about it [here](http://chrisdermody.com/subscribing/?utm_source=github&utm_medium=css-loader-repo&utm_campaign=eng_mark).

I'm [@cderm](https://twitter.com/cderm) on Twitter too ;)

<style>
    
   /* colors of monokai: http://www.colourlovers.com/palette/1718713/Monokai
       orchid(pink): #F92672
       bounded rationality (blue): #66D9EF
       henn1nk (green): #A6E22E
       pumpkin spice (orange): #FD971F 
    */

   :root {
         --orchid: #F92672;
         --br-blue: #66D9EF;
         --henn1nk: #A6E22E;
         --spice: #FD971F;
         --classColour: #FFE792;
         --parColour: #F8F8F2;
   }

   body {
     background: #272822;
   }

   .loader-container {
     width:400px;
     height:175px;
     margin:auto;
      margin-top:30vh;
     overflow:hidden;
   }

   .line {
     margin-top:5px
   }

   .dash {
     height:20px;
     display: inline-block;
     border-radius: 10px
   }

   .div {
     background: var(--orchid);
   }

   .class-name {
     background: var(--henn1nk);
   }

   .class {
     background: var(--classColour);
   }

   .par {
     background: var(--parColour);
   }

   .exp-40 {
     animation: expand-40 0.2s linear forwards;
   }

   .exp-70 {
     animation: expand-70 0.2s linear forwards;
   }

   .exp-90 {
     animation: expand-90 0.2s linear forwards;
   }

   .exp-110 {
     animation: expand-110 0.2s linear forwards;
   }

   .exp-200 {
     animation: expand-200 0.2s linear forwards;
   }

   .exp-300 {
     animation: expand-300 0.2s linear forwards;
   }

   .line1 .dash-1 {
    /*animation-delay: 0.1s;*/
   }

   .line1 .dash-2 {
     animation-delay: 0.1s;
   }

   .line1 .dash-3 {
      animation-delay: 0.2s;
   }

   .line1 .dash-4 {
      animation-delay: 0.3s;
   }

   .line2 {
     margin-left:10%;
   }

   .line2 .dash-1 {
     animation-delay: 0.4s
   }

   .line2 .dash-2 {
     animation-delay: 0.5s
   }

   .line2 .dash-3 {
     animation-delay: 0.6s
   }

   .line3 {
     margin-left:20%;
   }

   .line3 .dash-1 {
     animation-delay: 0.7s
   }

   .line4 {
     margin-left: 20%
   }

   .line4 .dash-1 {
     animation-delay: 0.8s
   }

   .line5 {
     margin-left: 10%
   }

   .line5 .dash-1 {
     animation-delay: 0.85s
   }

   .line6 .dash-1 {
     animation-delay: 0.925s
   }

   .group-1 {
     animation: scroll 1s linear infinite;
     animation-delay: 1s;
     position:relative;
   }

   .group-2 {
     animation: scroll 1s linear infinite;
     animation-delay: 1s;
     position:relative;
   }


   .group-2 .line1 .dash-1 {
     animation: line1dash1 1s linear infinite;
   }

   .group-2 .line1 .dash-2 {
     animation: line1dash2 1s linear infinite;
   }

   .group-2 .line1 .dash-3 {
     animation: line1dash3 1s linear infinite;
   }

   .group-2 .line1 .dash-4 {
     animation: line1dash4 1s linear infinite;
   }

   .group-2 .line2 .dash-1 {
     animation: line2dash1 1s linear infinite;
   }

   .group-2 .line2 .dash-2 {
     animation: line2dash2 1s linear infinite;
   }

   .group-2 .line2 .dash-3 {
     animation: line2dash3 1s linear infinite;
   }

   .group-2 .line3 .dash-1 {
     animation: line3dash1 1s linear infinite;
   }

   .group-2 .line4 .dash-1 {
     animation: line4dash1 1s linear infinite;
   }

   .group-2 .line5 .dash-1 {
     animation: line5dash1 1s linear infinite;
   }

   .group-2 .line6 .dash-1 {
     animation: line6dash1 1s linear infinite;
   }
  
    /*keyframes for group2*/
   @keyframes line1dash1 {
       0% {
         width: 0px;
       }
       20% {
         width: 40px;
       }
       100% {
        width: 40px;
       }
   }

   @keyframes line1dash2 {
       0% {
         width: 0px;
       }
       10% {
         width: 0px;
       }
       30% {
        width: 70px;
       }
       100% {
        width: 70px;
       }
   }

   @keyframes line1dash3 {
       0% {
         width: 0px;
       }
       20% {
         width: 0px;
       }
       40% {
        width: 110px;
       }
       100% {
        width: 110px;
       }
   }

   @keyframes line1dash4 {
       0% {
         width: 0px;
       }
       30% {
         width: 0px;
       }
       50% {
        width: 70px
       }
       100% {
        width: 70px;
       }
   }

   @keyframes line2dash1 {
       0% {
         width: 0px;
       }
       40% {
         width: 0px;
       }
       60% {
        width: 40px
       }
       100% {
        width: 40px;
       }
   }

   @keyframes line2dash2 {
       0% {
         width: 0px;
       }
       50% {
         width: 0px;
       }
       70% {
        width: 70px
       }
       100% {
        width: 70px;
       }
   }

   @keyframes line2dash3 {
       0% {
         width: 0px;
       }
       60% {
         width: 0px;
       }
       80% {
        width: 90px
       }
       100% {
        width: 90px;
       }
   }

   @keyframes line3dash1 {
       0% {
         width: 0px;
       }
       60% {
         width: 0px;
       }
       80% {
        width: 300px
       }
       100% {
        width: 300px;
       }
   }

   @keyframes line4dash1 {
       0% {
         width: 0px;
       }
       70% {
         width: 0px;
       }
       90% {
        width: 200px
       }
       100% {
        width: 200px;
       }
   }

   @keyframes line5dash1 {
       0% {
         width: 0px;
       }
       75% {
         width: 0px;
       }
       85% {
        width: 40px
       }
       100% {
        width: 40px;
       }
   }

   @keyframes line6dash1 {
       0% {
         width: 0px;
       }
       85% {
         width: 0px;
       }
       100% {
        width: 40px;
       }
   }


   @keyframes expand-40 {
       from {
         width: 0px;
       }
       to {
         width: 40px;
       }
   }

   @keyframes expand-70 {
       from {
         width: 0px;
       }
       to {
         width: 70px;
       }
   }

   @keyframes expand-90 {
       from {
         width: 0px;
       }
       to {
         width: 90px;
       }
   }

   @keyframes expand-110 {
       from {
         width: 0px;
       }
       to {
         width: 110px;
       }
   }


   @keyframes expand-200 {
       from {
         width: 0px;
       }
       to {
         width: 200px;
       }
   }

   @keyframes expand-300 {
       from {
         width: 0px;
       }
       to {
         width: 300px;
       }
   }

  @keyframes scroll {
       from {
         top: 0px;
       }
       to {
         top: -175px;
       }
   }
  </style>
</head>
<body>

  <div class="loader-container">

  <div class="group-1">
    <div class="line line1">
      <div class="dash dash-1 exp-40 div"></div>
      <div class="dash dash-2 exp-70 class-name"></div>
      <div class="dash dash-3 exp-110 class"></div>
      <div class="dash dash-4 exp-70 class"></div>
    </div>
    <div class="line line2">
      <div class="dash dash-1 exp-40 div"></div>
      <div class="dash dash-2 exp-70 class-name"></div>
      <div class="dash dash-3 exp-90 class"></div>
    </div>
    <div class="line line3">
      <div class="dash dash-1 exp-300 par"></div>
    </div>
    <div class="line line4">
      <div class="dash dash-1 exp-200 par"></div>
    </div>
    <div class="line line5">
      <div class="dash dash-1 exp-40 div"></div>
    </div>
    <div class="line line6">
      <div class="dash dash-1 exp-40 div"></div>
    </div>
  </div>


  <div class="group-2">
    <div class="line line1">
      <div class="dash dash-1 div"></div>
      <div class="dash dash-2 class-name"></div>
      <div class="dash dash-3 class"></div>
      <div class="dash dash-4 class"></div>
    </div>
    <div class="line line2">
      <div class="dash dash-1 div"></div>
      <div class="dash dash-2 exp70 class-name"></div>
      <div class="dash dash-3 exp90 class"></div>
    </div>
    <div class="line line3">
      <div class="dash dash-1 par"></div>
    </div>
    <div class="line line4">
      <div class="dash dash-1 par"></div>
    </div>
    <div class="line line5">
      <div class="dash dash-1 div"></div>
    </div>
    <div class="line line6">
      <div class="dash dash-1 div"></div>
    </div>
  </div>
</div>
