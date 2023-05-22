<script>
export default {

}
</script>


<template>
  <nav>
    <div class="container">
      <div class="form-floating">
  <select class="form-select" id="floatingSelect" aria-label="Floating label select example">
    <option selected>Alien</option>
    <option value="1">Equip</option>
    <option value="2">Insects</option>
    <option value="3">Beasts</option>
  </select>
</div>
    </div>
  </nav>
</template>



<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

nav{
    height: 100px;
    background-color: rgba(212,143,56,255);
    .container{
        height: 100%;
        width: 80%;
        @include flex-margin-auto;
        align-items: center;
    }

}

select{
    width: 200px;
    height: 50px;
    font-size: 1.5em;
    padding: .2em;
    border-radius: 10px;
}

</style>