<template>
    <nav class="navbar navbar-default">
        <div class="container">
            <div class="navbar-header">
                <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#index_navigation" aria-expanded="false">
                    <span class="sr-only">Toggle navigation</span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" :href="logo.pic">{{logo.type=='string'?logo.text:logo.pic}}</a>
            </div>
            <div class="collapse navbar-collapse" id="index_navigation">
                <ul class="nav navbar-nav">
                    <li :class="m.children.length!=0?'dropdown':''" v-for="m in menus">
                        <template v-if="m.children.length!=0">
                            <a href="javascript:;" :title="m.desc" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"><i :class="['fa fa-fw fa-']+[m.icon]"></i> {{m.text}} <span class="caret"></span> </a>
                            <ul class="dropdown-menu">
                                <li v-for="c in m.children">
                                    <a :href="c.path" :title="c.desc"><i :class="['fa fa-fw fa-']+[c.icon]"></i> {{c.text}} </a>
                                </li>
                            </ul>
                        </template>
                        <template v-else>
                            <a href="javascript:;" :title="m.desc"><i :class="['fa fa-fw fa-']+[m.icon]"></i>{{m.text}} </a>
                        </template>
                    </li>
                </ul>
                <ul class="nav navbar-nav navbar-right">
                    <li><a href="javascript:;">help</a></li>
                    <li class="dropdown">
                        <a href="javascript:;" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"> {{user.nickname}} - {{user.grade}} <span class="caret"></span></a>
                        <ul class="dropdown-menu">
                            <li :class="s.children.length!=0?'dropdown':''" v-for="s in sys">
                                <template v-if="s.children.length!=0">
                                    <a href="javascript:;" :title="s.desc" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"><i :class="['fa fa-fw fa-']+[s.icon]"></i> {{s.text}} <span class="caret"></span> </a>
                                    <ul class="dropdown-menu">
                                        <li v-for="c in s.children">
                                            <a :href="c.path" :title="c.desc"><i :class="['fa fa-fw fa-']+[c.icon]"></i> {{c.text}} </a>
                                        </li>
                                    </ul>
                                </template>
                                <template>
                                    <a :href="s.path" :title="s.desc">{{s.text}}</a>
                                </template>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
    name: 'hello',
    data() {
        return {
            logo: {
                type: 'string',
                text: 'Vsery',
                pic: ''
            },
            menus: [{
                text: 'Index',
                desc: '首页',
                icon: 'home',
                path: '#/index',
                children: []
            }, {
                text: 'Blog',
                desc: '博客',
                icon: 'blog',
                path: '',
                children: [{
                    text: 'Front end Engineer',
                    desc: '前端程序员',
                    icon: 'home',
                    path: '#/blog/f2e',
                }, {
                    text: 'Back end Engineer',
                    desc: '后端程序员',
                    icon: 'home',
                    path: '#/blog/b2e',
                }, {
                    text: 'Soul Soother',
                    desc: '心灵鸡汤',
                    icon: 'home',
                    path: '#/blog/journal',
                }, {
                    text: 'Inspiration Design',
                    desc: '灵感设计',
                    icon: 'home',
                    path: '#/blog/id',
                }]
            }, {
                text: 'Books',
                desc: '书籍',
                icon: 'book',
                path: '',
                children: [{
                    text: 'jQuery',
                    desc: 'jQuery APi & DOC',
                    icon: 'book',
                    path: '#/books/jquery',
                }, {
                    text: 'Bootstrap',
                    desc: 'Bootstrap API & DOC',
                    icon: 'book',
                    path: '#/books/bootstrap',
                }, {
                    text: 'Vue',
                    desc: 'Vue API & DOC',
                    icon: 'book',
                    path: '#/books/vue',
                }, {
                    text: 'Angular',
                    desc: 'Angular API & DOC',
                    icon: 'book',
                    path: '#/books/angular',
                }, {
                    text: 'Node',
                    desc: 'Node API & DOC',
                    icon: 'book',
                    path: '#/books/Node',
                }, {
                    text: 'GIt',
                    desc: 'GIt API & DOC',
                    icon: 'book',
                    path: '#/books/GIt',
                }, {
                    text: 'Gulp',
                    desc: 'Gulp API & DOC',
                    icon: 'book',
                    path: '#/books/Gulp',
                }, {
                    text: 'W3C',
                    desc: 'W3C API & DOC',
                    icon: 'book',
                    path: '#/books/W3C',
                }, {
                    text: 'Browser',
                    desc: 'Browser API & DOC',
                    icon: 'book',
                    path: '#/books/Browser',
                }, {
                    text: 'jQueryMoblie',
                    desc: 'jQueryMoblie API & DOC',
                    icon: 'book',
                    path: '#/books/jQueryMoblie',
                }]
            }, {
                text: 'work',
                desc: '项目/工作/产品',
                icon: 'work',
                path: '',
                children: [{
                    text: 'MAll',
                    desc: '三件分销商品',
                    icon: 'home',
                    path: '#/work/f2e',
                }, {
                    text: 'Admin',
                    desc: '后台模板',
                    icon: 'home',
                    path: '#/work/b2e',
                }]
            }],
            sys: [{
                text: '今日签到',
                desc: '签到领几份',
                icon: 'zan',
                path: '',
                children: []
            }, {
                text: '个人设置',
                desc: '个人设置',
                icon: 'user',
                path: '',
                children: []
            }, {
                text: '发布需求',
                desc: '发布需求',
                icon: 'on',
                path: '',
                children: []
            }, {
                text: '退出',
                desc: '退出',
                icon: 'game over',
                path: '',
                children: []
            }],
            user: {
                nickname: 'vsery',
                grade: '管理员',
                star: 88775,
                wateing: 5576855,
                account: 'vsery',
                email: 'vsery@163.com',
                password: '!@#ASDqweZXC',
                token: 'bD3@hD4@gC2|rB4?cJ1#lB1`bB7@qC4{fI2;bD7~tE2?dB2%nU2$fD6ebN1@',
                avatar: 'static\\images\\header\\image_haeder.jpg'
            }
        }
    }
}

</script>
