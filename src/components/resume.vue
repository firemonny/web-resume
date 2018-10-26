<template>
<div class="container">
    <div class="jumbotron" id="header-card">
        <div class="container">
          <div class="row">
            <div class="col-lg-3 col-sm-12">
              <div class="d-flex align-items-start">
                <img src="headPhoto.jpg" id="headPhoto" alt="Nung-Shun Chou" />
              </div>  
            </div>
            <div class="col-lg-6 col-sm-12">
               <h1>{{space}}</h1>
              <h1 id="lastname" class="d-flex justify-content-start">Monny</h1>
              <h1 id="firstname" class="d-flex justify-content-end">Chou</h1>    
            </div>
            <div class="col-lg-3 col-sm-12" id="skill-set">
              <h5 :style="skillSetTitleStyleObject">Skill Set</h5>
              <div v-for="(skillSetDetail,index) in skillSetDetails" :key="index">
                <skill-set :skillSet="skillSetDetail"></skill-set> 
              </div>
              <br>
              <p class="d-flex justify-content-around">
                <a href="https://github.com/firemonny/" target="_blank"><i class="fab fa-github fa-3x"></i></a>  
                <a href="https://www.linkedin.com/in/nung-shun-chou" target="_blank"><i class="fab fa-linkedin fa-3x"></i></a>  
                <a href="mailto:firemonny@gmail.com" target="_blank"><i class="fas fa-envelope fa-3x"></i></a>
              </p>
            </div>
          </div> 
        </div>
    </div>
<div class="container">
  <div class="row">
    <div class="col-lg-8 col-sm-12">
        <div v-for="(workingHistoryDetail,index) in workingHistoryDeatils" :key="index">
          <working-history :workingHistoryDetail="workingHistoryDetail"></working-history>
        </div>
    </div>
    <div class="col-lg-4 col-sm-12">
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
import workingHistory from "./workingHistory";
import skillSet from "./skillSet";

export default {
  data() {
    return {
      name: "Nung-Shun Chou",
      imgUrl: "../assets/Headphoto.jpg",
      space: "               ",
      skillSetDetails: [
        {
          icon: {
            fab: true,
            "fa-js-square": true
          },
          skill: "Javascript/VueJs"
        },
        {
          icon: {
            fas: true,
            "fa-database": true
          },
          skill: "Postgre SQL"
        },
        {
          icon: {
            fas: true,
            "fa-database": true
          },
          skill: "MongoDB"
        },
        {
          icon: {
            fab: true,
            "fa-python": true
          },
          skill: "Python"
        },
        {
          icon: {
            fas: true,
            "fa-map-marked": true
          },
          skill: "MapBox GL/GoogleMap API"
        },
        {
          icon: {
            fab: true,
            "fa-aws": true
          },
          skill: "AWS Expereience"
        }
      ],
      projectDetails: [
        {
          title: "Taipei Ubike Live Map",
          description: "A real-time tracking bike sharing information web app",
          itemObjectClass: {
            fas: true,
            "fa-bicycle": true,
            "fa-2x": true
          },
          url: "https://taipei-youbike.monnychou.com"
        },
        {
          title: "Canada Food Guide",
          description: "Coding challenge for sensorup company",
          itemObjectClass: {
            fas: true,
            "fa-utensils": true,
            "fa-2x": true
          },
          url: "https://evening-escarpment-63030.herokuapp.com/"
        },
        {
          title: "Stock Trade Simulator App",
          description: "Vue Learning Project",
          itemObjectClass: {
            fas: true,
            "fa-money-bill": true,
            "fa-2x": true
          },
          url:
            "http://monny-stock-trade-app.s3-website.ca-central-1.amazonaws.com/"
        }
      ],
      workingHistoryDeatils: [
        {
          time: "2018 - present",
          company: "SensorUp Inc. – Calgary Alberta",
          jobTitle: "Junior Software Developer",
          tasks: [
            "Developing web apps project using Vue.js/React.js",
            "Geo-location API (Leaflet MapBoxGL) and chart library (Echart)",
            "Utilized git flow process and agile development",
            "Experience with Cloud Service (Amazon Web Services)",
            "Developing automate script and data analyzing using python"
          ]
        },
        {
          time: "2016 - 2017",
          company: "Hydro One – Mississauga Ontario",
          jobTitle: "Advance Meter Infrastructure Analyst Co-op",
          tasks: [
            "Full stack developer, Maintained metering data service production database",
            "Used SAP, IEE and Multiple Head end system to analyze and handle exceptions",
            "Produced automation script files for daily reports and tasks with Python",
            "Troubleshot and designed solutions for improving telecommunication network",
            "Completed complex meter system design projects"
          ]
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
    "project-card": projectCard,
    "working-history": workingHistory,
    "skill-set": skillSet
  }
};
</script>
<style>
#header {
  background-color: #42b9f4;
}

#lastname {
  font-family: "Kaushan Script";
  font-size: 6em;
  color: #0a8908;
  font-weight: 800;
  text-shadow: 2px 2px grey;
}

#firstname {
  font-family: "Kaushan Script";
  font-size: 4em;
  color: #0db20a;
  font-weight: 700;
  text-shadow: 2px 2px grey;
}

#header-card {
  background-color: #f5f5dc;
  border-color: #a5e510;
  border-width: 0 0 5px 0;
  border-style: solid;
  padding: 10px 0 0 0;
}

#skill-set {
  font-weight: 800;
  text-align: left;
}

#headPhoto {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  box-shadow: 3px 3px 8px gray;
  margin: 30px 0 0 0;
}
.experience-history {
  background-color: #f5f5dc;
}
</style>
