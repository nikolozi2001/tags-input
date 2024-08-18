<template>
    <div v-for="(tag, index) in tags">{{ index + ' : ' + tag }}</div>
    <input type="text" :value="newTag" @keydown.enter="tags.push($event.target.value)"
        @keydown.tab.prevent="tags.push($event.target.value)" />
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