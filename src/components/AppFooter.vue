<script>

  export default {

      data(){
        return{
          arrayIconeFooter : [
            { label: 'fa-brands fa-facebook',
              bk: 'background-color: #3b5998'
            },
            { label: 'fa-brands fa-instagram',
              bk: 'background-color: #c32aa3'  
            },
            { label: 'fa-brands fa-linkedin',
              bk: 'background-color: #0077b5' 
            },
            { label: 'fa-brands fa-pinterest',
              bk: 'background-color: #bd081c' 
            },
            { label: 'fa-brands fa-twitter',
              bk: 'background-color: #1da1f2' 
            },
            { label: 'fa-solid fa-basketball',
              bk: 'background-color: #ea4c89' 
            },
            { label: 'fa-brands fa-google-plus',
              bk: 'background-color: #db4437' 
            },
            { label: 'fa-brands fa-skype', 
              bk: 'background-color: #00aff0'
            },
          ]
        }
      }
  }
</script>
<template lang="">
  <footer >
    <div class="container-fluid">

        <div class="container-small">
            <div class="row">
                  <div class="col-3 text-white">
                      <h4>ABOUT</h4>
                      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid deserunt similique exercitationem numquam aut consequuntur repellendus culpa magnam et iusto.</p>
                  </div>
                  <div class="col-3 text-white">
                      <h4>CONTACT</h4>
                      <ul class="list-unstyled lista-contatti">
                        <li>USA, California 20, First Avenue, Callifornia</li>
                        <li>Tel.: +1 212 458 300 32</li>
                        <li>Fax: +1 212 375 24 14</li>
                        <li>info@masterstudy.com</li>
                      </ul>
                  </div>
                  <div class="col-3  text-white">
                      <h4>SOCIAL NETWORK</h4>
                      <div >
                        <ul class="list-unstyled d-flex  flex-wrap prova">
                          <li v-for="(item, index) in arrayIconeFooter" :key="index"  class=" d-flex align-item-center justify-content-center" :style="item.bk">
                              <i :class="item.label" class="align-self-center"></i> 
                          </li>
                        </ul>
            
                      </div>
                  </div>
                  <div class="col-3">
                      <img src="../assets/img/Top-udemy-courses-90-percent-off.jpg">
                  </div>
            </div>    
        </div>
    </div>
    
    <div class="container-fluid border-top color-grey"></div>
    <div class="container-fluid">
        <div class="container-small-2">
            <div class="row footer-inferiore">
                  <div class="col-12 d-flex text-white">
                    <img src="../assets/img/footer-logo2x-50x56.png" alt="logo-footer">
                    <span class="ms-3">Copryright <i class="fa-regular fa-copyright"></i> 2022. <a href="#">MasterStudy</a>. Theme by <a href="#">StylemixThemes</a></span>
                  </div>
            </div>    
        </div>
    </div>

  </footer>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

footer{
  background-color: $colorBlue;

  /*sezione superiore */
    .container-small{
      max-width: 1176px;
      margin: 0 auto;
      padding: 50px 0px;
        h4{
          font-weight: bold;
          font-family: 'Roboto', sans-serif;
        }
        p{
          font-weight: 100;
          font-size: 14px;
        }

        .lista-contatti{
          li{
            margin: 5px;
            font-size: 14px;
          }
          li:last-child{
            color: $colorGrey ;
            cursor: pointer;
          }
        }

        img{
          width: 100%;
        }
        .prova li{
          height: 50px;
          width: 50px;
          border-radius: 50%;
          margin:5px 5px;
             
            &:hover{
              background-color: $colorRed !important;
              cursor: pointer;

            }
          
          i{
            font-size: 25px;
          }
        }       

    }
  
  .color-grey{
    border :$colorGrey 1px solid;
  }

  .container-small-2{
      max-width: 1176px;
      margin: 0 auto;
      padding: 30px 0px;
  .footer-inferiore{
    img{
      width: 25px;
    }
    a{
      color: #fff;
      text-decoration: underline;
      &:hover{
        color: $colorRed
      }
    }
  }
}
}
  
</style>