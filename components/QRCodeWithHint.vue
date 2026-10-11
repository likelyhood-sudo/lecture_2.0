<script setup lang="ts">
import QRCode from 'slidev-addon-qrcode/components/QRCode.vue'

const props = defineProps({
    ...QRCode.props,
    hint: String
})
</script>

<template>
    <div class="text-center w-fit">
        <QRCode class="w-fit" v-bind="$props" :height="props.width" />
        <a :href="props.data">
            {{ props.hint }}
        </a>
    </div>
</template>
