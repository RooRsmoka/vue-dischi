<template>
    <div class="album-card">
        <div class="album-cover">
            <img :src="album.poster" >
        </div>
        <h4>{{album.title}}</h4>
        <div class="info">
            <p>{{album.author}}</p>
            <p>{{album.year}}</p>
        </div>
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
.album-card {
    background-color: #2E3A46;
    padding: 20px;
    margin: 10px 15px;
    width: calc(20% - 30px);

    .album-cover {

        img {
            width: 100%;
        }
    }

    h4 {
        padding: 20px 0;
        color: #fff;
        font-size: 18px;
        text-align: center;
        text-transform: uppercase;
    }

    .info {
        text-align: center;
        color: #808080;
        padding: 20px 0;
    }
}
</style>