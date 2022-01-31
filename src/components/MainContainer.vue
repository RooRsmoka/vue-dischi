<template>
    <main>
        <div class="albums-container container">
            <album-card 
            v-for="album in albums.response" 
            :key="album.index"
            :album="album"
            />
        </div>
    </main>
</template>

<script>
import AlbumCard from './AlbumCard.vue'
export default {
    components: {
        AlbumCard
    },
    props: {
        albums: Object
    }
}
</script>

<style lang="scss" scoped>
main {
    background-color: #1E2D3B;
    padding: 60px 0;

    .albums-container {
        display: flex;
        flex-wrap: wrap;
    }
}
</style>