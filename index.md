Skip to content
 
Search…
All gists
Back to GitHub
@gyetman 
@mariawd
mariawd/calculator.html
Created 3 years ago • Report abuse
0
0
 Code
 Revisions 1
<script src="https://gist.github.com/mariawd/819e57131f42f3d2d2b71ee5d164d5b3.js"></script>
calculator.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->

    <title>Calculator</title>

    <!-- Bootstrap core CSS -->
    <!-- Latest compiled and minified CSS -->
    <!-- Latest compiled and minified CSS -->


    <!-- Custom styles for this template go here (AFTER Bootstrap CSS files)-->
    <link rel="stylesheet" href="css/calculatorstyles.css">


    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>

  <body>
  <br>

  <!-- Navigation bar starts here -->
    <div class="nav">
      <ul>
        <li><a href="index.html">Home</a></li>
      </ul>
    </div><!-- end div Nav -->

    <div class="container">
	   <fieldset id="container">
		  <form name="calculator">

			  <input id="display" type="text" name="display" readonly>

			  <input class="button digits" type="button" value="7" onclick="calculator.display.value += '7'">
			  <input class="button digits" type="button" value="8" onclick="calculator.display.value += '8'">
			  <input class="button digits" type="button" value="9" onclick="calculator.display.value += '9'">
			  <input class="button mathButtons" type="button" value="+" onclick="calculator.display.value += ' + '">
			  <br>
			  <input class="button digits" type="button" value="4" onclick="calculator.display.value += '4'">
			  <input class="button digits" type="button" value="5" onclick="calculator.display.value += '5'">
			  <input class="button digits" type="button" value="6" onclick="calculator.display.value += '6'">
			  <input class="button mathButtons" type="button" value="-" onclick="calculator.display.value += ' - '">
			  <br>
			  <input class="button digits" type="button" value="1" onclick="calculator.display.value += '1'">
			  <input class="button digits" type="button" value="2" onclick="calculator.display.value += '2'">
			  <input class="button digits" type="button" value="3" onclick="calculator.display.value += '3'">
			  <input class="button mathButtons" type="button" value="x" onclick="calculator.display.value += ' * '">
			  <br>
			  <input id="clearButton" class="button" type="button" value="C" onclick="calculator.display.value = ''">
			  <input class="button digits" type="button" value="0" onclick="calculator.display.value += '0'">
			  <input class="button mathButtons" type="button" value="=" onclick="calculator.display.value = eval(calculator.display.value)">
			  <input class="button mathButtons" type="button" value="/" onclick="calculator.display.value += ' / '">
		  </form>
	  </fieldset>
  </div>
</body>
</html>
calculatorstyles.css
body {
	 background: url("../img/compu4.jpg");
	 background-color: #424242;
	 font-family: Arial;
}

.container {
	 display: flex;
	 align-items: center;
	 justify-content: center;
	 height: 100vh;
	 width: 100vw;
}

#container {
	 width: 200px;
	 padding: 8px 8px 20px 8px;
	 margin: 20px auto;
	 background-color: #ABABAB;
	 border-radius: 4px;
	 border-top: 2px solid #FFF;
	 border-right: 2px solid #FFF;
	 border-bottom: 2px solid #C1C1C1;
	 border-left: 2px solid #C1C1C1;
	 box-shadow: -3px 3px 7px rgba(0, 0, 0, .6), inset -100px 0px 100px rgba(255, 255, 255, .5);
}

#display {
	 display: block;
	 margin: 15px auto;
	 height: 42px;
	 width: 174px;
	 padding: 0 10px;
	 border-radius: 4px;
	 border-top: 2px solid #C1C1C1;
	 border-right: 2px solid #C1C1C1;
	 border-bottom: 2px solid #FFF;
	 border-left: 2px solid #FFF;
	 background-color: #FFF;
	 box-shadow: inset 0px 0px 10px #030303, inset 0px -20px 1px rgba(150, 150, 150, .2);
	 font-size: 28px;
	 color: #666;
	 text-align: right;
	 font-weight: 400;
}

.button {
	 display: inline-block;
	 margin: 2px;
	 width: 42px;
	 height: 42px;
	 font-size: 16px;
	 font-weight: bold;
	 border-radius: 4px;
}

.mathButtons {
	 margin: 2px 2px 6px 2px;
	 color: #FFF;
	 text-shadow: -1px -1px 0px #44006F;
	 background-color: #434343;
	 border-top: 2px solid #C1C1C1;
	 border-right: 2px solid #C1C1C1;
	 border-bottom: 2px solid #181818;
	 border-left: 2px solid #181818;
	 box-shadow: 0px 0px 2px #030303, inset 0px -20px 1px #2E2E2E;
}

.digits {
	 color: #181818;
	 text-shadow: 1px 1px 0px #FFF;
	 background-color: #EBEBEB;
	 border-top: 2px solid #FFF;
	 border-right: 2px solid #FFF;
	 border-bottom: 2px solid #C1C1C1;
	 border-left: 2px solid #C1C1C1;
	 border-radius: 4px;
	 box-shadow: 0px 0px 2px #030303, inset 0px -20px 1px #DCDCDC;
}

.digits:hover,
.mathButtons:hover,
#clearButton:hover {
	 background-color: #FFBA75;
	 box-shadow: 0px 0px 2px #FFBA75, inset 0px -20px 1px #FF8000;
	 border-top: 2px solid #FFF;
	 border-right: 2px solid #FFF;
	 border-bottom: 2px solid #AE5700;
	 border-left: 2px solid #AE5700;
}

#clearButton {
	 color: #FFF;
	 text-shadow: -1px -1px 0px #44006F;
	 background-color: #D20000;
	 border-top: 2px solid #FF8484;
	 border-right: 2px solid #FF8484;
	 border-bottom: 2px solid #800000;
	 border-left: 2px solid #800000;
	 box-shadow: 0px 0px 2px #030303, inset 0px -20px 1px #B00000;
}
index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->

    <title>MRH Web Development</title>

    <meta property="og:url"           content="http://http://stoic-wing-510d47.bitballoon.com/" />
    <meta property="og:type"          content="website" />
    <meta property="og:title"         content="MRH Web Development" />
    <meta property="og:description"   content="Web Development services" />
    <meta property="og:image"         content="https://www.facebook.com/mrhwebdevelopment"/>


    <!-- Bootstrap core CSS -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.7/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Custom styles for this template go here (AFTER Bootstrap CSS files)-->
    <link rel="stylesheet" href="css/styles.css">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->

    <!--  JavaScript code -->
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>

  </head>


  <body data-spy="scroll" data-target=".navbar">

    <!-- Load Facebook SDK for JavaScript -->
    <div id="fb-root"></div>
    <script>(function(d, s, id) {
    var js, fjs = d.getElementsByTagName(s)[0];
    if (d.getElementById(id)) return;
    js = d.createElement(s); js.id = id;
    js.src = 'https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.12';
    fjs.parentNode.insertBefore(js, fjs);
    }(document, 'script', 'facebook-jssdk'));</script>

  <!-- Navigation bar starts here -->

  <!-- Collect the nav links, forms, and other content for toggling: -->
  <nav class="navbar navbar-inverse navbar-fixed-top" role="navigation">
    <div class="container-fluid">

        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header"> <!--Change the navigation bar to another type of navigation bar—a mobile-friendly one -->

          <!-- The following button only appears when the navigation bar is collapsed -->
           <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar-1" aria-expanded="false">
              <span class="sr-only">Toggle navigation</span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
           </button> <!--end button -->

           <div class="projectName navbar-brand">
              <a href="#index">MRH Web Development</a>
           </div>    <!--End projectName -->
        </div>  <!--End navbar-header -->

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="navbar-1">
          <ul class="nav navbar-nav navbar-right">

            <li><a href="#index">Home</a></li>
            <!-- Dropdown Menu -->
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Work <span class="caret"></span></a>
                <ul class="dropdown-menu">
                  <li><a href="#work1">Project I</a></li>
                  <li><a href="#work2">Project II</a></li>
                </ul><!-- End ul class Dropdown Menu -->
            </li><!-- end Dropdown Menu -->
            <li><a href="#about">About</a></li>
            <li><a href="#faq">FAQ</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul><!-- end class="nav navbar-nav navbar-right"-->
      </div><!-- end div navbar-collapse -->
    </div><!-- end div container-fluid -->
  </nav><!-- end navbar-inverse navigation -->
 <!-- Navigation bar ended here -->


<!-- =========================================== -->
<!--               Home Page                     -->
<!-- =========================================== -->


  <!--<!- Main jumbotron for a primary marketing message or call to action -<div class="jumbotron"> -->

   <div class="container-fluid anchor" id="index">

     <!-- - - - - -Carousel- - - - - - - -->

      <div id="carousel-example-generic" class="carousel slide" data-ride="carousel" style="height: 60%">

        <!-- Indicators - dots at the bottom indicating which slide you're currently on -->
        <ol class="carousel-indicators">
          <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
          <li data-target="#carousel-example-generic" data-slide-to="1"></li>
          <li data-target="#carousel-example-generic" data-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides - contains the images and captions for each slide -->
       <div class="carousel-inner" role="listbox">
         <div class="item active">
           <img src="img/compu1.jpg" alt="CLEAR AND CREATIVE IDEAS..." class="img-responsive">
           <div class="carousel-caption">
             <h3>CLEAR AND CREATIVE IDEAS...</h3>
             <br>
             <br>
             <br>
             <br>
            </div>
         </div> <!-- End div class item active -->

        <div class="item">
           <img src="img/compu2.jpg" alt="Slide 2">
           <div class="carousel-caption">
             <h3>MODERN, CLEAN AND TASTEFUL DESIGN ... </h3>
             <br>
             <br>
             <br>
           </div>
        </div> <!-- End  div class item -->

        <div class="item">
           <img src="img/compu3.jpg" alt="Slide 3">
           <div class="carousel-caption">
              <h3>AND ... YOU ARE NOW ON THE WEB!</h3>
              <br>
              <br>
              <br>
              <br>
            </div>
        </div> <!-- End  div class item -->

      </div> <!-- End div carousel-inner -->

       <!-- Controls - (are the arrows on the left and right sides of the slide) -->
       <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
         <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
         <span class="sr-only">Previous</span>
       </a>
       <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
         <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
         <span class="sr-only">Next</span>
       </a>
    </div> <!-- End div id -->
  </div> <!-- End div class=container-fluid -->


    <div class="container">
      <!-- Example row of columns -->
      <div class="index-copy"><!--styling this allows you to expand the page length if necessary-->

      <div class="row">
        <div class="col-md-4">
          <h2><strong>Portfolio Concept</strong></h2>
          <p>My portfolio should show my creative capacity, should reflect my desire to satisfy the client's needs with a personalized approach, a dynamic and engaging design, combining style, inspiration and aesthetics. </p>
          <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
        </div><!-- /End col -->
        <div class="col-md-4">
          <h2><strong>Project Goals</strong></h2>
          <p>My purpose is to dedicate 25 hours or more per week to the study of web developent techniques and to acquire the necessary practice for the creation of attractive web pages, with modern design techniques. </p>
          <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
       </div><!-- /End col -->
        <div class="col-md-4">
          <h2><strong>Course Goals</strong></h2>
          <p>With this course I intend to enter another area of ​​my professional training in computer science, focusing on the design, wich is one of my passions and the development of web pages, which seems to mee a fascinating work option.</p>
          <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
        </div><!-- /End col -->
      </div><!-- /End row -->

    </div> <!--/End index-copy-->

    </div> <!-- /End container -->


      <!-- =========================================== -->
      <!--                WORK Section                 -->
      <!-- =========================================== -->


    <div class="container-fluid anchor work" id="work1">

       <div class=”row”>
         <div class="header">
            <h1>My Work</h1>
         </div><!-- End header -->
         <h2 id="work2">Project I</h2>
           <div class="col-md-3 col-xs-6">
            <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>
           <div class="col-md-3 col-xs-6">
             <img src="img/work1.jpg" class="img-responsive center-block">
           </div>

        <div class="row anchor"  id="work2">
            <div class="col-md-4 col-xs-12">
             <h2>Project II</h2>
               <a href="calculator.html" title="Calculator" id="work2">
                <img src="img/calculator.jpg" alt="Calculator">
               </a>
            </div>
        </div>
  </div><!-- /End row -->

    </div> <!-- /End container -->

    <!-- ********************************* -->
    <!--            ABOUT SECTION          -->
    <!-- ********************************* -->

       <div class="container anchor about" id="about" data-stellar-background-ratio="0.5">
         <div class="header">
           <h1><strong>About Me</strong></h1>
         </div><!-- End header -->

         <div class="row">
           <div class="col-md-4 col-xs-12">
             <div class="image column">
               <img src="img/mrh.jpeg" alt="Image mrh">
             </div><!-- End image -->
           </div><!-- End col-md-4 col-xs-4 -->

           <div class="col-md-4 col-xs-12">
             <div class="intro column">
               <h2 class="concept">Introduction</h2>
                 <p>Creativity, passion for gut design, good taste and professionalism are the bases of my work as a Web Developer. Come and discover my talents!</p>
             </div><!-- End intro -->
           </div><!-- End col-md-4 col-xs-4 -->

           <div class="col-md-4 col-xs-12">
             <div class="skills column" style="background: #fff8dc;">
               <h3 class="concept">My Skills</h3>
                 <ul class="skill-list" id="skill-list">
                   <li>Creativ</li>
                   <li>Professional</li>
                   <li>Innovative</li>
                   <li>Enthusiastic</li>
                 </ul><!-- End ul -->
             </div><!-- End skills column -->
           </div><!-- End col-md-4 col-xs-4 -->
         </div><!-- End row -->

         <div class="main-text">
           <h3 class="concept"><strong>More About Me</strong></h3>
             <strong>I like to put my qualities and inspiration at the service of those who are looking for novelty, quality, empathy and commitment.</strong></p>
         </div><!-- End main-text-->
       </div><!-- End container -->


  <!-- ********************************* -->
  <!--            FAQ SECTION            -->
  <!-- ********************************* -->

<section class="faq" id="faq">

  <div class="container-fluid anchor">
    <div class="row">
      <div class="header">
        <h1><strong>Frecuently asked question</strong></h1>
      </div><!-- End header - Título del texto -->
    </div><!-- /row -->
<br>
<br>

  <!-- ***********  Acordeon  ************* -->


  <div class="panel-group" id="accordion">
    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#missingcode" href="#collapseOne"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
            How can we help you with your project?
          </a><!-- end collapsed -->
        </h4><!-- end panel title -->
    </div><!-- end panel-heading -->

    <div id="collapseOne" class="panel-collapse collapse in">
        <div class="panel-body">
          If you tell us about your ideas, we can help you to plan them, to specify them or to improve them, with the best design tools.
        </div><!-- end panel body -->
      </div><!-- end collapseOne -->
    </div><!-- end panel panel-default -->

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#missingcode" href="#collapseTwo"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
            How to engage  the services of web developer?
          </a><!-- end collapsed -->
        </h4><!-- end panel title -->
    </div><!-- end panel-heading -->

    <div id="collapseTwo" class="panel-collapse collapse">
        <div class="panel-body">
          Contact us  on the phone 00 49 6684952 or send us an email to the email address: mroblesar@hotmail.com
You can also do it on the contact page through the formular.
Once we have talked about your project, we will propose a budget and if you agree, we will proceed to work.
        </div><!-- end panel body -->
      </div><!-- end collapse -->
    </div><!-- end panel panel-default -->

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#missingcode" href="#collapseThree"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
            What kind of projects will be undertaken?
          </a><!-- end collapsed -->
        </h4><!-- end panel title -->
      </div><!-- end panel-heading -->

      <div id="collapseThree" class="panel-collapse collapse">
        <div class="panel-body">
          The projects can be a rebuild website or a new one. If it is a rebuild one, we will review your current content and we will make recommendations for improvements. If it is a new site, we will start by discussing the subjects and functionality you envisage for your site and we will develop an outline for you.
        </div><!-- end panel body -->
      </div><!-- end collapse -->
    </div><!-- end panel panel-default -->

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#missingcode" href="#collapseFour"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
            How long does it take to develop a web page?
          </a><!-- end collapsed -->
        </h4><!-- end panel title -->
      </div><!-- end panel-heading -->

      <div id="collapseFour" class="panel-collapse collapse">
        <div class="panel-body">
          The time of web design and development depends on the type of project and the workload that exists at the moment.
In general terms a corporate website can be completed between 15 and 30 days.
For an online store the development time can include between 20 and 40 days.
        </div><!-- end panel body -->
      </div><!-- end collapse -->
    </div><!-- end panel panel-default -->

      <div class="panel panel-default">
        <div class="panel-heading">
          <h4 class="panel-title">
            <a data-toggle="collapse" data-parent="#missingcode" href="#collapseFive"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
              How does the development process work?
            </a><!-- end collapsed -->
          </h4><!-- end panel title -->
        </div><!-- end panel-heading -->

        <div id="collapseFive" class="panel-collapse collapse">
          <div class="panel-body">
            The development process involve some steps:
Preliminary Design: We create a home page concept including colors, fonts, image style and layout.
Structuration: When we have received all content in its final version, we review it to determine the best way to organize the information. The structure of the site is based on this organizational scheme and must be approved by you.
Design Revision – After reviewing the initial design, you have the opportunity to request changes.
Implementation – With your approval on the design, we begin the implementation, so the approved design becomes concrete, with all the content that the site should include and all the data.
Testing - We run through a final set of tests to be sure that everything is functional. You have an opportunity at this time to test the site as well.
Launch – Once we have your final approval, we launch the site.
          </div><!-- end panel body -->
        </div><!-- end collapse -->
      </div><!-- end panel panel-default -->

      <div class="panel panel-default">
        <div class="panel-heading">
          <h4 class="panel-title">
            <a data-toggle="collapse" data-parent="#missingcode" href="#collapseSix"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
              Are your sites mobile-friendly?
            </a><!-- end collapsed -->
          </h4><!-- end panel title -->
        </div><!-- end panel-heading -->

        <div id="collapseSix" class="panel-collapse collapse">
          <div class="panel-body">
            Yes. The method we use to achieve this is known as responsive design, which ensures that the site works well on a wide variety of screen sizes, from smartphones and tablets through to small and large desktop monitors.
          </div><!-- end panel body -->
        </div><!-- end collapse6 -->
      </div><!-- end panel panel-default -->

      <div class="panel panel-default">
        <div class="panel-heading">
          <h4 class="panel-title">
            <a data-toggle="collapse" data-parent="#missingcode" href="#collapseSeven"><span class="glyphicon glyphicon glyphicon-menu-down"></span>
              Who are our customers?
            </a><!-- end collapsed -->
          </h4><!-- end panel title -->
        </div><!-- end panel-heading -->

        <div id="collapseSeven" class="panel-collapse collapse">
          <div class="panel-body">
            We are oriented to all kinds of clients, from individuals looking to have their personal informative website, as well as those who want commercial web pages or companies that require complex interactive web pages.
          </div><!--"panel-body"-->
        </div><!-- end collapseOne -->
      </div><!-- end panel panel-default -->

  </div><!--end panel panel-group-->

 </div><!-- end container -->

</section><!-- end section -->


<!-- ********************************* -->
<!--               CONTACT             -->
<!-- ********************************* -->

   <div class="contact-info" id="contact">
     <div class="container-fluid anchor">

       <div class="col-lg-4 col-md-4">
         <h1><strong>Contact</strong></h1>
         <h6><strong> Contact us, to make your website unique, like yourself.</strong></h6>
         <br>
         <h2><span class="glyphicon glyphicon-envelope"></span> Email: mroblesar@hotmail.com</h2>
         <h3><span class="glyphicon glyphicon-home"></span> Address: Heresbachstr. 22</h3>
         <h4>40223 Düsseldorf. Germany</h4>
         <h5><span class="glyphicon glyphicon-earphone"></span> Phone: 049 3625678</h5>
      </div> <!-- end div class col-lg-4 col-md-4 -->


         <div class="contact-form-info">
           <form id="contact-form">

             <div class="col-lg-8 col-md-8">

               <div class="col-md-6 col-xs-6">
                 <div class="form-group">
                   <label for="Name">Name *</label>
                   <input class="form-control" type="text" placeholder="Enter your name here" required="required" id="Name">
                 </div> <!-- end div class form-group -->
               </div> <!-- end div class col-md-6 col-xs-12" -->

               <div class="col-md-6 col-xs-6">
                 <div class="form-group">
                   <label for="Phone">Phone</label>
                   <input class="form-control" type="tel" placeholder="Enter your phone number here" required="required" id="Phone">
                 </div><!--end form-group -->
              </div> <!-- end div class col-md-6 col-xs-12" -->


                <div class="form-group">
                  <label for="Email">Email address *</label>
                  <input class="form-control" type="email" placeholder="Enter your email" required="required" type="text" id="Email">
                </div><!-- end div class form-group -->
                <div class="form-group">
                  <label for="Message">Your Message *</label>
                  <textarea class="form-control" style="resize:none" cols="40" rows="5" placeholder="Place your message here ..." required="required" minlength="10" id="Message" ></textarea>
                </div> <!-- end div class form-group -->

                <button type="submit" class="btn btn-primary">Submit</button>
               </div> <!-- end div class col-lg-8 col-md-8 -->

            </div> <!-- end div class="col-lg-8 col-md-8" -->

           </form> <!-- end form -->

        </div> <!-- end div class contact-form-info -->

    </div><!-- end container -->
  </div>  <!-- end div class contact-info id=contact -->

  <div class="viedecontainer" id="video">
     <div class="embed-responsive embed-responsive-16by9">
       <iframe width="560" height="315" src="https://www.youtube.com/embed/LISBVqL6wGA?rel=0&amp;controls=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
     </div><!-- end responsive embed -->
   </div><!-- end container -->


<!-- ********************************* -->
<!--              FOOTER               -->
<!-- ********************************* -->


<footer class="footer">

  <div class="container">

          <!-- Twitter button code -->
      <a href="https://twitter.com/mrhwebdev?ref_src=twsrc%5Etfw" class="twitter-follow-button" data-size="large" data-show-count="false">Follow @mrhwebdev</a><script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

      <!-- Facebook Like button code -->
       <!--<div class="fb-like footer-element"
         data-href="http://youthful-borg-bcd031.bitballoon.com/"
         data-layout="button"
         data-action="like"
         data-size="large"
         data-show-faces="false"
         data-share="false">-->

      <div class="fb-like footer-element"
        <div class="fb-like" data-href="http://http://stoic-wing-510d47.bitballoon.com/" data-width="47" data-layout="button" data-action="like" data-size="large" data-show-faces="false" data-share="false">
      </div>
       </div> <!-- End Facebook Like button code -->

      <div class="footer-element">&copy; MRH Web Development, Inc. 2018</div>

 </div><!-- end container footer -->

</footer><!-- end footer -->

    <!-- ============================= -->
  <!-- All your JavaScript comes now -->
  <!-- ============================= -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <!-- Bootstrap core JS -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.7/js/bootstrap.min.js"></script>

  <script src="bootstrap/js/bootstrap.min.js"></script>

  <!-- Can place script tags with JavaScript files here -->
    <script src="js/jquery-3.2.1.min.js"></script>

  <!-- Smooth Scrolling-->

 <script type="text/javascript">
      var $root = $('html, body');
      $('.navbar-nav a').click(function() {
        var href = $.attr(this, 'href');
        if (href != undefined && href != '#') {
          $root.animate({
            scrollTop: $(href).offset().top
          }, 500, function () {
            window.location.hash = href;
          });
        }
        return false;
      });
    </script>
<!-- End Smooth Scrolling-->


    <script>
    $('.dropdown-toggle').dropdown()
    </script>


  </body>
</html>
styles.css


/**************************************************************/
/******************Navbar, Buttons, Elements *****************/
/**************************************************************/
/***** Navigation bar ****/
/********************************
.nav ul li {
   display: inline-block;
   padding: 10px 15px 5px;
   text-align: center;
  	color: #white;
   font-weight: bold;
}
.nav {
	 z-index: 1;
   background-color: black;
	 color: #faebd7;
   position: fixed;
   width: 100%;
   top: 0;
   text-transform: uppercase;
   text-align: center;
   font-size: 1.5em;
   font-weight: bold;
   letter-spacing: 0.05em;
/* Properties of the navigationbar, included fonts*/
/********************************
}
.nav a:hover {
  color: #ff0;
  text-decoration: none;
  transition: color 600ms;
  -webkit-transition: color 600ms;
 /* change the colorr of the navigationbar when the mouse is on */
     /********************************
}
nav a {
	text-transform: uppercase;
	text-decoration: none;
	color: #faebd7;
	letter-spacing: 1px;
	margin-right: 10px;
	 text-align: right;
}*/



/***********************
      Navbar
************************/

.projectName {
  text-transform: uppercase;
}

.projectName a {
  color: white;
}


/***********************
      Home Page
************************/

body {
  background-color: #fffeea;
  background-attachment: fixed;
	position: relative;
	font-family: Verdana, Helvetica, Arial, sans-serif;
}

.container {
  margin: 0 auto;
  width: 100%;
}

.header {
  text-align: center;
}

.header h1 {
	margin-bottom: 40px;
	text-align: center;
}

.anchor {
  padding-top: 50px;
}

/*****Carousel******/

.carousel {
  margin-left: -15px;
  margin-right: -15px;
}

.carousel-inner{
  background-position: center center;
  background-repeat: no-repeat;
  background-size: 100%;
	height: 70%;
	color: #white;
	font-size: 30px;
	font-weight: bold;
	height: 100vh
  padding-bottom: 20px;
}

.carousel-caption h3 {
  color: #fff
}

.carousel-inner img {
  width: 100%;
  height: calc( 100vh - auto);
  color: #468499;
}


/***********************
      WORK
************************/


#work {
  margin-top: 20px;
}

.work {
  padding-top: 86px;
}

.row {
  padding-left: 20px;
}

.work-img {
  display: block;
  margin: auto;
  max-width: 200px;
  position: relative;
  padding-bottom: 20px;
}

#work h1 {
  font-size: 1.5em;
  text-align: center;
  margin-bottom: 40px;
  font-weight: bold;
}
.work2 {
  padding-top: 86px;
  padding-bottom: 50px;
  margin-top: 40px;
  margin-bottom: 20%;
}

#work2 img {
  display: block;
  margin: auto;
  max-width: 50px;
  position: relative;
  float: left;
  padding-top: 30px;
}

#work2 h2 {
  font-size: 1.5em;
  padding-top: 40px;
  margin-top: 10px;

}

	/***********************
	      ABOUT ME
	************************/

.about {
  background-attachment: fixed;
   /*Give the background a fixed position (it doesn´t scroll when you scroll*/
  background-size: cover;
   /*Have the background cover the entire div section*/
  background-repeat: no-repeat;
	background-position: center;
  padding-bottom: 100px;
  padding-top: 70px;
	padding-right: 20px;
	padding-left: 20px;
	text-align: center;
}

.main-text {
  padding-top: 40px;
  clear: both;
	font-size: 1.2em;
}

.main-text h3 {
  padding-top: 10px;
	font-size: 1.3em;
}

.image img {
  width: 50%;
}

.concept {
  text-align: center;
}

.intro {
  padding-top: 10px;
  font-size: 1.5em;
}

.skill-list {
  margin-left: 0px;
	font-family: Verdana, Helvetica, Arial, sans-serif;
  font-size: 1.7em;
	text-align: left;
	padding-right: 10px;
}

.skills {
  text-align: left;
}

.skills h3 {
  text-align: left;
  font-family: Verdana, Helvetica, Arial, sans-serif;
  font-size: 2em;
  padding-top: 10px;
	padding-left: 20px;
}

/***********************
      FAQ
************************/

.faq {
  text-align: left;
	margin-bottom: 30px;
	padding-top: 30px;
	font-family: Times, Arial, sans-serif;
  font-size: 1.5em;
	color: #468499;
	 /* properties of FAQ body */
}

#faq h1 {
  font-size: 1em;
}

#faq {

  padding-top: 50px;
  padding-bottom:50
  height: 400px;
}
/**** End FAQ page ****/


/***********************
      CONTACT
************************/
.contact {
  text-align: left;
  padding-top: 10px;
  font-family: Times, Arial, sans-serif;
  font-size: 1em;
  color: #468499;
}

#contact h1 {
  font-size: 2em;
  text-align: left;
  margin-bottom: 10px;
  margin-top: 1px;
  font-weight: bold;
}

#contact h6 {
  font-size: 1.6em;
  text-align: left;
  margin-bottom: 5px;
  margin-top: 10px;
  font-weight: bold;
  color: #468499;
}

.contact Phone {
  text-align: left;
  float; left;
}


 /*Parallax Effect: make the background images and website content scroll at different rates */
#contact {
  background-image: url("../img/compu4.jpg");
  /*Add a background image*/
  background-attachment: fixed;
  /*Give the background a fixed position does it not scroll when you scroll*/
  background-size: cover;
  /*Have the background cover the entire div section*/
  color: black;
  /*Change the color of the text on top so it is readable and adjust the padding as needed.*/
  padding-top: 60px;
  padding-bottom:40
  height: 400px;
}
 /*End Parallax Effect*/

/**** End Contact page ****/

.form-control {
	width: 80%;
}
/***********************
         VIDEO
************************/

#video {
  position: relative;
  padding-bottom: 20%;
  padding-top: 30px;
  padding-left: 30%;
  padding-right: 30%;
  margin-left: 50px;
  margin-right: 50px;
  height: 0;
  overflow: hidden;
}

/***********************
         FOOTER
************************/

.footer {
  padding: 50px 10px 50px;
  color: rgb(255, 255, 255);
  background-color: #222831;
  text-align: center;
  height: 50px;
  width: 100%;
}



/* Typography */

h1,
h2,
h3,
h4,
h5 {
	font-family: Verdana, Helvetica, Arial, sans-serif;
	color: #34495e;
	font-size: 1.8em;
}
@gyetman
 



