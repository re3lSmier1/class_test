<script setup>
  const props = defineProps({
    name: {
      required: true
    },
    description: {
      required: true
    },
    imageUrl: {
      required: true
    }
  })
</script>

<template>
  <div class="col-sm-12 col-md-6 col-lg-4">
    <div class="card" style="margin: 15px" >
      <img :src="props.imageUrl" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{ props.name }}</h5>
        <p class="card-text">{{ props.description }}</p>
        <a href="#" class="btn btn-primary">{{ props.description }}</a>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>