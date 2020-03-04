<template>
    <div class="stats">
        <div>
            <h3> Advanced Statistics</h3>
            <p class="track">Track how your links are oerforming across the web with <br>
                our advanced statistics board.
            </p>
        </div>

    </div>
</template>

<style scoped>
    .stats{
        background: hsl(0, 0%, 75%)
    }


    @media screen and (max-width: 700px) {
        
        .pb-5, .py-5{
             position: relative !important; 
            right:20px !important;
            width:10px !important;
            text-align: left !important;   
            color:red !important;    
        }
    }
</style>