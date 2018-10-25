<template>
    <div>
    <h3 :style="h3StyleObject"><strong>{{workingHistoryDetail.time}}	    {{workingHistoryDetail.jobTitle}}</strong></h3>
			<h5 :style="h5StyleObject">{{workingHistoryDetail.company}}</h5>
        <ul class="list-group text-sm-left experience-history" style="text-align: 'left'">           
            <li v-for="(task,index) in workingHistoryDetail.tasks" 
            :key="index"
            class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i> {{task}}}</li>
        </ul>
    </div>
</template>
<script>
export default {
  props: ["workingHistoryDetail"],
  data() {
    return {
      h3StyleObject: {
        color: "#4392F1"
      },
      h5StyleObject: {
        color: "#109fce",
        "font-weight": 800
      },
      listStyleObject: {
        color: "#ffffff",
        "background-color": "#4392F1"
      }
    };
  }
};
</script>
