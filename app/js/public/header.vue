<template lang="html">
    <div :class="$style.header">
        <span :class="$style.left">
            <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
        </span>
        <btn :class="$style.btnDownload">
            APP下载
        </btn>
    </div>
</template>
<script>
    import btn from '../core/btn.vue'
    export default {
        components: {
            btn
        }
    }
</script>
<style lang="scss" module>
    .header{
        z-index:100;
        position:fixed;
        left:0;
        top:0;
        right:0;
        height:100px;
        font-size:32px;
        background:#fff url(https://m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
        background-size:auto 50%;
        line-height:100px;
        color: #666;
        .left{
            height:30px;
            margin:17px 0 0 18px;
            line-height:30px;
            font-size:28px;
        }
        .btnDownload{
            float:right;
            height:56px;
            min-width:120px;
            margin:28px 24px 0 0;
            padding:0;
            line-height:56px;
            font-size:24px;
            border-width:0;
            color: #fff;
            border-radius:4px;

        }
    }
</style>