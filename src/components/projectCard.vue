<template>
    <div class="card" :style="listStyleObject">
        <a style="color: #934505" :href="projectDetail.url" target="_blank">
          <div class="card-body" >
              <i :class="projectDetail.itemObjectClass"></i>
              <h5 class="card-title">{{projectDetail.title}}</h5>
              <p  class="card-text">{{projectDetail.description}}</p>
          </div>
        </a>
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
        color: "#934505"
      }
    };
  },
  name: "projectCard"
};
</script>