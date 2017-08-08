<template>
    <ol class="breadcrumb">
        <li v-for="p in paths" :class="p.id==3?'active':''">
            <a v-if="p.id!=3" :href="p.path">{{p.title}}</a>
            <span v-else>{{p.title}}</span>
        </li>
    </ol>
</template>
<script>
export default {
    name: 'breadcrumb',
    data() {
        return {
            paths: [{
                id: 1,
                title: 'Home',
                path: './#'
            }, {
                id: 2,
                title: 'Library',
                path: 'javascript:alert("Hello world!");'
            }, {
                id: 3,
                title: 'data',
                path: ''
            }]
        }
    }
}
</script>