<template>
  <div>
    <div class="short">
      <div class="flex-container">
        <div class="t">
          <input v-model="url" type="text" placeholder="    shorten a link here..." />
          <button v-on:click="shortenlink" class="shortbtn">shorten it!</button>

          <div v-bind:class="{ active: isActive }" class="shorts card w-100">
            <div class="ml-2 card-textd flex-container">
              <p id="myInput" class="card-text">{{shortenedurl}}</p>

              <button
                type="button"
                @click="showAlert"
                v-clipboard:copy="shortenedurl"
                v-clipboard:success="onCopy"
                v-clipboard:error="onError"
                class="copy btn btn-outline-primary"
              >Copy Link</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="stats">
      <div class="advm">
        <h3 class="mt-5 adv">Advanced Statistics</h3>
        <p class="pb-5">
          Track how your links are performing across the web with
          <br />our advanced statistics board.
        </p>
      </div>

      <div class="flex-containe mt-5">
        <div class="box brand mx- my-">
          <div class="vector">
            <img src="../../../public/icon-brand-recognition.svg" class="vetor pt-2" alt />
          </div>
          <h5 class="boxheader">Brand Recognition</h5>
          <p class="ptext">
            Boost your brand recognition with
            <br />each click. Generic links dont mean a
            <br />thing.Branded links help instill
            <br />confidence in your content.
          </p>
        </div>
        <div class="hrdiv">
          <hr />
        </div>

        <div class="box mx- my- detailed">
          <div class="vector">
            <img src="../../../public/icon-detailed-records.svg" class="vetor pt-2 mt-1" alt />
          </div>
          <h5 class="boxheader">Detailed Records</h5>
          <p class="ptext">
            Gain insights into who is clicking your
            <br />links. Knowing when and where
            <br />people engage with your content
            <br />helps inform better decisions.
          </p>
        </div>
        <div class="hrdiv">
          <hr />
        </div>
        <div class="box mx- my- fully">
          <div class="vector">
            <img src="../../../public/icon-fully-customizable.svg" class="vetor pt-2 mt-1" alt />
          </div>
          <h5 class="boxheader">Fully Customizable</h5>
          <p class="ptext">
            Improve brand awareness and
            <br />content discoverability through
            <br />Customizable links,Supercharging
            <br />audience engagement.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src

const axios = require("axios");
export default {
  name: "home",
  data() {
    return {
      isActive: true,
      url: "",
      shortenedurl: null,
      message: ""
    };
  },

  computed: {},

  methods: {
    shortenlink: function() {
      this.isActive = false;
      axios
        .post(`https://rel.ink/api/links/`, {
          url: this.url,

          if(url = this.url) {
            alert("Input a valid link");
          }
        })

        .then(response => {
          console.log(response.data);
          this.shortenedurl = "https://rel.ink/" + response.data.hashid;
        })
        .catch(function(error) {
          $swal(error);
        });
    },

    onCopy: function(e) {
      this.message = this.shortenedurl;
    },
    onError: function(e) {
      alert("Failed to copy texts");
    },

    showAlert() {
      this.$swal({
        position: "center",
        icon: "success",
        title: " Link Copied",
        showConfirmButton: true,
        timer: 5000
      });
    }
  }
};
</script>

<style scoped>
.card-text {
  padding: auto;
}
.active {
  display: none;
}
.swal-overlay {
  background-color: rgba(43, 165, 137, 0.45);
}
.copy {
  margin-left: 400px; 
  position: relative;
  bottom: 10px;
}

.card {
  margin-top: 40px;
  height: 6vh;
}
.fully {
  margin: 60px 0px 60px 0px;
  height: 40vh;
}
.detailed {
  margin: 30px 0px 30px 0px;
}
.hrdiv {
  margin-top: 100px;
}
hr {
  border: 10px hsl(180, 66%, 49%);
  height: 6px;
  width: 10px;
  background: hsl(180, 66%, 49%);

  padding-left: 10px;
}
.ptext {
  font-size: 14px;
  text-align: left;
  padding-left: 20px;
  padding-top: 5px;
  line-height: 26px;
}

.cardbtn {
  border: 1px solid #071878 !important;
  width: 173px;
  height: 43px;

  box-sizing: border-box;
  border-radius: 2px;
  margin: 20px 180px 20px 0px;
  justify-content: left;

  font-size: 12px;
}

.vector {
  margin-left: 50px;

  border-radius: 50%;
  background: hsl(260, 8%, 14%);
  width: 50px;
  height: 50px;
  margin-bottom: 20px;

  margin-top: -25px;
}
.vetor {
  width: 2vw;
  height: 5vh;
}
.boxheader {
  font: bolder;
  font-weight: 1000;
  font-size: 14px;
  text-align: left;
  padding-left: 20px;
  padding-top: 15px;
}
.servicediv {
  background: #e5e5e5;
}
.services {
  color: #484848;

  line-height: 55px;
}
.flex-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 20px;
}
.flex-containe {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.box {
  min-width: 20vw;
  max-height: 30vh;
  border: 1px solid #e5e5e5;
  box-shadow: 0px 12px 75px rgba(67, 73, 106, 0.09);
  border-radius: 5px;
  background: white;
}
.adv {
  padding-top: 200px;
  font-weight: 700;
  font: bolder;
}
.stats {
  background: hsl(0, 0%, 75%);
}
.t {
  display: inline-block;
  margin: 0 auto;
  padding: 10px;
}
.short {
  width: 90%;

  height: 15vh;
  background: url("../../../public/bg-shorten-desktop.svg");
  background-size: cover;
  background-position: center;

  background-color: hsl(260, 8%, 14%);

  margin: auto;
  border: 0.1px outset hsl(260, 8%, 14%);
  border-radius: 7px;
  margin-top: 35px;
  position: relative;
  top: 90px;
}

.shorts {
  max-width: 100%;

  height: 8vh;

  background-size: cover;
  background-position: center;

  background-color: white;
  margin: auto;
  border: 0.1px outset hsl(260, 8%, 14%);
  border-radius: 7px;
  margin-top: 35px;
  position: relative;
}

.shortbtn {
  background: hsl(180, 66%, 49%);
}
.flex-container {
  display: flex;
  justify-content: center;
}

input {
  border-radius: 7px;
  width: 40vw;

  height: 8vh;
  border: 0.1px outset hsl(260, 8%, 14%);
  justify-content: space-between;
}
.shortbtn {
  height: 8vh;
  width: 10vw;
  margin-left: 20px;
  border: 0.1px outset hsl(260, 8%, 14%);
  border-radius: 7px;
  color: white;
}
/* @media screen and (max-width: 1030px) {
  input {
    margin: -30px 0px 0px 0px !important;
    position: relative;
    bottom: 10px;
  }
  .shortbtn {
    position: relative;
    bottom: 10px;
    width: 17vw;
  }
} */

@media screen and (max-width: 700px) {
  .copy {
    position: relative;
    bottom: 25px;
    left: 70px;
    font-size: 10px;
    max-width: 70px;
    -moz-text-size-adjust: auto;
  }
  .card-textd {
    width: 2vw !important;
    height: 1vh !important;
    margin-bottom: 40px;
  }
  .stats {
    margin-top: 40px;
  }
  .shortbtn {
    position: relative;
    bottom: 10px;
    width: 17vw;
  }
  div .short {
    position: relative !important;
    top: 130px !important;
    height: 160px !important;
  }
  .shortbtn {
    position: relative !important;
    top: 10px !important;
    right: 10px;
    text-align: center !important;
    width: 200px;
  }
  input {
    position: relative !important;
    top: -3px !important;
    width: 200px;
    text-align: center !important;
  }
  .pb-5,
  .py-5 {
    width: 250px !important;
    text-align: center !important;
    margin-left: 60px;
    font-size: 18px;
  }
  hr {
    margin-top: 150px !important;
    margin-left: -150px;
    height: 60px;
    width: 0px;
    position: relative;
    left: -17px;
    top: 10px;
    text-align: center;
  }
  .vetor {
    width: 6vw;
  }
  .vector {
    position: relative;
    left: 60px;
  }
  .fully {
    position: relative;

    margin-top: 5px;
    width: 80%;
  }
  .detailed {
    position: relative;

    margin-top: 15px;
    width: 80%;
  }
  .brand {
    position: relative;
    bottom: 5px;
    margin-top: 20px;
    width: 80%;
  }
}
</style>