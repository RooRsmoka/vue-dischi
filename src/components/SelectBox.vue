<template>
    <div class="select-box">
        <select v-model="selectedGenre" @change="$emit('search', selectedGenre)">
            <option value="all">All</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
            <option value="pop">Pop</option>
            <option value="rock">Rock</option>
        </select>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selectedGenre: 'all',
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';
.select-box {
    background-color: $primary-color;
    display: flex;
    justify-content: center;
    padding: 15px 0;
}
</style>