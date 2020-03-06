<template>
  <div class="col-12 row foot container-fluid mx-0">
    <div class="col-md-1 mx-auto">
      <h3 class="shortly">Shortly</h3>
    </div>
    <div class="mx-auto row">
      <div class="col-md-3 mx-auto">
        <h6 class="foothead">Features</h6>
        <ul>
          <li>Link Shortening</li>
          <li>Branded Links</li>
          <li>Analytics</li>
        </ul>
      </div>
      <div class="col-md-2 mx-auto">
        <h6 class="foothead">Resources</h6>
        <ul>
          <li>Blog</li>
          <li>Developers</li>
          <li>Support</li>
        </ul>
      </div>
      <div class="col-md-2 mx-auto">
        <h6 class="foothead">Company</h6>
        <ul>
          <li>About</li>
          <li>Our Team</li>
          <li>Careers</li>
          <li>Contact</li>
        </ul>
      </div>
    </div>
    <div class="fi row">
      <div>
        <img class="mx-2 footimg" src="../../public/icon-facebook.svg" />
      </div>
      <div>
        <img class="mx-2 footimg" src="../../public/icon-twitter.svg" />
      </div>
      <div>
        <img class="mx-2 footimg" src="../../public/icon-pinterest.svg" />
      </div>
      <div>
        <img class="mx-2 footimg" src="../../public/icon-instagram.svg" />
      </div>
    </div>
  </div>
</template>

<style scoped>
img {
  height: 2vh;
  width: 1vw;
  cursor: pointer;
}
li {
  list-style-type: none;
  cursor: pointer;
  text-align: left;
  font: small-caption;
  color: hsl(0, 0%, 75%);
  font-weight: 500;
  line-height: 22px;
}
.foot {
  background-color: hsl(260, 8%, 14%);
  /* width: 100%; */
  min-height: 30vh;
  color: #ffffff;
  padding: 80px;
}
.shortly {
  font-weight: bolder;
  color: #fff;
  cursor: pointer;
  /* margin-right: 2000px; */
}
.foothead {
  text-align: left;
  margin-left: 40px;
  font-weight: 400;
  width: 140px;
}

@media screen and (max-width: 700px) {
  .shortly {
    margin-right: 15px !important;
  }
  .foothead {
    margin-top: 10px;
  }
  .footimg {
    width: 4vw;
  }
  .fi {
    margin-left: 45px;
  }
}
</style>