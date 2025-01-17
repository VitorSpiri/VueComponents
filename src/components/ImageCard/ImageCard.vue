<script setup lang="ts">
import { computed } from 'vue';


interface ImageCardProps{
  width?: string,
  height?: string,
  src: string
}

const props = defineProps<ImageCardProps>()

const cssProps = computed(() => {
  return {
    'width': props.width ?? '100px',
    'height': props.height ?? '100px'
  }
})

</script>

<template>
    <figure :style="cssProps" class="image-card">
        <img class="image" :src="src" alt="selected image by user">
    </figure>
</template>

<style lang="css" scoped>

  .image-card{
    @apply rounded-lg
    border-2 border-gray-600;
  }

  .image{
    @apply w-full h-full;
    border-radius: 50%;
    box-shadow: 2px 2px 10px 0px rgba(0,0,0,0.75);
  }

  .image:hover{
    @apply cursor-pointer;
    transform:scale(1.02);
  }


</style>
