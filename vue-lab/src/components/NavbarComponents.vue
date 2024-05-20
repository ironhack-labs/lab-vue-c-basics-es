
<script setup> 


</script>

<template>
<header>
    <nav >
      <div class="nav-bar">
        <h1 class="logo">Vue</h1>
        <ul class = 'list'>
          <li><a href="#">Learn More</a></li>
          <li><a href="#">Service</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
     </div>
  </nav>
  </header>
</template>

<style scoped>

.nav-bar {
 display: flex;
 flex-direction: row;
 padding: 30px;
 justify-content: space-between;
 width: 100vw;
 background-color: lightgreen

}
.list{
    justify-content: space-evenly;
    display: flex;
    width: 50%;
    list-style: none
}
</style>