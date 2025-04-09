<script setup lang="ts">

export interface ButtonData {
    text: string,
    link: string,
}

const props = defineProps<{
    href: string,
    name: string,
    description: string,
    image: string,
    buttons?: Array<ButtonData>,
}>();
</script>

<template>
    <a class="card">
        <div>
            <img class="image" :src="props.image" />
        </div>
        <div class="content">
            <h3>{{ props.name }}</h3>
            <p class="desc">{{ props.description }}</p>
            <div class="buttons">
                    <BoldButton v-for="(data, i) of buttons" :key="i" class="button" :text="data.text"
                        :href="data.link" />
                </div>
            <ClientOnly>
                
            </ClientOnly>
        </div>
    </a>
</template>

<style scoped>
.card {
    display: flex;
    width: 45%;
    /* height: 200px; */
    max-width: 450px;
    padding: 25px;
    background-color: rgba(0, 53, 122, 1);
    border-radius: 5px;
    flex-direction: row;

}

/* .card:hover{
        background-color: rgb(0, 80, 184);
    } */

.image {
    width: 200px;
    height: 200px;
    border-radius: 5px;
}

.content {
    color: aliceblue;
    position: relative;
    flex-grow: 1;
    visibility: visible;
    text-align: left;
    padding: 10px;

}

h3{
    margin: 0;
    margin-bottom: 5px;
}

.desc{
    font-size: 80%;
}

.buttons {
    margin-top: 5px;
}

.button {
    margin-right: 5px;
}

@media (max-width: 1000px) {
    .card {
        flex-direction: column;
        width: auto;
    }
}

a {
    text-decoration: none;
}
</style>