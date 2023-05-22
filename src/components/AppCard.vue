<script>

export default {
    props: {
        CharacterData: Object,
    }

}
</script>


<template>
  <div class="card">
    <img :src="CharacterData.card_images[0].image_url" :alt="CharacterData.name">
    <h4>{{ CharacterData.name }}</h4>
    <div class="species">{{ CharacterData.race }} </div>
  </div>
</template>



<style lang="scss" scoped>

.card{
    width: 200px;
    height: 400px;
    text-align: center;
    background-color: rgba(212,143,56,255);

    img{
        width: 100%;
    }

    h4{
        color: white;
    }


}

</style>