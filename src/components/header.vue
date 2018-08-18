<template>
    <header class="">
        <h1>查理 <a class="s-btn" @click="showIndex">主页</a><a class="t-btn" @click="showTools"><span></span></a></h1>
    </header>
</template>

<script>
    export default {
        props:['isShow'],
        methods: {
            showTools(){
                this.$emit('tools');
            },
            showIndex(){
                this.$emit('tools');
            }
        }
    }

</script>

<style lang="scss" rel="stylesheet/scss">
    header{
        width:100%;
        height:70px;
        background:#eee;
        h1{
            position: relative;
            width:100%;
            max-width:800px;
            margin:0 auto;
            line-height: 70px;
            color:#24292e;
            a.s-btn{
                font-size: large;
                float: right;
                margin-right: 45px;
            }
            a.t-btn{
                position: absolute;
                right:10px;
                top:22px;
                width:30px;
                height:26px;
                cursor: pointer;
            }
            span,span:before,span:after{
                position: absolute;
                left:0;
                width:30px;
                height:4px;
                content: '';
                background: #fff;
            }
            span{
                top:11px;
                &:before{
                    top:0;
                    transform: translateY(-7px);
                    transition: all .3s;
                }
                &:after{
                    transform: translateY(7px);
                    transition: all .3s;
                }
            }
        }
    }
</style>
