<template>
    <div class="base-layout">
        <BaseHeader/>
        <BaseNav/>
        <BaseAside/>
        <main><slot name="main"></slot></main>
        <BaseFooter/>
    </div>
    
</template>
<script setup lang="ts">
import BaseHeader from './BaseHeader.vue';
import BaseNav from './BaseNav.vue';
import BaseAside from './BaseAside.vue';
import BaseFooter from './BaseFooter.vue';
</script>
<style lang="scss" scoped>
.base-layout{
    display: grid;
    grid:'header header ' 100px
         'nav nav '          50px
         'aside main '     calc(100vh - 250px)
         'footer footer ' 100px/
         260px calc(100% - 260px)

}
main{
    grid-area: main;
}
</style>
