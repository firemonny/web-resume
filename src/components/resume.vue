<template>
<div class="container">
    <div class="jumbotron">
        <div class="container">
            <div class="d-flex align-items-start">
                <img src="Headphoto.jpg" style="height: 180px" alt="Nung-Shun Chou" />
                <h1>{{space}}</h1>
                <h1>Monny Chou</h1>
            </div>      
        </div>
    </div>
<div class="container">
  <div class="row">
    <div class="col-8">
            <h3><strong>2018 - present	    Junior Software Developer</strong></h3>
			<h5>SensorUp Inc. – Calgary Alberta</h5>
        <ul class="list-group">
            <li class="list-group-item"><i class="fa fa-check"></i>Developing Web App project by Vue/React Js</li>
            <li class="list-group-item"><i class="fa fa-check"></i>Geo-location API (Leaflet MapBoxGL) and chart library (Echart)</li>
            <li class="list-group-item"><i class="fa fa-check"></i>Following git flow process and agile developemnt team</li>
            <li class="list-group-item"><i class="fa fa-check"></i>Experience with Cloud Service (Amazon Web Services) </li>
            <li class="list-group-item"><i class="fa fa-check"></i>Analyzing different user requirements for the various database applications </li>
        </ul>
            <i class="fa fab fa-github"></i>
            <i class="fa fa-address-card"></i>
            <i class="fa fa-check"></i>
    </div>
    <div class="col-4">
        <div v-for="(projectDetail, index) in projectDetails" :key="index">
            <project-card :projectDetail="projectDetail"></project-card>
        </div>
    </div>
  </div>
</div>
    </div>
    
</template>
<script>
import projectCard from "./projectCard.vue";
export default {
  data() {
    return {
      name: "Nung-Shun Chou",
      imgUrl: "../assets/Headphoto.jpg",
      space: "               ",
      projectDetails: [
        {
          title: "Taipei Ubike Live Map",
          description: "A real-time tracking bike sharing information web app"
        },
        {
          title: "Canada Food Guide",
          description: "Coding challenge for sensorup company"
        }
      ]
    };
  },
  components: {
    "project-card": projectCard
  }
};
</script>
<style>
#header {
  background-color: #42b9f4;
}
</style>
