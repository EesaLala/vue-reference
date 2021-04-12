<template>
<div class="content">
    <h2>Footer component</h2>
    <br>
    <h4>
      {{ propMsg }}
    </h4>
</div>
</template>

<script>
export default {
    props: ['propMsg']

};
</script>

<style>
    .content {
        background-color: aquamarine;
    }
</style>