<script setup>
import navButton from "./NavButton.vue"
import selectionBox from "./SelectionBox.vue"
import W3 from "./icons/W3Schools.vue"
</script>

<template> 
<div id="navContainer">
    <div id="term">
        <selectionBox/>
        <selectionBox/>
    </div>
    <navButton></navButton>
    <navButton></navButton>
    <navButton></navButton>
    <navButton></navButton>
    <navButton></navButton>
    <div id="navFooter"><p>Can't find what you need?</p>
        <W3/>
    </div>
</div>
</template>

<style scoped>
    #navContainer{
        min-height: calc(100vh - 82px);
        /* position: sticky; */
        width: 190px;
        background-color: #372549;
    }
</style>