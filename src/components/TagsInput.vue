<template>
    <div v-for="(tag, index) in tags">{{ index + ' : ' + tag }}</div>
    <hr>
    {{ newTag }}
    <input type="text" v-model="newTag" @keydown.enter="tags.push(newTag)" @keydown.tab.prevent="tags.push(newTag)" />
    <!-- <button @click="tags.push(newTag)">OK</button> -->
</template>

<script>

export default {
    data: () => ({
        tags: ["vue", "react", "angular"],
        newTag: "preact "
    }),
};


</script>