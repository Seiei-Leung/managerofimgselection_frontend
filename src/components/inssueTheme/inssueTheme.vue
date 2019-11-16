<template>
    <div class="inssueTheme-component">
        <div class="itemWrapper">
            <div class="title">
                主题：
            </div>
            <div class="content">
                <Input v-model="theme" placeholder="请输入主题内容" style="width: 500px;vertical-align: top;" />
            </div>
        </div>
        <div class="itemWrapper">
            <div class="title">
                描述：
            </div>
            <div class="content">
                <Input v-model="describe" :rows="4" type="textarea" placeholder="请输入主题描述" style="width: 500px;vertical-align: top;" />
            </div>
        </div>
        <div class="btnWrapper">
            <Button style="width: 400px;" size="large" type="primary">提 交</Button>
        </div>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            theme: "", // 主题内容
            describe: "", // 主题描述
        }
    }
}
</script>

<style>
.inssueTheme-component {
    margin: auto;
    padding-top: 30px;
    width: 90%;
    background-color: #fff;
    border: 1px solid #ddd;
}
.inssueTheme-component .itemWrapper {
    margin-bottom: 30px;
    font-size: 30px;
    text-align: center;
}
.inssueTheme-component .itemWrapper .title {
    display: inline-block;
    min-width: 6em;
    vertical-align: top;
}
.inssueTheme-component .itemWrapper .content {
    display: inline-block;
}
.inssueTheme-component .btnWrapper {
    padding-bottom: 15px;
    text-align: center;
}

.inssueTheme-component .ivu-input {
    font-size: 18px;
}

.inssueTheme-component .ivu-input {
    font-size: 18px;
}

.inssueTheme-component textarea.ivu-input {
    font-size: 18px;
}
</style>