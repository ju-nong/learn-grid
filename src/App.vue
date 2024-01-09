<template>
    <div class="container">
        <div
            v-for="(item, index) in arr"
            :key="index"
            :style="`--item-value: ${item};`"
        >
            {{ item }}
        </div>
    </div>
</template>

<script setup lang="ts">
const arr = [
    "a-side",
    "b-side",
    "footer",
    "main",
    "footer",
    "header",
    "footer",
    "header",
    "header",
    "footer",
];
</script>

<style scoped>
.container {
    display: grid;
    grid-template-areas:
        "header header header"
        "a-side main b-side"
        ".... .... none"
        "footer footer footer";

    > div {
        padding: 8px;
        border: 1px solid #999;
        border-radius: 0.5rem;

        grid-area: var(--item-value);
    }
}
</style>
