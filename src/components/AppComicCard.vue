<script>
export default {
    props: {
        comics: Object,
        title: String,
    }
}
</script>

<template lang="">

    <div class="card">
        <div class="card-image">
            <img :src="comics.thumb" alt="comic-image"> 
        </div>
        <div class="card-name">
            {{comics.series}}
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .card{
        width: calc(15% - 10px);
        text-align: center;
        margin: 5px;
        padding: 1rem;
        color: white;

        img{
            width: 100%;
        }
    }
    
</style>