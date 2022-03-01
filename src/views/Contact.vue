<template>
  <div class="container d-flex justify-content-center">
    <div class="row my-2 mx-2">
        <div class="col-md-6"> <img src="../assets/undraw_contact_us_re_4qqt.svg" alt="IMG"> </div>
        <!--col-->
        <div class="col-md-6">
            <h2 class="form-title" style="color: #004c4c">Contact us</h2>
            <p class="justify text-muted">Have an enquiry or would like to give us feedback?<br>Fill out the form below to contact our team.</p>
            <div class="social-icons">
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-instagram"><b-icon-instagram></b-icon-instagram></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-twitter"><b-icon-twitter></b-icon-twitter></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-facebook"><b-icon-facebook></b-icon-facebook></i></span> </li></a>
          <a href="#"
            ><li> <span class="dot"><i class="fa fa-linkedin"><b-icon-linkedin></b-icon-linkedin></i></span> </li></a>
        </div>
            <form>
                <div class="form-group pt-2 pl-1"> <label for="exampleInputName">Your name</label> <input type="text" class="form-control" id="exampleInputName"> </div>
                <div class="form-group pl-1"> <label for="exampleInputEmail1">Your email address</label> <input type="email" class="form-control" id="exampleInputEmail1"> </div>
                <div class="form-group pl-1"> <label for="exampleFormControlTextarea1">Your message</label> <textarea class="form-control" id="exampleFormControlTextarea1" rows="5"></textarea> </div>
                <div class="row">
                    <div class="col-md-3 offset-md-9"><button type="submit" class="btn btn-primary">Send</button></div>
                </div>
            </form>
        </div>
        <!--col-->
    </div>
    <!--row-->
</div>
</template>

<script></script>

<style scoped>
.container {
    background: #fff;
    margin-top: 50px;
    padding: 20px 20px 20px 20px;
    box-sizing: border-box;
    border-radius: 20px;
    width: auto
}

img {
    padding-top: 110px;
    padding-left: 50px;
    width: 100%;
    height: 100%
}

.text-muted {
    font-size: 15px;
    font-weight: bold
}

.form-title {
    font-weight: bold
}

.form-group label {
    font-size: 15px;
    font-weight: bold;
    padding-left: 5px;
    color: #004c4c
}

.form-control {
    border: none;
    border-radius: 20px;
    background: rgba(165, 147, 69, 0.075);
    box-shadow: 0px 1px 1px 1px rgba(0, 0, 0, 0.2)
}

.form-control:focus {
    color: #004c4c;
    border-color: #fff !important;
    outline: 0;
    box-shadow: 0 1px 1px 1px rgba(0, 123, 255, .25) !important
}

.social-icons {
    list-style: none;
    display: inline-flex;
    right: 16px;
    position: relative
}

.social-icons li {
    padding: 10px
}

.social-icons li i {
    line-height: 50px;
    position: relative;
    font-size: 30px;
    color: #004c4c;
}

.btn {
    background: linear-gradient(to right, #004c4c  0%, #1ea1a1 100%);
    border: none;
    height: 45px;
    transition: all 3s
}

.btn:hover {
    background: linear-gradient(to right, #1ea1a1 0%, #004c4c 100%)
}

.btn:focus {
    box-shadow: none
}
@media (max-width: 700px) {
img {
    padding-top: 70px;
    width: 65%;
    height: auto
}

}
</style>
