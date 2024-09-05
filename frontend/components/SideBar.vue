<template>
    <el-menu class="el-menu-vertical-demo" :default-active="activeMenu" background-color="#545c64" text-color="#fff"
        active-text-color="#ffd04b" router :collapse = "isCollapse">
        <el-menu-item index="/">
            <el-icon>
                <home />
            </el-icon>
            <template #title>Home</template>
        </el-menu-item>
        <el-menu-item index="/mytest/test">
            <el-icon>
                <info />
            </el-icon>
            <template #title>Test</template>
        </el-menu-item>
        <el-sub-menu index="1">
            <template #title>
                <el-icon>
                    <setting />
                </el-icon>
                <span>Settings</span>
            </template>
            <el-menu-item index="/settings/profile">Profile</el-menu-item>
            <el-menu-item index="/settings/security">Security</el-menu-item>
        </el-sub-menu>
    </el-menu>
</template>

<script setup>
import { ref } from 'vue'
import { useRoute } from 'vue-router'

// 动态设置活跃菜单项
const route = useRoute()
const activeMenu = ref(route.path)

// 展开折叠侧边栏
const isCollapse = ref(false)
</script>

<style scoped>
.el-menu-vertical-demo {
    width: 200px;
    min-height: 100vh;
}
</style>