<template>
    <article class="">
        <Slider :items="items" :cname="$style.slider"></Slider>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider";
export default {
    components: {
        Slider
    },
    data () {
        return {
            options:{
                pagination:true
            },
            items:[
                {
                    src:'https://img12.360buyimg.com/jrpmobile/jfs/t21445/342/2330997341/45152/a58b625c/5b51c68dNc9c51bf2.jpg?width=750&height=320',
                    href:'home',
                    title:'1'
                },
                {
                    src:'https://img12.360buyimg.com/jrpmobile/jfs/t21607/320/2356730454/57260/ab624cbb/5b552930Nb68f5f55.jpg?width=750&height=320',
                    href:'home',
                    title:'2'
                },
                {
                    src:'https://img12.360buyimg.com/jrpmobile/jfs/t22615/58/1124507568/53603/c91e47d7/5b51c664N2ca1ca35.jpg?width=750&height=320',
                    href:'home',
                    title:'3'
                }
            ],
            enters:[
                {
                    title:'优惠券',
                    img:'https://img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
                    href:'1'
                },
                {
                    title:'领福利',
                    img:'https://img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
                    href:'2'
                },
                {
                    title:'抢钢镚',
                    img:'https://img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                    href:'3'
                },
                {
                    title:'白条提额',
                    img:'https://img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                    href:'4'
                }
            ]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
    margin-top: 120px;
    font-size: 0;
    img {
        width: 100%;
    }
}
.list {
    @include list(row);
    background: #fff;
    padding: 20px 0;
    justify-content: space-around;
    .item {
        flex: 1;
        text-align: center;
    }
    a {
         width: 100%;
         float: left;
        text-decoration: none;
        font-size: 0;
        img {
            width: 90px;
            height: 90px;
        }
        h4 {
            font-size: 24px;
            text-align: center;
            display: block;
            color: #666;
            margin-top: 12px;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
        }
    }
}
</style>
