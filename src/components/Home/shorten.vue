<template>
<div>
    <div class="short">
        <div class="flex-container">
            <div class="t">
                <input v-model='url' type="text" placeholder="    shorten a link here...">
            <button v-on:click='shortenlink' class="shortbtn">shorten it!</button>
            <p>{{shortenedurl}}</p>
            </div>
            
        </div>

    </div>
    <div class="stats">
        <div >
            <h3 class="adv"> Advanced Statistics</h3>
            <p class="pb-5">Track how your links are performing across the web with <br>
                our advanced statistics board.
            </p>
        </div>
    
         <div class="flex-containe mt-5">
             <!-- <img src="../../../public/icon-brand-recognition.svg" class="vetor pt-2"  alt=""> -->
            <div class="box mx- my-">
                <div class="vector"> 
                <img src="../../../public/icon-brand-recognition.svg" class="vetor pt-2"  alt="">
                </div>
                <h5 class="boxheader ">Brand Recognition</h5>
                <p class="ptext">Boost your brand recognition with <br>
                 each click. Generic links dont mean a <br> 
                 thing.Branded links help instill <br>
                 confidence in your content.
                 </p>
                 
    </div>
    <div class="hrdiv">
        <hr>
    </div>
    

      <!-- <div class="flex-container mt-5"> -->
             <!-- <img src="../../../public/icon-brand-recognition.svg" class="vetor pt-2"  alt=""> -->
            <div class="box mx- my- detailed">
                <div class="vector"> 
                <img src="../../../public/icon-detailed-records.svg" class="vetor pt-2 mt-1"  alt="">
                </div>
                <h5 class="boxheader ">Detailed Records</h5>
                <p class="ptext">Gain insights into who is clicking your <br>
                 links. Knowing when and where<br> 
                 people engage with your content <br>
                helps inform better decisions. 
                 </p>
                 
    </div>
     <div class="hrdiv">
        <hr>
    </div>
        <div class="box mx- my- fully">
            
                <div class="vector"> 
                <img src="../../../public/icon-fully-customizable.svg" class="vetor pt-2 mt-1"  alt="">
                </div>
                <h5 class="boxheader ">Fully Customizable</h5>
                <p class="ptext">Improve brand awareness and<br>
                 content discoverability through<br> 
                 Customizable links,Supercharging <br>
                 audience engagement.
                 </p> 
                 
    </div>
    
    </div>
    
    </div>
    

    </div>
   

</template>
<script>
// @ is an alias to /src

const axios = require('axios');
export default {
  name: 'home',
  data(){
      return {
        url: '',
        shortenedurl:  null
      }
    
  },

  computed: {
      
  },
  
  methods: {
      
      shortenlink: function() {
       axios.post(`https://rel.ink/api/links/`, {
        url: this.url,
       if (url = ''){
           alert('Input a valid link')
       }
  })
  .then(response => {
    console.log(response.data);
    this.shortenedurl = 'https://rel.ink/' + response.data.hashid;
  })
  .catch(function (error) {
    console.log(error);
  });

      }
  }
  
}
</script>

<style scoped>
.fully{
    margin: 60px 0px 60px 0px;
}
.detailed{
    margin: 30px 0px 30px 0px;
}
.hrdiv{
    /* padding: 0px 10px 0px 10px */
    margin-top: 100px;
    
}
hr {
    border: 10px hsl(180, 66%, 49%);
    height: 6px;
    width: 10px;    
    background: hsl(180, 66%, 49%);
    /* position: relative; */
    /* float:left; */
    /* margin-top: 30px; */
    /* margin:auto; */
    padding-left: 10px;
    
}
.ptext{
     font-size: 14px;
    text-align:left;
    padding-left:20px;
    padding-top:5px;
    line-height: 26px;
}
.servicebg{
    
}
.cardbtn{
    border:1px solid #071878 !important;
    width: 173px;
height: 43px;
/* border: 1px solid #071878; */
box-sizing: border-box;
border-radius: 2px;
margin:20px 180px 20px 0px;
justify-content: left;
/* margin-right:  100px; */
/* float:left; */
font-size:12px
}
 
.vector{
    margin-left:50px;
    /* justify-content:left; */
    border-radius: 50%;
    background: hsl(260, 8%, 14%);
   width: 50px;
    height: 50px;
    margin-bottom:20px;
     /* padding-top:400px; */
     margin-top:-25px
   
}
.vetor{
    width:2vw;
    height:5vh;
}
    .boxheader{
        /* color: #484848; */
        Font:bolder;
        font-weight: 1000;
        font-size: 14px;
        text-align: left;
        padding-left:20px;
        padding-top: 15px;
        /* line-height:16px; */
        /* margin-bottom: 10px */
    }
    .servicediv{
        background: #E5E5E5;
    }
    .services{
        color: #484848;
        /* text-align: center; */
        line-height: 55px;
    }
    .flex-container{
        display: flex;    
        flex-wrap: wrap;
        justify-content: center;
      
    }
     .flex-containe{
        display: flex;    
        flex-wrap: wrap;
        justify-content: center;
     }
    .box{
       min-width: 24vw;
        max-height: 30vh;
        border: 1px solid #E5E5E5;
        box-shadow: 0px 12px 75px rgba(67, 73, 106, 0.09);
        border-radius: 5px;
        background: white;
        
    }
    .adv{
        padding-top: 150px;
        font-weight: 700;
        font: bolder
    }
    .stats{
        background: hsl(0, 0%, 75%)
    } 
    .t{
         display: inline-block; 
      margin: 0 auto;    
      padding: 40px;
    }
    .short{
        width: 90%;
      
        height: 15vh;
       background: 
    url("../../../public/bg-shorten-desktop.svg");
  background-size: cover;
  background-position: center;
  /* background-repeat: no-repeat; */
  background-color:  hsl(260, 8%, 14%);
  /* align-items: center */
  /* margin: 20px 10px 20px 40px; */
  margin: auto;
  border: 0.1px outset hsl(260, 8%, 14%) ;
  border-radius: 7px;
  margin-top: 35px;
    position: relative;
     top: 60px;
    }

    .shortbtn{
         background: hsl(180, 66%, 49%);
    }
    .flex-container{
        display: flex;
        justify-content:center;
           
    }

    input{
        border-radius: 7px;
        width: 40vw;
        /* width: 50%; */
        height: 6vh;
         border: 0.1px outset hsl(260, 8%, 14%) ;
        justify-content: space-between;
    }
     .shortbtn{
      height: 6vh;
      width:10vw;
      margin-left: 20px;  
      border: 0.1px outset hsl(260, 8%, 14%) ;
      border-radius: 7px;
      color: white;
    }
</style>