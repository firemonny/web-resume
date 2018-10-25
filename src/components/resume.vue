<template>
<div class="container">
    <div class="jumbotron" id="header-card">
        <div class="container">
          <div class="row">
            <div class="col-2">
              <div class="d-flex align-items-start">
                <img src="Headphoto.jpg" style="height: 180px" alt="Nung-Shun Chou" />
              </div>  
            </div>
            <div class="col-7">
               <h1>{{space}}</h1>
              <h1 id="lastname" class="d-flex justify-content-start">Monny</h1>
              <h1 id="firstname" class="d-flex justify-content-end">Chou</h1>    
            </div>
            <div class="col-3" id="skill-set">
              <h5 :style="skillSetTitleStyleObject">Skill Set</h5>
              <p><i class="fab fa-js-square"></i> Javascript/VueJs
              <br>
              <i class="fas fa-database"></i> Postgre SQL
              <br>
              <i class="fas fa-database"></i> MongoDB
              <br>
              <i class="fab fa-python"></i> Python
              <br>
              <i class="fas fa-map-marked"></i> MapBox GL/GoogleMap API
              <br>
              <i class="fab fa-aws"></i> AWS Expereience
              </p>
            <h5 :style="skillSetTitleStyleObject">Contact</h5>
              <p class="d-flex justify-content-around">
                <i class="fab fa-github fa-2x"></i>  
                <i class="fab fa-linkedin fa-2x"></i>  
                <i class="fas fa-envelope fa-2x"></i>  
              </p>
            </div>
          </div> 
        </div>
    </div>
<div class="container">
  <div class="row">
    <div class="col-8">
      <h3 :style="h3StyleObject"><strong>2018 - present	    Junior Software Developer</strong></h3>
			<h5 :style="h5StyleObject">SensorUp Inc. – Calgary Alberta</h5>
        <ul class="list-group text-sm-left experience-history" style="text-align: 'left'">
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Developing Web App project by Vue/React Js</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Geo-location API (Leaflet MapBoxGL) and chart library (Echart)</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Following git flow process and agile developemnt team</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Experience with Cloud Service (Amazon Web Services) </li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Analyzing different user requirements for the various database applications </li>
        </ul>
         <h3 :style="h3StyleObject"><strong>2016 - 2017	    Advance Meter Infrastructure Analyst Co-op</strong></h3>
			<h5  :style="h5StyleObject">Hydro One – Mississauga Ontario</h5>
        <ul class="list-group text-sm-left experience-history" style="text-align: 'left'">
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Full stack developer, Maintained metering data service production database</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Used SAP, IEE and Multiple Head end system to analyze and handle exceptions</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Produced automation script files for daily reports and tasks with Python</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Troubleshot and designed solutions for improving telecommunication network</li>
            <li class="list-group-item" :style="listStyleObject"><i class="fa fa-check"></i>Completed complex meter system design projects</li>
        </ul>
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
          description: "A real-time tracking bike sharing information web app",
          itemObjectClass:{
            fas :true,
            "fa-bicycle": true
          }
        },
        {
          title: "Canada Food Guide",
          description: "Coding challenge for sensorup company",
          itemObjectClass:{
            fas :true,
            "fa-utensils": true
          }
        }
      ],
      listStyleObject: {
        color: "#ffffff",
        "background-color": "#4392F1"
      },
      h3StyleObject: {
        color: "#4392F1"
      },
      h5StyleObject: {
        color: "#109fce",
        "font-weight": 800
      },
      skillSetTitleStyleObject: {
        "font-size": "1.75em",
        "font-weight": 900,
        color: "#0a8908"
      }
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

#lastname {
  font-family: "Permanent Marker";
  font-size: 8em;
  color: #0a8908;
  font-weight: 1000;
}

#firstname {
  font-family: "Permanent Marker";
  font-size: 3em;
  color: #0db20a;
  font-weight: 800;
}

#header-card {
  background-color: #f5f5dc;
  border-color: #a5e510;
  border-width: 20px;
  border-radius: 40px 40px;
  border-style: double;
}

#skill-set {
  font-weight: 800;
  text-align: left;
}

.experience-history {
  background-color: #f5f5dc;
}
</style>
