<template>
    <div :class="$style.header">
        <span :class="$style.left">
            <em>注册</em>&nbsp;&nbsp;|&nbsp;&nbsp;<em>登录</em>
        </span>
        <btn :class="$style.btnDownload">APP下载</btn>
    </div>
</template>

<script>
import Btn from '../core/btn'
export default {
    components: {
        Btn
    }
}
</script>

<style lang="scss" module>
.header {
    color: #666;
    height:100px;
    line-height:100px;
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
    background-size: auto 50%;
    z-index: 9;
    .left {
        font-size: 28px;
        line-height: 30px;
        margin: 36px 0 0 18px;
       float: left;
    }
    .btnDownload {
        float: right;
        font-size: 24px;
        border-width: 0;
        line-height: 56px;
        min-width: 120px;
        border-radius: 4px;
        margin: 28px 24px 0 0;
    }
}
</style>
