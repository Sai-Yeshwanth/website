<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" 
    integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w==" 
    crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="index.css">
    <script src="https://kit.fontawesome.com/a076d05399.js"></script>
    <title>Document</title>
  <style>
    *{
    padding: 0;
    margin: 0;
    text-decoration: none;
    font-family: Arial, Helvetica, sans-serif;
    box-sizing: border-box;
}

/* first nav-bar */
.container .nav1{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    background: rgba(46, 139, 87, 0.5);
    top: 0;
    position: fixed;
    width: 100%;
    padding: 10px 0;
}
/* logo */
.nav1 .logo{
    padding-left: 15px;
}

/* a tags in links */
.nav1 .links a{
    text-decoration: none;
    color: black;
    font-size: 22px;
    padding: 10px 20px;
}
.nav1 .links a:hover{
    border-bottom: black 2px solid;
    font-size: 24px;
}

.links .current{
    background-color: rgba(61, 73, 128, 0.3);
    border-radius: 5px;
    font-weight: bolder;
}

.nav2{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-end;
    padding: 0px 20px 0 0;
    margin-top: 57px;
    background: rgb(231, 231, 102);
    padding: 10px;
}
.nav2 .search{
    padding-right: 300px;
}
.nav2 .login{
    padding-right: 100px;
}
.nav2 .login a{
    text-decoration: none;
    color: black;
    padding: 10px;
}
.nav2 .login a:hover{
    border-bottom: black 2px solid;
    font-size: 1.1em;
}
.nav2 .account{
    padding-right: 10px;
}
.nav2 .account a{
    text-decoration: none;
    color: black;
    padding: 10px;
}
.nav2 .account a:hover{
    border-bottom: black 2px solid;
    font-size: 1.1em;
}
.nav2 .search input{
    width: 400px;
    padding: 6px;
}

.side{
    position: absolute;
    padding: 0px 0 0 10px;
}

.sidemenu{
    position: fixed;
    width: 250px;
    height: fit-content;
    left: -250px;
    background: black;
    margin-top: 4px;
    transition: all .5s ease;
}
.btn{
    position: absolute;
    top: 70px;
    height: 45px;
    width: 45px;
    left: 25px;
    transition: left 0.4s ease;
    text-align: center;
    cursor: pointer;
}
.btn span{
    color: black;
}
.sidemenu .text{
    color: white;
    font-size: 25px;
    font-weight: 600;
    line-height: 65px;
    text-align: center;
}
.sidemenu ul li{
    line-height: 60px;
    border-bottom: 1px solid rgba(61, 73, 128, 0.3);
}
.sidemenu ul li a{
    color: white;
    font-size: 18px;
    padding-left: 20px;
    font-weight: 550;
    display: block;
    width: 100%;
    border-left: 5px solid transparent;
}
.sidemenu ul li a:hover{
    color: teal;
    border-left-color: teal;
}
#check{
    display: none;
}

label #btn,label #cancel{
    position: absolute;
    cursor: pointer;
}
label #btn{
    top:10px;
    left:25px;
    font-size: 30px;
    color: black;
    transition: all .5s ease;
}
label #cancel{
    z-index: 1111;
    left: -220px;
    top: 30px;
    color: white;
    transition: all .5s ease;
}
#check:checked ~ .sidemenu{
    left: 0;
}
#check:checked ~ label #btn{
    left: 250px;
    opacity: 0;
    pointer-events: none;
}
#check:checked ~ label #cancel{
    left: 220px;
}

  </style>
  
</head>
<body>
    <div class="main">
        <div class="container">
            <div class="nav1">
                <div class="logo">
                    <h1><i class="fas fa-dollar-sign"></i> Fair-Fare</h1>
                </div>
                <div class="links">
                    <a href="#" class="current"><i class="fas fa-home"></i> Home</a>
                    <a href="#" ><i class="fas fa-globe"></i> About Us</a>
                    <a href="#" ><i class="fas fa-users"></i> Our Team</a>
                    <a href="#" ><i class="fas fa-cogs"></i> Support</a>
                </div>
            </div>
            <div class="side">
                <input type="checkbox" id="check">
                <label for="check">
                <i class="fas fa-bars" id="btn"></i>
                <i class="fas fa-times" id="cancel"></i>
                </label>
                <div class="sidemenu">
                    <div class="text">Categories</div>
                        <ul>
                            <li><a href="#">Clothes</a></li>
                            <li><a href="#">Mobiles</a></li>
                            <li><a href="#">Laptops</a></li>
                            <li><a href="#">Jewellery</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="nav2">
                <div class="search">
                    <input type="text" placeholder="Search here...">
                    <i class="fas fa-search"></i>
                </div>
                <div class="login">
                    <h3><a href="#"><i class="fas fa-user"></i> Login</a></h3> 
                </div>
                <div class="account">
                    <div class="account">
                        <h3><a href="#"><i class="fas fa-user"></i> My Account</a></h3> 
                    </div>
                </div>
            </div>
        </div>
    </div> 
</body>
</html>
