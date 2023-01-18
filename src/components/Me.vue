<template>
  <main class="background">
    <h1>
      About Me
    </h1>
    <div class="row">
      <img alt="me" src="../images/me-again.png" width="375" height="500" />
      <img alt="me-three" src="../images/me-photoshop.png" width="215" height="300" />
    </div>
  </main>
</template>

<style scoped>
.background {
  background-color: white;
  height: 100vh;
  top: 225%;
  width: 142.1%;
  left: 0.01rem;
  position: absolute;
  border-radius: 35px;
}

h1 {
  color: black;
  font-weight: 300;
  font-size: 3.0rem;
  text-align: center;
}

.row {
  display: flex;
  flex-direction: row;
  align-items: center;
}
</style>
<script>
    export default 
    {
        name: "Me",
        data() {
            return {
            }
        }
    }
</script>
