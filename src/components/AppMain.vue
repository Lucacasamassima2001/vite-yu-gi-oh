<script>
import { store } from '../store';
import AppCard from './AppCard.vue';

export default {
    
    
    data(){
        
        return{
            store,
        }
    },

    components: {
        AppCard,
    }
}
</script>


<template>
    <main>
        <div class="container">
            <div class="counter">Found {{ store.CharacterList.length }} Cards! This is your Deck! </div>
        <div class="container-cards">
            <AppCard v-for="Character in store.CharacterList" 
            :key="Character.id"
            :CharacterData="Character"
            />
        </div>
        </div>
        
    </main>
  
</template>

<style lang="scss" scoped>

main{
    background-color: rgba(212,143,56,255);
}


.container{
    width: 80%;
    margin-inline: auto;
}

.counter{
    margin-inline: auto;
    background-color: rgba(33,37,41,255);
    color: white;
    height: 50px;
    padding: 1em;
    font-size: 2em;
}

.container-cards{
    border: 50px solid white;
    background-color: white;
    margin-inline: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 1em;
}

</style>