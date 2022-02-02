<template>
    <header>
        <div class="logo">
            <img src="@/assets/spotify-logo.png">
        </div>  
    </header>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
header {
    background-color: $secondary-color;
    height: 60px;
    display: flex;

    .logo {

        img {
            height: 100%;

        }
    }
}
</style>