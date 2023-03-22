<script>

export default{
    data(){
        return{
thisActive:false,
thisHovered:false

        }
    },
    methods: {
    Hovered:function(){
        // alert("Hovered!");
        this.thisHovered=true;
    },
    Unhovered:function(){
        this.thisHovered=false;
    }
    
  }
}
</script>

<template>

<div @mouseover="thisHovered = true" @mouseleave="thisHovered = false" class="buttonContainer">
    
    <div class = "buttonBackground" :class="{ extended: thisActive, extended:thisHovered } ">
    </div>
    <!-- <div class="innerTextCenter"> -->
    <p class =navText>{{thisHovered}}</p>
    <!-- </div> -->
    <!-- <p>Example Text</p> -->
   
</div>

</template>

<style scoped>
.buttonContainer{
    font-size: 20px;
    position: relative;
    /* background-color: #372549; */
    /* color: #fff; */
    width: 190px;
    height: 98px;
    margin: 0px;
    padding: 0px;
}
.buttonBackground{
    /* z-index: 1; */
    width: 0%;
    height: 100%;
    display: flexbox;
    background-color: #DA4469;
    position: absolute;
    top: 0px;
    left: 0px;
    transition: width;
    transition-duration: 300ms;
    
}
.navText{
    /* padding: 14px; */
    position: relative;
    /* background-color: aliceblue; */
    top:20px;
    z-index: 20;
    margin-left: 14px;
    margin-right: 14px;
    margin-top: 0px;
}
.extended{
    width: 100%;
}

</style>