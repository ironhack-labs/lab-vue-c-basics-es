<script setup>

</script>




<template>
    <footer class="footer">
        <div>
            <h3>Contact Us!</h3>
            <p>C/falsa, 123, Barcelona</p>
        </div>
        <div class="footer-container">
         <ul class="footer-list">
             <li><a href="#">Learn More</a></li>
             <li><a href="#">Service</a></li>
             <li><a href="#">Contact</a></li>
        </ul>
     </div>
    </footer>
</template>

<style scoped>

.footer{
    background-color: lightgreen;
    display: flex;
    justify-content: space-between;
    width: 100vw;
}
.footer-list{
    display: flex;
    justify-content: space-evenly;
    list-style: none;
}
.footer-container{
    width: 50%;
}
</style>