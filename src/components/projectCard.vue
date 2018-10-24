<template>
    <div class="card" style="width: 18rem;">
        <div class="card-body">
            <h5 class="card-title">{{projectDetail.title}}</h5>
            <p class="card-text">{{projectDetail.description}}</p>
        </div>
    </div>
</template>
<script>
export default {
  props: ["projectDetail"],
  name: "projectCard"
};
</script>