# EXP 09 - BIRTHDAY CARD

## AIM:

To create a Birthday card using HTML and CSS

## SOFTWARE:

Visual Studio Code.

## ALGORITHM:

1. Set up the basic structure of your HTML document and include the CSS stylesheet.

2. Design the layout of your birthday card using HTML elements such as < div >, < h1 >, < p >, < img >, and < span >. 

3. Add a container < div > to hold the entire birthday card content.
  
4. Use paragraph tag to disply the personalised greeting. Add an image element to display a birthday-themed image.

## PROGRAM:


### HTML PROGRAM FOR FRONT PAGE

```java

<!DOCTYPE html>
<head>
    <title>BIRTHDAY CARD</title>
</head>
<body  style = "background: #DCE35B; 
background: -webkit-linear-gradient(to right, #45B649, #DCE35B); 
background: linear-gradient(to right, #45B649, #DCE35B);">
    <div style="border:5px solid rgb(242, 104, 127);margin-top:80px;margin-left: 150px;margin-right: 150px; padding-bottom:300px;font-size:40px;background-color:#12192c;">
        <img src="download.jpeg" style="float:right;padding-TOP: 50px;padding-right: 80PX;" alt="Photo" width="750" height="750">
        <BR>
        <P align="center"><font color="#45B649">&emsp;<BR>HAPPY&emsp;</font></P>
        <P align="center"><font color="#45B649">&emsp;BIRTHDAY&emsp;</font></P>
        <P align="center"><font color="#45B649">&emsp;BROOO!&emsp;</font></P>
        <P align="center"><font color="#45B649">&emsp;I HAVE A SUPRISE FOR U CLICK <BR>THE BELOW BUTTON &emsp;</font></P>
            <CENTER>
        <DIV style="float:left;padding-TOP: 200px;padding-right: 80PX;padding-left: 220PX;padding-bottom: 150PX;">
            </CENTER>
<button><a href = "http://127.0.0.1:5500/2.html"><img src="images.png" alt="Photo" width="50" height="50"></a></button>
        </DIV>
        <p></p>
    </div>
</body>
       
```

### HTML PROGRAM FOR INSIDE PAGE

```java

<!DOCTYPE html>
<html lang="en">
<head>
    <title>card</title>
    <link rel="stylesheet" href="2.css">
</head>
<body>
</body>
</html>
<div class="birthdayCard">
    <div class="cardFront">
      <div class="front-text">
      <h3 class="happy">HAPPY</h3>
      <h2 class="bday">BIRTHDAY</h2> 
      <h3 class="toyou">to you BROO!</h3>  
      </div>
      <div class="wrap-deco">
    <div class="decorations"></div>
    <div class="decorationsTwo"></div>
      </div> 
        <div class="wrap-decoTwo">
    <div class="decorations"></div>
    <div class="decorationsThree"></div>
      </div>
      <div class="plate">
        <div class="cake"></div>
        <div class="flame"></div>
      </div>
    </div>  
      <div class="cardInside">
         <div class="inside-text">
      <h3 class="happy">HAPPY</h3>
      <h2 class="bday">BIRTHDAY</h2> 
      <h3 class="toyou">BROOO!</h3>  
      </div>
        <div class="wishes">
        <p>Dear FRND ,</p>
        <p>Happy birthday!! I wish u always stay happy and with ur loved one dont worry babe i always here to torture u love you </p>
        <p class="name">by<br>moni</p>
        </div>
      </div>
    </div>
    
```

### CSS PROGRAM FOR INSIDE PAGE

```java

body {
    
    display: flex;
    align-items: center;
    justify-content: center;
    height:100vh;
    background-color: #00f9ae;
  }
  .birthdayCard {
    position: relative;
    width: 250px;
    height:350px;
    cursor: pointer;
    transform-style: preserve-3d;
      transform: perspective(2500px);
    transition: 4s;
  }
  
  .birthdayCard:hover {
      transform: perspective(2500px) rotate(5deg);
      box-shadow: inset 100px 20px 100px rgba(0,0,0,.15), 0 10px 100px rgba(0,0,0,0.3);
  }
  
  .birthdayCard:hover .cardFront {
    transform: rotateY(-160deg); 
  }
  
  .birthdayCard:hover .front-text {
    display: none;
  }
  
  .birthdayCard:hover .wrap-deco {
    display: none;
  }
  
  .birthdayCard:hover .wrap-decoTwo {
    display: none;
  }
  
  .birthdayCard:hover .plate {
    display: none;
  }
  .cardFront {
    position: relative;
    background-color: #f3ccfa;
    width: 250px;
    height:350px;
    overflow: hidden;
    transform-origin: left;
    box-shadow: inset 100px 20px 100px rgba(0,0,0,.13), 30px 0 50px rgba(0,0,0,0.1);
    transition: .4s;
  }
  
  .happy, .toyou {
    position: relative;
    font-family: didot;
    text-align: center;
    backface-visibility: hidden;
    font-size: 30px; 
  }
  
  .happy {
    top:198px;
  }
  
  .toyou {
    top:123px;
  }
  
  .bday {
    position: relative;
    font-family: arial;
    font-size: 35px;
    text-align: center;
    top:163px;
  }
  
  .wrap-deco {
    position: absolute;
    top:-230px;
    left:-200px;
  }
  
  .decorations {
    position: absolute;
    width: 400px;
    height: 300px;
    border: 3px solid #333;
    border-radius: 50%;
  }
  
  .decorations:before, .decorations:after, .decorationsTwo:before, .decorationsTwo:after, .decorationsThree:before, .decorationsThree:after {
    content:"";
    position: absolute;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    width:0;
    height:0;
  }
  
  .decorations:before {
    border-top: 40px solid #f15bb5;
    top:297px;
    left:210px;
    transform: rotate(-5deg);
  }
  
  .decorations:after{
    border-top: 40px solid #f4d35e;
    top:288px;
    left:260px;
    transform: rotate(-17deg);
  }
  
  .decorationsTwo:before {
    border-top: 40px solid #00f5d4;
    top:268px;
    left:315px;
    transform: rotate(-30deg);
  }
  
  .decorationsTwo:after, .decorationsThree:after {
    border-top: 40px solid #9b5de5;
    top:238px;
    left:355px;
    transform: rotate(-40deg);
  }
  
  .wrap-decoTwo {
    transform: scaleX(-1);
    position: absolute;
    top:-230px;
    left:445px; 
  }
  
  .decorationsThree:before {
    border-top: 40px solid #00bbf9;
    top:268px;
    left:315px;
    transform: rotate(-30deg);
  }
  
  .plate {
    position: absolute;
    width: 130px;
    height: 5px;
    background-color: #00bbf9;
    left:60px;
    top:213px;
  }
  
  .cake {
    position: absolute;
    overflow: hidden;
    width:100px;
    height: 50px;
    background-color: #f15bb5;
    border-radius: 10px 10px 0 0;
    top:-50px;
    left:15px;
    box-shadow: inset 0 -15px #f9c74f, inset 0 15px #432818;
  }
  
  .cake:before {
    content:"";
    position: absolute;
    background-color: #432818;
    width:10px;
    height:20px;
    top:5px;
    border-radius:20px;
    box-shadow: 10px 5px #f15bb5, 20px 0px #432818, 30px 2px #f15bb5, 40px 5px #432818, 50px 5px #f15bb5, 60px 0px #432818, 70px 5px #f15bb5, 80px 5px #432818, 90px 5px #f15bb5;
  }
  
  .plate:before {
    content:"";
    position: absolute;
    background: repeating-linear-gradient(-45deg, #9b5de5, #9b5de5 3px, #00f5d4 3px, #00f5d4 6px);
    width:7px;
    height: 25px;
    top:-75px;
    left:61px;
  }
  
  .plate:after {
    content:"";
    position: absolute;
    width:1px;
    height: 5px;
    background-color: #333;
    top:-80px;
    left:64px;
  }
  
  
  .flame {
    position: absolute;
    background-color: #fb5607;
    border-radius: 80% 0 55% 50% / 55% 0 80% 50%;
    transform: rotate(-45deg);
    width:15px;
    height:15px;
    opacity:0.7;
    top:-93px;
    left:57px;
  }
  .cardInside {
    position: absolute;
    background-color: #f3ccfa;
    width: 250px;
    height:350px;
    z-index:-1;
    left:0;
    top:0;
    box-shadow: inset 100px 20px 100px rgba(0,0,0,0.2);
  }
  
  .inside-text {
    position: relative;
    top:-160px;
    transform: scale(0.7);
  }
  
  .wishes {
    position: relative;
    top:-100px;
    margin: 25px;
  }
  
  p {
    font-family: 'Brush Script MT', cursive;
    color: #333;
  }
  
  .name {
    margin-left:150px;
  }
  
  ```
  
  ## OUTPUT 
  
  ### FRONT - PAGE 
  
  <img width="1280" alt="image" src="https://user-images.githubusercontent.com/93427240/230823280-c01f218d-c656-488b-9d82-8efa6c04fe1d.png">

  ### INSIDE - PAGE
  
  <img width="1199" alt="image" src="https://user-images.githubusercontent.com/93427240/230823553-fd3a1b2c-4075-4b49-bf7f-f27715a4043c.png">
  
  ## RESULT:
  
  So, a birthday card is created using CSS and HTML.
