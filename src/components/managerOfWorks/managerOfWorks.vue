<template>
    <div class="managerOfWorks-component">
        <div class="olderWorksWrapper">
            <div class="itemWrapper">
                <div class="item">
                    <div class="title">
                        作品名：
                    </div>
                    <div class="content">
                        今天天气真好
                    </div>
                </div>
                <div class="item">
                    <div class="title">
                        简述：
                    </div>
                    <div class="content">
                        哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈呵呵呵呵哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈呵呵呵呵哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈呵呵呵呵哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈呵呵呵呵
                    </div>
                </div>
                <div class="item">
                    <div class="title">
                        参与人：
                    </div>
                    <div class="content">
                        Seiei
                    </div>
                </div>
                <div>
                    作品列表：
                </div>
                <div class="picWrapper">
<!--                     <div class="picItem">
                        <img class="img" src="https://dev-file.iviewui.com/userinfoPDvn9gKWYihR24SpgC319vXY8qniCqj4/avatar"/>
                        <div class="iconWrapper">
                            <Icon type="ios-close-circle" style="font-size: 30px;" />
                        </div>
                    </div> -->
<!--                     <div class="picItem">
                        <img class="img" src="https://dev-file.iviewui.com/userinfoPDvn9gKWYihR24SpgC319vXY8qniCqj4/avatar"/>
                        <div class="iconWrapper">
                            <Icon type="ios-close-circle" style="font-size: 30px;" />
                        </div>
                    </div> -->
                    <div class="demo-upload-list" v-for="(item, index) in uploadList" :key="index">
                        <template v-if="item.status === 'finished'">
                            <img :src="item.url">
                            <div class="demo-upload-list-cover">
                                <!-- <Icon type="ios-eye-outline" @click.native="handleView(item.name)"></Icon> -->
                                <Icon type="ios-trash-outline" @click.native="handleRemove(item)"></Icon>
                            </div>
                        </template>
                        <template v-else>
                            <Progress v-if="item.showProgress" :percent="item.percentage" hide-info></Progress>
                        </template>
                    </div>
                    <Upload
                        ref="upload"
                        :show-upload-list="false"
                        :default-file-list="defaultList"
                        :on-success="handleSuccess"
                        :format="['jpg','jpeg','png']"
                        multiple
                        type="drag"
                        action="//jsonplaceholder.typicode.com/posts/"
                        style="display: inline-block;width:58px;">
                        <div style="width: 58px;height:58px;line-height: 58px;">
                            <Icon type="ios-camera" size="20"></Icon>
                        </div>
                    </Upload>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            uploadList: [],
            defaultList: [],
        }
    },
    methods: {
        handleRemove: function(){

        },
        handleSuccess: function() {

        }
    }
}
</script>

<style scoped>
.itemWrapper {
    font-size: 18px;
}
.itemWrapper .item {
    display: flex;
    line-height: 1.8em;
}
.itemWrapper .item .title {
    width: 6em;
}
.itemWrapper .item .content {
    flex: 1;
}
.picWrapper {
    margin-top: 10px;
}
.picWrapper .picItem {
    display: inline-block;
    position: relative;
    width: 200px;
    height: 200px;
    margin-left: 5px;
}
.picWrapper .picItem .img {
    width: 100%;
    height: 100%
}
.picWrapper .picItem .iconWrapper {
    position: absolute;
    top: 0;
    right: 0;
}
</style>