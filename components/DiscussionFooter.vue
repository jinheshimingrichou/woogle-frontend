<script lang="ts" setup>
import { ref, reactive } from 'vue'
const data = ref([
    {
        to: '/contactus',
        text: 'Contact Us',
    },
    {
        to: '/privacy',
        text: 'Privacy Policy',
    },
    {
        to: '/legalterms',
        text: 'Legal Terms',
    },
])
</script>

<template>
    <footer class="w-full b-t-2px b-color-#00EBFF">
        <div class="relative h-[30px] flex justify-center gap-[20px] flex-items-center bg-#01074B">
            © 2024
            <a
                v-for="(item, index) in data"
                :key="index"
                :href="item.to"
                class="text-[14px] color-[#fff] hover:color-color8 hover:underline"
            >
                {{ item.text }}</a
            >
        </div>
    </footer>
</template>

<style scoped lang="less"></style>
