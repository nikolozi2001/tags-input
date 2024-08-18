<template>
    <div v-for="(tag, index) in tags">{{ index + " : " + tag }}
        <a href="#" @click.prevent="removeTag(index)">&times;</a>
    </div>
    <hr />
    {{ newTag }}
    <input type="text" v-model="newTag" @keydown.enter="addNewTag" @keydown.delete="removeLastTag"
        @keydown.tab.prevent="addNewTag" />
</template>

<script>
export default {
    data: () => ({
        tags: ["vue", "react", "angular"],
        newTag: "preact ",
    }),

    methods: {
        addNewTag() {
            if (this.newTag) {
                this.tags.push(this.newTag.trim());
                this.newTag = "";
            }
        },
        removeTag(index) {
            this.tags.splice(index, 1);

        },
        removeLastTag() {
            if (this.newTag.length === 0) {
                this.removeTag(this.tags.length - 1);
            }
        }
    },
};
</script>
