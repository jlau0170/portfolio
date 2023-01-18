<template>
    <transition name="fade">
    <div class="page-loader" v-if="!isloaded">
        <div class="loading-container">
        <div class="loading"></div>
          <div id="loading-text"><img class="logo" alt="JLau logo" src="../images/lightLogo.png" width="150" height="150" /></div>
      </div>
    </div> 
    </transition>
  </template>
  
  <script>
    export default {
      data: () => {
        return {
          isloaded: false
        }
      },
      mounted() {
        document.onreadystatechange = () => {
          if (document.readyState == "complete") { 
            setTimeout(() => this.isloaded = true, 2000);
          } 
        }
      },
    }
  </script>
  
  <style lang="scss" scoped>
    // -----------------------------------------------------
    .page-loader {
      display: flex;
      justify-content: center;
      align-items: center;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: #1b1b1b;
      z-index: 999;
    }
    
    // -----------------------------------------------------
    @keyframes top {
        40% {
            transform: translateY(20px);
        }
        50% {
            transform: translateY(0);
        }
    }

    @keyframes rotate-loading {
            0%  {transform: rotate(0deg);}
            100% {transform: rotate(360deg);}
        }

        @keyframes rotate-loading {
            0%  {transform: rotate(0deg);}
            100% {transform: rotate(360deg);}
        }
        @keyframes loading-text-opacity {
            0%  {opacity: 0}
            20% {opacity: 0}
            50% {opacity: 1}
            100%{opacity: 0}
        }

        .loading-container,
        .loading {
            height: 150px;
            position: relative;
            width: 150px;
            border-radius: 50%;
        }


        .loading-container { margin: 40px auto }

        .loading {
            border: 2px solid transparent;
            border-color: transparent #fff transparent #FFF;
            animation: rotate-loading 1.5s linear 0s infinite normal;
            transform-origin: 50% 50%;
        }

        .loading-container:hover .loading {
            border-color: transparent rgb(6, 87, 174) transparent rgb(6, 87, 174);
        }
        .loading-container:hover .loading,
        .loading-container .loading {
            transition: all 0.5s ease-in-out;
        }

        #loading-text {
            animation: loading-text-opacity 2s linear 0s infinite normal;
            opacity: 0;
            position: absolute;
            text-align: center;
            top: 0;
            width: 100px;
        }

        .fade-enter-active, .fade-leave-active {
          transition: all 1.0s;
        }
        .fade-enter {
          opacity: 0;
        }
        .fade-leave-to {
          opacity: 0;
        }
        /*
        .fade-enter-active, .fade-leave-active {
          transition: 5s;
        }
        .fade-enter
        {
          transform: translate(100%, 0);
        } 
        .fade-leave-to {
          transform: translate(-680px, -380px);
        }
        */
  </style>