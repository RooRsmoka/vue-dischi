<template>
    <div class="app-container">
        <div class="albums-container container">
            <album-card 
            v-for="(album, index) in albums" 
            :key="index"
            :album="album"
            />
        </div>
    </div>
</template>

<script>
import AlbumCard from './AlbumCard.vue'
export default {
    components: {
        AlbumCard
    },
    props: {
        albums: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
.app-container {
    background-color: $primary-color;

    .albums-container {
        display: flex;
        flex-wrap: wrap;
    }
}
</style>