<template>
    <div>
        <img :src="album.poster">
        <h4>{{album.title}}</h4>
        <p>{{album.author}}</p>
        <p>{{album.year}}</p>
    </div>
</template>

<script>
export default {
    props: {
        album: Object
    }
}
</script>

<style lang="scss" scoped>

</style>