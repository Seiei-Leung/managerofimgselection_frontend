<template>
    <div class="index-component">
        <div class="tabWrapper">
            <Tabs value="inssueTheme">
                <TabPane label="发布主题" name="inssueTheme">
                    <v-inssueTheme></v-inssueTheme>
                </TabPane>
                <TabPane label="主题管理" name="managerOfTheme">
                    <v-managerOfTheme></v-managerOfTheme>
                </TabPane>
            </Tabs>
        </div>
    </div>
</template>

<script>
import managerOfTheme from "../managerOfTheme/managerOfTheme";
import inssueTheme from "../inssueTheme/inssueTheme";

export default {
    data: function() {
        return {

        }
    },
    components: {
        "v-managerOfTheme": managerOfTheme,
        "v-inssueTheme": inssueTheme,
    }
}
</script>

<style scoped>
.tabWrapper {

}
</style>