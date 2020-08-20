# php_landing_page_project
Web students: get ready for “Landing Page” walkthrough webinar! Download This 


# steps:
1. download the project folders.
2. Download Laragon.
3. open laragon app and click on Start All
4. wait then open browser enter this url localhost/phpmyadmin
5. user = root , password =  no password to login, leave it empty
6. on the left menu click on new enter the name must be landing_page_project
7. wait then click on import the select the landing_page_project.sql and wait
8. then we finish database setup and creation and add items to it move to C folder
8. open laragon folder inside the C (windows).
9. open www folder inside laragon folder.
10. extract the project zip inside www make sure the folder name landing
11. now we have life data base and life server lets check the app on the localhost
12. make sure to name the proejct folder landing or the same name we gonna visit localhost/landing
13. after we finish the js code we going to copy the js code inside app.js and we did it



## like this

```
<!-- header info and body -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Manipulating the DOM</title>
  <!-- Load Google Fonts -->
  <link href="https://fonts.googleapis.com/css?family=Fira+Sans:900|Merriweather&display=swap" rel="stylesheet">  <!-- Load Styles -->

  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <!-- HTML Follows BEM naming conventions 
  IDs are only used for sections to connect menu achors to sections -->
  <header class="page__header">
    <nav class="navbar__menu">
      <!-- Navigation starts as empty UL that will be populated with JS -->
      <ul id="navbar__list"></ul>
    </nav>
  </header>
  <main>
    <header class="main__hero">
      <h1>Landing Page </h1>
    </header>
    <!-- Each Section has an ID (used for the anchor) and 
    a data attribute that will populate the li node.
    Adding more sections will automatically populate nav.
    The first section is set to active class by default -->
    

	 
<!-- php code here stati -->
	   
	       <?php 
	 global $con;
	 
	 
	$query = "SELECT * FROM sections ";
    $res = mysqli_query($con, $query);


    while ($row = mysqli_fetch_assoc($res)) {
	 $section_id = $row['id'];
	 $section_title = $row['name'];
	 $section_deatlis = $row['details'];


    
    ?>
    
    <!-- HTML area here we add only 1 secions -->
    
    <section id="<?php echo 'section' . $section_id . '"' ?> data-nav="Section 1" class="your-active-class">
      <div class="landing__container">
        <h2><?php echo $section_title ?></h2>
        <p><?php echo $section_deatlis; ?></p>
      </div>
    </section>
    
    
    
    
    <?php      
         }
    
    ?>
   
  </main>
  <footer class="page__footer">
    <p>&copy Udacity</p>
  </footer>
  

  

<script src="app.js"></script>
```


