<template>
    <div class="container">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam
            laudantium corporis dolore, magni aliquam sed voluptatum eius quae,
            iure hic beatae, fugiat dolor natus minus ad dignissimos doloribus
            laboriosam incidunt.
        </div>
        <div>5</div>
        <div>6</div>
        <div>7</div>
        <div>8</div>
        <div>9</div>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(20%, auto));
    /* grid-template-rows: repeat(3, minmax(100px, auto)); */
    /* grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); */
    /* grid-template-columns: repeat(3, 1fr); */
    /* grid-template-rows: minmax(100px, auto); */
    /* grid-gap: 20px; */

    > div {
        padding: 8px;
        border: 1px solid #999;
        border-radius: 0.5rem;
    }
}
</style>
