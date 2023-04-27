<script>
  import ExpertConsultant from "./Expertconsultant.vue";
  export default {
    name: "Jumbotron",
    components: {
      ExpertConsultant,
    },
    }  
  </script>

<template>
    <div class="jumbotron">
      <div class="container">
        <div class="content">
          <!-- Area Text -->
          <div class="area-text">
            <h2>Unlock Your Online Growth Potential</h2>
            <p>Online Marketing to secure customer retention, leads, and sales. We focus on the bigger picture.</p>
            <div class="white-button">
              Our Services <i class="fa-solid fa-arrow-right"></i>
            </div>
          </div>
          <!-- Expert consultant -->
          <div class="expert-consultant">
            <ExpertConsultant />
          </div>
        </div>
      </div>
    </div>
  </template>
 
  
  <style lang="scss" scoped>
  @import '../style/variable.scss';
  .jumbotron {
    background-image: url('../assets/img/marketing-intro.jpg');
    background-repeat: no-repeat;
    background-position-y: top;
    background-size: cover;
    height: 700px;
    width: 100%;
    .content {
      padding-top: 120px;
      display: flex;
    }
    .area-text {
      color: white;
      width: 50%;
      h2 {
        font-size: 70px;
        font-weight: bold;
      }
      p {
        font-size: 30px;
        padding: 25px 0;
      }
      .white-button {
        margin-top: 15px;
        i {
          padding-left: 10px;
        }
      }
    }
    .expert-consultant {
      position: relative;
      top: -20px;
    }
    
  }
  </style>