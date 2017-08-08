<template>
    <div id="carousel-example-generic" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
            <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
            <li data-target="#carousel-example-generic" data-slide-to="1"></li>
            <li data-target="#carousel-example-generic" data-slide-to="2"></li>
        </ol>
        <div class="carousel-inner" role="listbox">
            <div class="item active">
                <img src="static/images/360wallpaper (0).jpg" class="img-responsive" alt="...">
                <div class="carousel-caption">
                    <search-view></search-view>
                </div>
            </div>
            <div class="item">
                <img src="static/images/360wallpaper (1).jpg" class="img-responsive" alt="...">
                <div class="carousel-caption">
                </div>
            </div>
            <div class="item">
                <img src="static/images/360wallpaper (2).jpg" class="img-responsive" alt="...">
                <div class="carousel-caption">
                </div>
            </div>
        </div>
        <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
            <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </a>
        <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
            <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
         </a>
    </div>
</template>
<script>
import search from '@/components/search' //面包屑导航
export default {
    name: 'carousel',
    data() {
        return {

        }
    },
    components: {
        "search-view": search
    }
}

</script>
