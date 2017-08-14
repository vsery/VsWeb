<template>
    <div class="container-fluid jumbotron" id="searchBox">
        <div class="row">
            <div class="col-lg-8 col-sm-12 col-xs-12 col-md-8 col-lg-offset-2 col-md-offset-2">
                <!-- <h2>Vsery</h2> -->
                <p>Vsery 位您 <span class="package-amount">共收录了 <strong>3107</strong> 篇本章</span></p>
                <div class="search-wraper col-lg-10 col-sm-12 col-xs-12 col-md-10 col-lg-offset-1 col-md-offset-1 text-center" role="search">
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
    name: 'searchBox',
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
<style>
    #searchBox {
        background-color: rgba(255,255,255,.25);
        border-radius: 10px;
    }
    #searchBox p {
        color: #000;
    }
    #searchBox strong {
        color: rgba(255,175,175,.7);
    }
</style>
