<template>
    <div class="card" :style="listStyleObject">
        <div class="card-body" >
            <i :class="projectDetail.itemObjectClass"></i>
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