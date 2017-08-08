<template>
    <div class="container-fluid jumbotron">
        <div class="row">
            <div class="col-lg-8 col-sm-12 col-xs-12 col-md-8 col-lg-offset-2 col-md-offset-2">
                <h1>Vsery</h1>
                <p><span class="package-amount">共收录了 <strong>3107</strong> 篇本章</span></p>
                <div class="search-wraper col-lg-6 col-sm-12 col-xs-12 col-md-6 col-lg-offset-3 col-md-offset-3 text-center" role="search">
                    <div class="input-group">
                        <input type="text" class="form-control" placeholder="搜索博文,书籍,作品... 例如：jQuery">
                        <div class="input-group-btn">
                            <button class="btn btn-success" type="button" :onclick="search()">Go!</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'jumbotron',
    data() {
        return {

        }
    },
    methods: {
        /* 搜索文博 */
        search() {}
    }
}

</script>
