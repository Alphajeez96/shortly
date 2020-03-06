<template>
  <div class="flex-container">
    <div class="hero-text">
      <h2 class="heroh2">
        More than Just
        <br />shorter links
      </h2>

      <p class="herop">
        Build Your brand's recognition and get detailed
        <br />insights on how links are performing
      </p>
      <button class="btn btn-s login-btn mx-2">Get Started</button>
    </div>
    <div class="heroimg">
      <img src="../../../public/illustration-working.svg" />
    </div>
  </div>
</template>

<style scoped>
.herop{
  font-size: 16px
}
img {
  width: 50vw;
  height: 60vh;
}
.heroimg {
  margin-top: 20px;
}
.btn-s {
  background: hsl(180, 66%, 49%);
  color: white;
  border-radius: 30px;
  width: 10vw;
  /* margin-right: 30px; */
  text-align: center;
  -webkit-animation: glowing 1500ms infinite;
  -moz-animation: glowing 1500ms infinite;
  -o-animation: glowing 1500ms infinite;
  animation: glowing 1500ms infinite;
}
@-webkit-keyframes glowing {
  0% {
    background-color: hsl(180, 66%, 49%);
    -webkit-box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
  50% {
    background-color: #ff0000;
    -webkit-box-shadow: 0 0 40px #ff0000;
  }
  100% {
    background-color: hsl(180, 66%, 49%);
    -webkit-box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
}

@-moz-keyframes glowing {
  0% {
    background-color: hsl(180, 66%, 49%);
    -moz-box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
  50% {
    background-color: hsl(180, 35%, 27%);
    -moz-box-shadow: 0 0 40px hsl(180, 35%, 27%);
  }
  100% {
    background-color: hsl(180, 66%, 49%);
    -moz-box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
}

@-o-keyframes glowing {
  0% {
    background-color: hsl(180, 66%, 49%);
    box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
  50% {
    background-color: hsl(180, 35%, 27%);
    box-shadow: 0 0 40px hsl(180, 35%, 27%);
  }
  100% {
    background-color: hsl(180, 66%, 49%);
    box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
}

@keyframes glowing {
  0% {
    background-color: hsl(180, 66%, 49%);
    box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
  50% {
    background-color: hsl(180, 35%, 27%);
    box-shadow: 0 0 40px hsl(180, 35%, 27%);
  }
  100% {
    background-color: hsl(180, 66%, 49%);
    box-shadow: 0 0 3px hsl(180, 66%, 49%);
  }
}
.flex-container {
  display: flex;
  justify-content: space-between;
}
.hero-text {
  text-align: center;
  /* flex-flow: row; */
  flex-wrap: wrap;
  flex-direction: row;
  text-align: left;
  margin-left: 120px;
  margin-top: 70px;
}
.heroh2 {
  font: 700;
  font-weight: bolder;
  text-align: left;
  font-size: 50px;
}

@media screen and (max-width: 700px) {
   img{
     display:none;
   }
   p{

     font-size: 20px;
     font-weight: lighter;
     text-align: left !important;
     padding-left: -10px !important;
     width: 250px;
     position: relative;
     right:30px !important;
   }
   h2{
     font-size:40px !important;
     text-align: left !important;
     position: relative;
     right:30px !important;
     
   }
   button{
     width: 200px !important;
     height: 55px !important;
     position: relative;
    right: 30px;

   }
    
}


</style>