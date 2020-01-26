<template>
    <div class="flex-container">
        <div class="hero-text">
            <h2 class="heroh2"> More than Just <br>
            shorter links
            </h2>

            <p>Build Your brand's recognition and get detailed <br>
            insights on how links are performing
            </p>
            <button class="btn btn-s  login-btn mx-2" >Get Started</button>
        </div>
        <div class="heroimg">
            <img src="../../../public/illustration-working.svg">

        </div>


    </div>
</template>

<style scoped>
img{
    width:50vw;
    height: 60vh; 
 
}
.heroimg{
     margin-top: 20px;
    

}
.btn-s{
        background: hsl(180, 66%, 49%);
        color: white;
        border-radius: 30px;
        width: 10vw;
        /* margin-right: 30px; */
        text-align: center;
    }
    .flex-container{
        display: flex;
        justify-content: space-between;
        
    }
    .hero-text{
        text-align: center;
        /* flex-flow: row; */
        flex-wrap: wrap;
        flex-direction: row;
        text-align: left;
        margin-left: 80px;
        margin-top:70px;
        
       
    }
    .heroh2 {
        
        font:700;
        font-weight:bolder;
        text-align: left;
         font-size: 50px
    }
</style>