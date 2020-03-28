# day4
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link rel="stylesheet" href="css/style.css">
<link rel="shortcut icon" href="css/sss.png" type="image/x-icon">
<title>Technosaraus</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<div class="topnav" id="myTopnav">
  <center><h1>TECHNOSARAUS</h1></center>
    <a href="#home" class="active">Home</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact Us</a>
    <a href="javascript:void(0);" class="icon" onclick="myFunction()">
      <i class="fa fa-bars"></i>
    </a>
  </div>
</head>
<body class="flex-container">
  <div >
  <div id="home" class="flex-item">
   <h1>HOME</h1>
   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt quaerat est neque quibusdam placeat porro, consequatur dolorum, explicabo, quisquam exercitationem illum cum<br/> delectus ducimus numquam animi suscipit. Magnam, delectus nisi?
  Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat laboriosam provident qui mollitia, ratione eaque laborum<br/> pariatur eligendi accusantium debitis facere, natus temporibus molestiae quis perspiciatis at voluptatem ipsum earum?
Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloribus repudiandae vel ad sit consequuntur, <br/>porro debitis fugiat nobis perferendis nostrum harum maxime in ea non facere veniam architecto, deleniti maiores?  
</P>
  </div>
<div id="gallery" class="flex-item">
  <h1><center>GALLERY</center></h1>
  <figure class="visible">
    <img src="css/lapu.jpg" alt="">
   <figcaption>Macbook Air</figcaption>
  </figure>
  <figure>
    <img src="css/macbook.jpg" alt="">
    <figcaption> Macbook Pro</figcaption>
  </figure>
  <figure>
    <img src="css/rollie.jpg" alt="">
    <figcaption>Alienware Area 51 M15x</figcaption>
  </figure>
  <figure>
    <img src="css/sammie.jpg" alt="">
    <figcaption>Samsung S20</figcaption>
  </figure>
  <figure>
    <img src="css/Pixelbook-hero-2_328851.jpg" alt="">
    <figcaption>Google Pixelbook</figcaption>
  </figure>
  </div>
<div class="flex-item" id="contact">
<h1><center>CONTACT US</center></h1>
<center>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste numquam laborum sed delectus iusto aliquid <br/>rem quis magnam, eius cum ea minima doloremque ipsam voluptate repellendus dolore? Recusandae, quasi obcaecati.</p>
<button type="button" class="collapsible">Read More</button>
<div class="content">
    <center>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora autem molestiae corporis quidem mollitia nesciunt ipsum fugiat, neque nobis iste iure. Numquam exercitationem voluptatum eveniet sequi porro<br/> ex commodi similique?Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt distinctio qui mollitia iusto nulla, quas a <br/>eligendi at asperiores labore ipsum eos, facere molestias! Beatae praesentium iure molestiae non quisquam.</p>
    </center>
  </div>
</center>

<footer id="sls" class="flex-item"><center><a href="#" class="fa fa-facebook"></a><a href="#" class="fa fa-twitter"></a></center></footer>

<script>
function myFunction() {
  var x = document.getElementById("myTopnav");
  if (x.className === "topnav") {
    x.className += " responsive";
  } else {
    x.className = "topnav";
  }
}
var slideInterval = 3500;
function getFigures() {
    return document.getElementById('gallery').getElementsByTagName('figure');

}

function moveFoward() {
    var pointer;
    var figures = getFigures();
    for (var i = 0; i< figures.length; i++) {
        if (figures[i].className == 'visible') {
            figures[i].className = '';
            pointer = i;
        }
    }
    if (++pointer == figures.length) {
        pointer = 0;
        
    }
    figures[pointer].className = 'visible';
    setTimeout(moveFoward, slideInterval);
}
function startPlayback() {
    setTimeout(moveFoward, slideInterval);
}
startPlayback();
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    if (content.style.display === "block") {
      content.style.display = "none";
    } else {
      content.style.display = "block";
    }
  });
}
</script>

</body>
</html>
