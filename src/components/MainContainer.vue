<template>
    <div>
        <album-card 
        v-for="album in albums.response" 
        :key="album.index"
        :album="album"
        />
    </div>
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

</style>