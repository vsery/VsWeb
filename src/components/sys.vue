<template>
    <div class="sys">
        <div class="list-group">
            <a href="JavaScript:;" @click="goTop" class="list-group-item list-group-item-success"><i class="fa fa-fw fa-home"></i></a>
            <a href="JavaScript:;" @click="goFooter" class="list-group-item list-group-item-info"><i class="fa fa-fw fa-wordpress"></i></a>
            <a href="JavaScript:;" class="list-group-item list-group-item-warning"><i class="fa fa-fw fa-music"></i></a>
            <a href="JavaScript:;" class="list-group-item list-group-item-danger"><i class="fa fa-fw fa-bars"></i></a>
        </div>
    </div>
</template>
<script>
export default {
    name: 'sys',
    data() {
        return {}
    },
    methods: {
        goTop() {
            $('body,html').animate({
                scrollTop: 0
            }, 1000);
        },
        goFooter() {
            $('body').scrollspy({ target: '#navbar-example' });
        }
    }
}

</script>
<style>
.sys {
    position: fixed;
    right: 10px;
    bottom: 10px;
}

</style>
