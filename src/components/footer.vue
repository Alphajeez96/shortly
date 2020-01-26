<template>
    <div class="col-12 row foot container-fluid mx-0 ">

        <div class="col-md-1 mx-5">
            <h3 class="shortly ">Shortly</h3>
        </div>
        <div class="mx-5 row">
        <div class="col-md- mx-4">
            <h6 class="foothead">Features</h6>
            <ul >
                <li>Link Shortening</li>
                <li>Branded Links</li>
                <li>Analytics</li>
            </ul>
        </div>
        <div class="col-md-3 mx-4">
            <h6 class="foothead">Resources</h6>
            <ul>
                <li>Blog</li>
                <li>Developers</li>
                <li>Support</li>
            </ul>
        </div>
        <div class="col-md- mx-4">
            <h6 class="foothead">Company</h6>
            <ul>
                <li>About</li>
                <li>Our Team</li>
                <li>Careers</li>
                <li>Contact</li>
            </ul>
        </div>
        </div>
        <div>
            <img class="mx-2" src="../../public/icon-facebook.svg">
        </div>
        <div>
             <img class="mx-2" src="../../public/icon-twitter.svg">
        </div>
        <div>
             <img class="mx-2" src="../../public/icon-pinterest.svg">
        </div>
        <div>
             <img class="mx-2" src="../../public/icon-instagram.svg">
        </div>

    </div>
</template>

<style scoped>
    img{
        height: 2vh;
        width: 1vw;
        cursor:pointer;
    }
    li {
        list-style-type: none;
        cursor: pointer;
        text-align: left;
        font:small-caption;
        color: hsl(0, 0%, 75%);
        line-height: 22px;
        
    }
    .foot{
        background-color:  hsl(260, 8%, 14%);
        width: 100%;
        min-height: 30vh;
        color:#ffffff;
        padding: 80px
    }
    .shortly{
        font-weight: bolder;
        color:#fff;
        cursor: pointer;
    }
    .foothead{
        text-align: left;
        margin-left:40px;
        font-weight: 400;
        
    }
</style>