<template>
    <div class="managerOfTheme-component">
        <div class="themeWrapper" v-if="!isShowManagerOfWorks">
            <List item-layout="vertical">
                <ListItem v-for="(item, index) in resourceData" :key="index">
                    <ListItemMeta  avatar="https://dev-file.iviewui.com/userinfoPDvn9gKWYihR24SpgC319vXY8qniCqj4/avatar" :title="item.title" :description="item.describe" />
                    <template slot="action">
                        <li>
                            <a href="">修改主题</a>
                        </li>
                        <li>
                            <a href="">管理参赛作品</a>
                        </li>
                        <li>
                            <a href="">删除主题</a>
                        </li>
                    </template>
                </ListItem>
            </List>
        </div>
        <!-- 管理参赛作品 -->
        <v-managerOfWorks v-if="isShowManagerOfWorks"></v-managerOfWorks>
    </div>
</template>

<script>
import managerOfWorks from "../managerOfWorks/managerOfWorks";

export default {
    data: function() {
        return {
            isShowManagerOfWorks: true, // 是否显示作品管理
            resourceData: [
                {
                    "title": "图片投票",
                    "describe": "赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情赛事详情"
                },
                {
                    "title": "图片投票",
                    "describe": "赛事详情"
                }
            ],
        }
    },
    components: {
        "v-managerOfWorks": managerOfWorks
    }
}
</script>

<style scoped>
.managerOfTheme-component {
    box-sizing: border-box;
    margin: auto;
    width: 90%;
    padding: 20px;
    background-color: #fff;
    border: 1px solid #ddd;
}
</style>