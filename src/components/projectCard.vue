<template>
    <div class="card" :style="listStyleObject">
        <div class="card-body" >
            <a style="color: #FFAD05" :href="projectDetail.url" target="_blank"><i :class="projectDetail.itemObjectClass"></i></a>
            <h5 class="card-title">{{projectDetail.title}}</h5>
            <p  class="card-text">{{projectDetail.description}}</p>
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
        "background-color": "#FEDD14",
        "margin-top": "20px",
        "color": "#FFAD05"
      }
    };
  },
  name: "projectCard"
};
</script>