<script>
export default {
  name: "Header",
  props: {
      linksArray: Array,
      service: String,
  }
  
}
</script>

<template>
    <header>
        <div class="logo">
            <a href="#">
                <img src="../assets/images/avada-marketing-logo.png" alt="logo AvadaConsultant">
            </a>
        </div>

        <!-- Menu -->
        <nav>
            <ul>
                <li v-for="(link, index) in linksArray" :key="index">
                    <a :href="link.url">
                        {{link.text}}
                        <span v-if="link.dropDown"><i class="fa-solid fa-angle-down"></i></span>
                    </a>
                </li>
            </ul>
        </nav>

        <!-- Servizi -->
        <div class="services">
            <ul>
                <li class="number">
                    <a href="#">
                        <i class="fa-solid fa-phone"></i>{{service}}
                    </a>
                </li>

                <li>
                    <a href="#">
                        <span class="secondary-button"> 
                            Free Quote
                        </span>
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@import '../style/variable.scss';

header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100px;
    background-color:lime;
     ul {
        display: flex;
        
        li {
            padding-left: 30px;
            font-size: 15px;
            display: flex;
            align-items: center;
            
            a {
                color: black;
                padding: 5px 10px;
            }
        }
    }
    nav a:hover {
        color: $primary-color;
        border-bottom: 2px solid $primary-color ;
        padding-bottom: 3px;
    }
    .services {
        padding-left: 50px;
        font-size: 19px;
        i {
            color: orange;
            padding-right: 18px;
        }
        .secondary-button:hover {
            color: white;
            background-color: $primary-color;
        }
    }
}
</style>