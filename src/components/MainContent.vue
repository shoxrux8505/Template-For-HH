<template>
    <div class="main-content">
        <SaidBar />
        <Carusel/>
    </div>
</template>
<script>

import SaidBar from './SaidBar.vue';
import Carusel from './Carusel.vue';
export default {
    name: 'MainContent',
    components: {
        SaidBar,
        Carusel
    }
}
</script>
<style lang="scss" scoped>
.main-content {
    display: flex;
    gap: 20px;
    padding: 20px;
}
</style>