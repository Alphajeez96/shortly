<template>
  <div>
    <div class="t">
      <h2 class="boost">Boost Your links today</h2>
      <button class="btn btn-s login-btn mt-2">Get Started</button>
    </div>
  </div>
</template>

<style scoped>
.boost {
  color: #fff;
  font-weight: 700;
}
div {
  height: 30vh;
  background: url("../../../public/bg-boost-desktop.svg");
  background-size: cover;
  background-position: center;

  background-color: hsl(260, 8%, 14%);
  align-items: center;

  margin: auto;
}
.shortbtn {
  background: hsl(180, 66%, 49%);
  border-radius: 20px;
  width: 20px;
}
.t {
  display: inline-block;
  margin: 0 auto;
  padding: 50px;
}
.btn-s {
  background: hsl(180, 66%, 49%);
  color: white;
  border-radius: 30px;
  width: 10vw;

  text-align: center;
}
@media screen and (max-width: 700px) {
  .boost {
    font-size: 25px;
    margin-top: 30px;
  }
  .login-btn {
    width: 40vw;
  }
}
</style>