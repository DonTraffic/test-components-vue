<template>
    <div>
        <v-list-item class="listItem">
            <v-list-item-content class="listItem-content">
                <v-list-item-title class="listItem-title">{{info.title}}</v-list-item-title>
                <ListTags :info='info.data'/>
            </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
    </div>
</template>

<script>
import ListTags from "./ListTags.vue";

export default {
    name: 'ListItem',
    props: {
        info: Object
    },
    components: {ListTags}
}
</script>

<style lang="scss">
.listItem{
    &-title{
        font-size: 25px;
        @media screen and (max-width: 500px) {
            font-size: 20px;
        }
    }
}
</style>