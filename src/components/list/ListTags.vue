<template>
    <div class="listTags">
        <div class="listTags-item" v-for="(item, index) of info" :key="item.id">
            <v-icon class="listTags-item-divider" v-if="index">mdi-circle-small</v-icon>
            <v-icon class="listTags-item-icon">{{item.icon}}</v-icon>
            <v-list-item-title class="listTags-item-title">{{item.value}}</v-list-item-title>
        </div>

    </div>
</template>

<script>
export default {
    name: 'ListTags',

    props: {
        info: Array
    },

    mounted() {

        for (let i = 0; i < document.getElementsByClassName('listTags-item').length; i++) {
            this.visibilityElem(document.getElementsByClassName('listTags-item')[i])

            window.addEventListener('resize', () => {
                this.visibilityElem(document.getElementsByClassName('listTags-item')[i])
            }, true);
        }

    },

    methods: {
        visibilityElem(elem) {
            let container = document.getElementsByClassName('listTags')[0]
            
            if (elem.offsetWidth + elem.offsetLeft < container.offsetWidth || elem.offsetWidth + elem.offsetLeft != 0) {
                elem.style.display = 'flex'
            }   
            if (elem.offsetWidth + elem.offsetLeft > container.offsetWidth || elem.offsetWidth + elem.offsetLeft == 0) {
                elem.style.display = 'none'
            }
            
        }

    }

}
</script>

<style lang="scss">
.listTags{
    margin-top: 8px;
    display: flex;

    &-item{
        display: flex;
        align-items: center;
        
        &-icon{
            margin-right: 4px;
        }

    }

}
</style>