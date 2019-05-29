# Skill Refresh - Bootstrap 4 Introduction

## Create Project Structure

* Create myproject and myproject/src folder.
* Install Bootstrap
  * Go to https://getbootstrap.com, click _**Download**_ button, it will take us to Download page. 
  * Go ahead and click _**Donwload**_ button to download the compiled CSS and JS.
  * Extract the downloaded file, and move /css and /js folders into myproject/src folder.

* Prepare File Structure
  * Create a new empty style.css file in the src/css folder.
  * Create a new empty index.html file in the src folder.

* Prepare index.html for Bootstrap 4
  * Go to https://getbootstrap.com, click _**Get started**_ button, it will take us to Documentation page.
  * Look for _**Starter template**_ section, copy and paste the codes to the empty index.html file.
  * Remove the code \<h1>Hello, world!\</h1>
  * Add link to style.css, inside the \<head> section, after all \<link>, add
    ```
    <link rel="stylesheet" href="css/style.css">
    ```

* Install Font Awesome 5
  * Go to https://fontawesome.com, click _**Download**_ link, it will take us to Download page. Go ahead and click _**Free for Web**_ button to download the file.
  * Extract the downloaded file, move /css/all.css file to src/fontawesome/css folder, move /webfonts folder to src/fontawesome folder.
  * Add link to all.css, inside the \<head> section, after all \<link>, add
    ```
    <link rel="stylesheet" href="fontawesome/css/all.css">
    ```

* Download Background Image and Logo
  * Go to https://unsplash.com, 
    * search for an image you love, download and rename it to bg.jpg, and move it to src/img folder.
  * Go to https://www.freelogodesign.org, 
    * search for a logo you love, download and rename it to logo.png, and move it to src/img folder.

## Creating Our Page

* Add Background Image
  * In style.css, add
    ```css
    html, body {
        background: linear-gradient(rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25)), url(../img/bg.jpg) no-repeat center center fixed; 
        -webkit-background-size: cover;
        -moz-background-size: cover;
        -o-background-size: cover;
        background-size: cover;
    }
    ```

* Add Logo Image
  * In index.html, add _**logo**_ \<section> inside \<body>
    ```html
    <section id="logo">
        <div class="container">
            <div class="row">
                <div class="col-md-12 text-center">
                    <img src="img/logo.png" class="img-fluid"/>
                </div>
            </div>
        </div>
    </section>
    ```

  * Adjust the Logo position. In style.css, add
    ```css
    #logo img {
        padding-top: 20px;
    }
    ```

* Add Intro Text
  * In index.html, add _**intro**_ \<section> inside \<body>
    ```html
    <section id="intro">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <p>We're working hard, we'll be ready to launch in ...</p>
                </div>
            </div>
        </div>
    </section>
    ```
  * In style.css, add
    ```css
    #intro p {
        color: white;
        text-align: center;
    }
    ```

  * Go to https://fonts.google.com, search for font you love, click on the “+” sign, click on the notification “1 Family Selected” at the bottom. The notification will popup and show more information.
  * Find and copy the HTML code that link to font’s stylesheet, paste it to index.html file, inside the \<head> section, after all \<link>. Example here using “Baloo Bhai” font,
    ```html
    <link href="https://fonts.googleapis.com/css?family=Baloo+Bhai&display=swap" rel="stylesheet">
    ```
  * Find and copy the CSS code that specify the font family, paste it to style.css file inside the _**#intro p**_ section. Example here using "Baloo Bhai" font,
    ```css
    font-family: 'Baloo Bhai', cursive;
    ```
  * Adjust the font size. In style.css, inside the _**#intro p**_ section, add
    ```css
    font-size: 1.8em;
    ```

* Add Countdown Clock
  * In index.html, add _**counter**_ \<section> inside \<body> 
    ```html
    <section id="counter">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                </div>
            </div>
        </div>
    </section>
    ```

  * Go to https://github.com/rendro/countdown, click _**Clone or download**_ button, then click _**Download ZIP**_ button to download the file.
  * Extract the downloaded file, move /dest/jquery.countdown.min.js file to the src/js folder.
  * Goto https://github.com/rendro/countdown/blob/master/Readme.md, and look for _**Uber simple setup**_ section.
  * Find and copy HTML code that link to required javascripts, paste it to index.html file, at the line above \</body>, change the _**path/to/jquery.countdown.min.js**_ to _**js/jquery.countdown.min.js**_
    ```html
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
    <script type="text/javascript" src="js/jquery.countdown.min.js"></script>
    ```
  * Find and copy JavaScript code, paste it to index.html file, at the line above \</body>, inside \<script>\</script>, change the _**.yourCountdownContainer**_ to _**.countdown**_
    ```html
    <script>
        $(function() {
            $('.countdown').countdown({
                date: "July 1, 2085 08:00:00"
            });
        });
    </script>
    ```
  * Let the countdown message shown on page. In index.html, inside _**counter**_ \<section>, add
    ```html
    <section id="counter">
        ...
            <div class="col-md-12">
                <div class="countdown"></div>
            </div>
        ...
    </section>
    ```
  * In style.css, add
    ```css
    #counter .countdown {
        color: white;
        text-align: center;
    }
    ```
  * Go to https://fonts.google.com, search for font you love, click on the “+” sign, click on the notification “1 Family Selected” at the bottom. The notification will popup and show more information.
  * Find and copy the HTML code that link to font’s stylesheet, paste it to index.html file, inside the \<head> section, after all \<link>. Example here using “Stylish” font,
    ```html
    <link href="https://fonts.googleapis.com/css?family=Stylish&display=swap" rel="stylesheet">
    ```
  * Find and copy the CSS code that specify the font family, paste it to style.css file, inside the _**#counter .countdown**_ section. Example here using "“Stylish”" font,
    ```css
    font-family: 'Stylish', sans-serif;
    ```
  * Adjust the font size. In style.css, inside the _**#counter .countdown**_ section, add
    ```css
    font-size: 3em;
    ```
  * Adjust the margin to reduce the gap between the countdown and the text above it. In style.css, inside the _**#counter .countdown**_ section, add
    ```css
    margin: -15px 0 0;
    ```

* Add Social Icon
  * In index.html, add _**icons**_ \<section> inside \<body> 
    ```html
    <section id="icons">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <ul class="list-inline">
                    </ul>
                </div>
            </div>
        </div>
    </section>
    ```

  * Go to https://fontawesome.com, click “Icons” link, and it will take us to Icons page.
  * Search for “twitter”, click the twitter-square icon, and it will take us to the twitter-square detail page.
  * Find and copy the HTML code of the twitter-square icon, paste it to index.html file in the _**icons**_ \<section>. Add a _**fa-3x**_ class to the icon \<i> tag to increase the size. Add a hyperlink _**\<a>**_ to the twitter icon.
    ```html
    <section id=“icons”>
        ...
            <ul class="list-inline">
                <a href="http://www.twitter.com" target="blank"><li class="list-inline-item"><i class="fab fa-twitter-square fa-3x"></i></li></a>
            </ul>
        ...
    </section>
    ```

  * Similarly for other icons
    ```html
    <section id=“icons”>
        ...
            <ul class="list-inline">
                <a href="http://www.twitter.com" target="blank"><li class="list-inline-item"><i class="fab fa-twitter-square fa-3x"></i></li></a>
                <a href="http://www.facebook.com" target="blank"><li class="list-inline-item"><i class="fab fa-facebook-square fa-3x"></i></li></a>
                <a href="http://www.google.com" target="blank"><li class="list-inline-item"><i class="fab fa-google-plus-square fa-3x"></i></li></a>
                <a href="http://www.instagram.com" target="blank"><li class="list-inline-item"><i class="fab fa-instagram fa-3x"></i></li></a>
            </ul>
        ...
    </section>
    ```
  * In style.css, add
    ```css
    #icons {
        text-align: center;
    }
    
    #icons .fab {
        color: white;
        margin: 5px 15px;
    }
    ```

* Produce icons bouncing effect on hover
    * In style.css, inside _**#icons .fab**_ section, add
        ```css
        #icons .fab {
            ...
            position: relative;
            bottom: 0;
        }
        ```
    * Add class to each icon
        ```html
        <i class="fab twitter fa-twitter-square fa-3x"></i>
        <i class="fab facebook fa-facebook-square fa-3x"></i>
        <i class="fab google fa-google-plus-square fa-3x"></i><
        <i class="fab instagram fa-instagram fa-3x"></i>
        ```
    * In style.css, add
        ```css
        #icons .twitter:hover {
            color: #6cadde;
            bottom: 5px;
        }

        #icons .facebook:hover {
            color: #3b5998;
            bottom: 5px;
        }

        #icons .google:hover {
            color: #ea4335;
            bottom: 5px;
        }

        #icons .instagram:hover {
            color: #517fa6;
            bottom: 5px;
        }
        ```

* Add Signup Box
  * In index.html, add _**signup**_ \<section> inside \<body> 
    ```html
    <section id="signup">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                </div>
            </div>
        </div>
    </section>
    ```

  * Go to https://getbootstrap.com/docs/4.3/components/forms/, refer _**Inline forms**_ section
  * In index.html, inside _**signup**_ \<section>, add
    ```html
    <section id="signup">
        ...
            <div class="col-md-12">
                <form class="form-inline" role="form" method="post" action="#signup">
                    <input type="email" class="form-control form-control-sm" name="email" placeholder="enter your email">
                    <button type="submit" class="btn btn-signup btn-sm" name="submit" value="send">find out more</button>
                </form>
            </div>
        ...
    </section>
    ```

  * In style.css, add
    ```css
    #signup {
        text-align: center;
    }

    #signup .form-inline {
        display: block;
    }

    #signup .btn-signup {
        background-color: rgba(161, 186, 226, 0.5);
        color: white;
    }

    #signup .btn-signup:hover {
        background-color: rgba(37, 165, 82, 1);
    }
    ```

* Add Media Queries
  * To make UI presented responsively to different devices in portrait and landscape mode. In style.css, add
    ```css
    @media(max-width:768px), (max-height: 414px) {

        #intro p {
            font-size: 1.2em !important;
        }

        #counter .countdown {
            font-size: 2.0em !important;
        }

        #icons .fab {
            margin: 10px 0 0 !important;
            font-size: 2em;
        }

    }

    @media(max-width:768px) {
            
        #logo img {
            width: 50%;
        }

    }

    @media(max-height: 414px) {

        #logo img {
            width: 25%;
        }

    }
    ```

## Using PHP to Send Email 

* Prepare PHP file
  * Transform HTML file into PHP file, Save As… change filename from index.html to index.php
* Add PHP code
  * In index.php, at the top, before \<!doctype html>, add
    ```php
    <?php
        if (isset($_POST['submit'])) {
            $email = $_POST['email'];
            $from = 'your-app-email@gmail.com';
            $to = 'your-support-email@gmail.com';
            $subject = 'Email signup';
            $body = "Please sign me ($email) up to the mailing list";
            
            if (!$_POST['email']) {
                $emailError = 'Please enter a valid email address</div>';
            }
            
            if (!$emailError) {
                if (mail ($to, $subject, $body, "From: {$from}")) {
                    $result = 'thank you we\'ll keep you updated</div>';
                } else {
                    $result = 'sorry there has been an error, please try again</div>';
                }
            }   
        }
    ?>
    ```

  * In index.php, after the \</form>, add
    ```html
    <section id="signup">
        ...
            <div class="col-md-12">
                <form class="form-inline" role="form" method="post" action="#signup">
                    ...
                </form>
                <?php echo $emailError;?>
                <?php echo $result;?>
            </div>
        ...
    </section>
    ```

* Add Styling
   * Add bootstrap styling and fontawesome icon to the success and failure messages
        ```php
        if (!$_POST['email']) {
            $emailError = '<div class="text-danger"><i class="fa fa-exclamation-triangle" aria-hidden="true"></i> &nbsp;Please enter a valid email address</div>';
        }

        if (!$emailError) {
            if (mail ($to, $subject, $body, "From: {$from}")) {
                $result = '<div class="text-success"><i class="fa fa-check" aria-hidden="true"></i> &nbsp;thank you we\'ll keep you updated</div>';
            } else {
                $result = '<div class="text-danger"><i class="fa fa-exclamation-triangle" aria-hidden="true"></i> &nbsp;sorry there has been an error, please try again</div>';
            }
        }
        ```

## Setup Docker for Apache, PHP with SMTP Client

* Create a new empty _**Dockerfile**_ file in the myproject folder, add
    ```
    FROM php:7-apache

    RUN apt-get update
    RUN apt-get install -q -y ssmtp
    RUN echo "TLS_CA_File=/etc/ssl/certs/ca-certificates.crt" >> /etc/ssmtp/ssmtp.conf
    RUN echo "root=your-gmail-address@gmail.com" >> /etc/ssmtp/ssmtp.conf
    RUN echo "mailhub=smtp.gmail.com:587" >> /etc/ssmtp/ssmtp.conf
    RUN echo "AuthUser=your-gmail-address@gmail.com" >> /etc/ssmtp/ssmtp.conf
    RUN echo "AuthPass=your-gmail-app-password" >> /etc/ssmtp/ssmtp.conf
    RUN echo "UseTLS=YES" >> /etc/ssmtp/ssmtp.conf
    RUN echo "UseSTARTTLS=YES" >> /etc/ssmtp/ssmtp.conf
    RUN echo "FromLineOverride=YES" >> /etc/ssmtp/ssmtp.conf
    RUN echo "sendmail_path=ssmtp -t" >> /usr/local/etc/php/conf.d/php-ssmtp.ini

    COPY src/ /var/www/html/
    ```
* Run the command in the myproject folder to start the app
    ```
    $ docker build -t bootstrap-intro-app .
    $ docker run -p 80:80 -d —-name my-bootstrap-intro-app bootstrap-intro-app
    ```

* Open web browser, test http://localhost