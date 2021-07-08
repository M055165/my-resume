<template>
<div id="contact">
    <div class="container">
       <div class="contact_content">
         <div class="header">
           <h2>Contact Me</h2>
         </div>
         <div class="content">
           <div class="img">

           </div>
           <div class="detail">
             <p>蔡竣智</p>
             <p><i class="fas fa-envelope mr-2"></i>Michael50601@gmail.com</p>
             <p><i class="fas fa-phone-alt mr-2"></i>0968-739-913</p>
           </div>
           <div class="icon">
             <a href="https://www.facebook.com/profile.php?id=100003019470559" target="_blank"><i class="fab fa-facebook-square"></i></a>
             <a href="https://github.com/M055165?tab=repositories" target="_blank"><i class="fab fa-github"></i></a>
             <a href="https://www.instagram.com/m055165/" target="_blank"><i class="fab fa-linkedin"></i></a>
           </div>
         </div>
       </div>
    </div>
</div>
</template>

<style lang="scss" scoped>
#contact {
  min-height: 80vh;
  color:white;
  font-weight: bold;
  padding-bottom: 80px;
}
.contact_content {
  margin: 0 auto;
  margin-top: 15vh;
  width: 50%;
  border-radius: 30px;
  background-image: linear-gradient(to bottom right, rgb(0, 79, 153), rgb(0, 149, 155));
  height: 90vh;
}
.header {
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  height: 25%;
  h2 {
    font-size: 40px;
  }
}
.content{
  height: 75%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  .img {
    width: 40%;
    height: 100%;
    border: 5px solid rgba($color: #fff, $alpha: .78);
    background-image: url('../assets/415644.jpg');
    background-size: cover;
    background-position: center center;
  }
  .detail {
    font-size: 25px;
    margin-top: 30px;
    height: 40%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
  }
  .icon {
    height: 40%;
    width: 100%;
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
    a {
      color:white;
      font-size: 40px;
      margin-right: 20px;
    }
  }
}
@media screen and (max-width: 767px) {
  .contact_content{
    width: 80%;
    height: 70vh;
  }
  .header {
    height: 25%;
    h2 {
    font-size: 30px;
  }
  }
  .content {
    .img {
      width: 65%;
      height: 100%;
    }
    .detail {
      p {
        font-size: 20px;
      }
    }
  }
}
</style>
