<template>
    <div class="card" :style="listStyleObject">
        <div class="card-body" >
            <h5 class="card-title">{{projectDetail.title}}</h5>
            <p :style="paraStyle" class="card-text">{{projectDetail.description}}</p>
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
      },
      paraStyle: {
        color: "FFAD05"
      }
    };
  },
  name: "projectCard"
};
</script>