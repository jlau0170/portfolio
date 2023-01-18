<template>
    <main class="background">
      <h1>
        Experience
      </h1>

      <!--MICROSOFT-->
      <div style="bottom: 700px;" class="glass">
        <div class="glass-inner">
          <div class="glass-front">
            <img style="top: 100px;" alt="Microsoft" src="../images/microsoft.png" width="440" height="330" />
          </div>
          <div class="glass-back">
            <div class="content">
              <h2 style="top: 240px; color:black;">Microsoft</h2>
              <h2 style="top: 240px; color:black;">Software Engineering Intern</h2>
            </div>
          </div>
        </div>
      </div>
      <!--
      <kinesis-container style="top: 700px; right: 400px;">
        <kinesis-element type="depth" :strength="15">
          <div class="triangle1"/>
          <div class="triangle2"/>
        </kinesis-element>
      </kinesis-container>
      <kinesis-container style="bottom: 250px; left: 400px;">
        <kinesis-element type="depth" :strength="15">
          <div class="triangle3"/>
          <div class="triangle4"/>
        </kinesis-element>
      </kinesis-container>
      -->
      
      <!--LOCKHEED MARTIN-->
      <div style="bottom: 500px;" class="glass">
        <div class="glass-inner">
          <div class="glass-front">
            <img style="top: 100px;" alt="Lockheed" src="../images/lockheed.png" width="500" height="121" />
          </div>
          <div class="glass-back">
            <div class="content">
              <h2 style="top: 240px; color:black;">Lockheed Martin</h2>
              <h2 style="top: 240px; color:black;">Software Engineering Intern</h2>
            </div>
          </div>
        </div>
      </div>
      <!--
      <kinesis-container style="top: 1270px; right: 400px;">
        <kinesis-element type="depth" :strength="15">
          <div class="triangle1"/>
          <div class="triangle3"/>
        </kinesis-element>
      </kinesis-container>
      <kinesis-container style="top: 300px; left: 400px;">
        <kinesis-element type="depth" :strength="15">
          <div class="triangle2"/>
          <div class="triangle4"/>
        </kinesis-element>
      </kinesis-container>
      -->
      
      <!--NASA-->
      <div style="bottom: 300px" class="glass">
        <div class="glass-inner">
          <div class="glass-front">
            <img style="top: 100px;" alt="NASA" src="../images/nasa.png" width="400" height="200" />
            </div>
          <div class="glass-back">
            <div class="content">
              <h2 style="top: 240px; color: black;">NASA</h2>
              <h2 style="top: 240px; color: black;">Research Intern</h2>
            </div>
          </div>
        </div>
      </div>
      <!--
      <kinesis-container>
        <kinesis-element :strength="50">
          <img style="top: 1100px; width: 140%; right: 200px; opacity: 0.7;" alt="stars" src="../images/stars.png" height="2300" />
        </kinesis-element>
      </kinesis-container>
          <img style="bottom: 700px; right: 250px;" alt="astronaut" src="../images/astronaut.png" width="50" height="100" />
          <img style="bottom: 800px; left: 350px;" alt="moon" src="../images/moon.png" width="125" height="125" />
      <div style="bottom: 800px; right: 450px;">
          <div class="triangle2"/>
      </div>
      <div style="bottom: 600px; right: 450px;">
          <div class="triangle4"/>
      </div>
      <div style="bottom: 1400px; left: 500px;">
          <div class="triangle1"/>
          <div class="triangle3"/>
      </div>
      -->
    </main>
  </template>
  
  <style scoped>
  .glass {
    min-height: 80vh;
    width: 60%;
    background-color: transparent;
    border-radius: 2rem;
    backdrop-filter: blur(2rem);
    perspective: 1000px;
  }

  .glass-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
  }

  .glass:hover .glass-inner {
    transform: rotateY(180deg);
  }
  .glass-front, .glass-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
  }
  .glass-front {
    min-height: 80vh;
    width: 100%;
    background: linear-gradient(
      to right bottom,
      rgba(255, 255, 255, 0.7),
      rgba(255, 255, 255, 0.3)
    );
    border-radius: 2rem;
    backdrop-filter: blur(2rem);
  }
  .glass-back {
    min-height: 80vh;
    width: 100%;
    background: linear-gradient(
      to right bottom,
      rgba(255, 255, 255, 0.7),
      rgba(255, 255, 255, 0.3)
    );
    border-radius: 2rem;
    backdrop-filter: blur(2rem);
    transform: rotateY(180deg);
  }

  .triangle1,
  .triangle2 {
    background: white;
    background: linear-gradient(
      to right bottom,
      rgba(255, 255, 255, 0.8),
      rgba(255, 255, 255, 0.3)
    );
    height: 10;
    width: 0;
    border-top: 18rem solid transparent;
    border-bottom: 18rem solid transparent;
    border-left: 18rem solid;
    display: flex;
    position: relative;
  }

  .triangle3,
  .triangle4 {
    background: white;
    background: linear-gradient(
      to right bottom,
      rgba(255, 255, 255, 0.8),
      rgba(255, 255, 255, 0.3)
    );
    height: 0;
    width: 0;
    border-top: 10rem solid transparent;
    border-bottom: 10rem solid transparent;
    border-left: 10rem solid;
    display: flex;
    position: relative;
  }


  .triangle1 {
    bottom: 10%;
    right: 15%;
    transform: rotate(32deg);
  }
  .triangle2 {
    top: 20%;
    right: 12%;
    transform: rotate(193deg);
  }

  .triangle3 {
    bottom: 25%;
    left: 16%;
    transform: rotate(64deg);
  }
  .triangle4 {
    bottom: 25%;
    left: 20%;
    transform: rotate(220deg);
  }

  .background {
    top: 60%;
    position: absolute;
    height: 150%;
    width: 142.1%;
    left: 0.01rem;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    background: linear-gradient(to right top, rgb(6, 87, 174), rgb(124, 170, 220));
    border-radius: 35px;
  }

  h1 {
    font-weight: 300;
    font-size: 3.0rem;
    text-align: center;
    color: black;
    bottom: 850px;
  }

  h2 {
    font-weight: 200;
    font-size: 2.0rem;
    text-align: center;
  }
  .content {
    display: flex;
    flex-direction: column;
  }
  </style>
  <script>
      export default 
      {
          name: "Experience"
      };
  </script>
  