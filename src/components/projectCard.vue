<template>
    <div class="card">
        <div class="card-body" :style="listStyleObject">
            <h5 class="card-title">{{projectDetail.title}}</h5>
            <p class="card-text">{{projectDetail.description}}</p>
        </div>
    </div>
</template>
<script>
export default {
  props: ["projectDetail"],
  data() {
    return {
      listStyleObject: {
        width: "18rem",
        "background-color": "#FEDD14"
      }
    };
  },
  name: "projectCard"
};
</script>