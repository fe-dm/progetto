<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, i
nitial-scale=1.0">
<title>Guitar GIF Background with Dropdown Menu</tit
le>
<style>
/* Full-screen background gif */
body {
margin: 0;
padding: 0;
height: 100vh;
background: url('https://media4.giphy.com/me
dia/v1.Y2lkPTc5MGI3NjExdzB1cTg5ZnhtN3d1YWxpOXhsNzJibGdma
3A5M2k5OGh4MG5oeGV4ZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY
3Q9Zw/hPlsN9Z6JNF4s/giphy.gif') no-repeat center center
fixed;
background-size: cover;
font-family: Arial, sans-serif;
color: white;
display: flex;
justify-content: center;
align-items: center;
}
/* Navbar styling */
nav {
background-color: rgba(0, 0, 0, 0.7);
padding: 15px 0;
border-radius: 8px;
}
/* Navbar container - Centering */
.navbar {
list-style-type: none;
margin: 0;
padding: 0;
text-align: center;
}
.navbar li {
position: relative;
display: inline-block;
padding: 10px 20px;
cursor: pointer;
text-align: center;
}
.navbar a {
color: white;
text-decoration: none;
display: block;
}
.navbar li:hover {
background-color: rgba(255, 255, 255, 0.2);
}
/* Dropdown menu */
.dropdown {
position: absolute;
display: none;
top: 40px;
left: 0;
background-color: rgba(0, 0, 0, 0.7);
list-style-type: none;
padding: 0;
margin: 0;
}
.dropdown li {
padding: 10px;
cursor: pointer;
}
.dropdown li:hover {
background-color: rgba(255, 255, 255, 0.2);
}
/* Show dropdown on hover */
.navbar li:hover .dropdown {
display: block;
}
/* Home Button styling */
.home-btn {
padding: 10px 20px;
text-decoration: none;
color: white;
background-color: rgba(0, 0, 0, 0.7);
border-radius: 5px;
cursor: pointer;
}
/* Page content */
.content {
display: none;
padding: 100px 20px;
text-align: center;
background-color: rgba(0, 0, 0, 0.5);
margin-top: 50px;
border-radius: 8px;
}
/* Active page content */
.active {
display: block;
}
</style>
</head>
<body>
<!-- Navbar -->
<nav>
<ul class="navbar">
<li><a href="javascript:void(0);" class="home-btn" onclick="showPage('home')">Home</a></li>
<li>
Page 1
<ul class="dropdown">
<li><a href="javascript:void(0);" on
click="showPage('page1-1')">Subpage 1</a></li>
<li><a href="javascript:void(0);" on
click="showPage('page1-4')">Subpage 4</a></li>
<li><a href="javascript:void(0);" on
click="showPage('page1-2')">Subpage 2</a></li>
</ul>
</li>
<li><a href="javascript:void(0);" onclick="s
howPage('page2')">Page 2</a></li>
<li><a href="javascript:void(0);" onclick="s
howPage('page3')">Page 3</a></li>
</ul>
</nav>
<!-- Content for Page 1, Page 2, Page 3 -->
<div id="home" class="content active">
<h2>Welcome to the Home Page</h2>
<p>This is the home page content.</p>
</div>
<div id="page1-1" class="content">
<h2>Page 1 - Subpage 1</h2>
<p>Content for Page 1, Subpage 1.</p>
</div>
<div id="page1-4" class="content">
<h2>Page 1 - Subpage 4</h2>
<p>Content for Page 1, Subpage 4.</p>
</div>
<div id="page1-2" class="content">
<h2>Page 1 - Subpage 2</h2>
<p>Content for Page 1, Subpage 2.</p>
</div>
<div id="page2" class="content">
<h2>Page 2</h2>
<p>Content for Page 2.</p>
</div>
<div id="page3" class="content">
<h2>Page 3</h2>
<p>Content for Page 3.</p>
</div>
<script>
function showPage(pageId) {
// Hide all content
const contents = document.querySelectorAll
('.content');
contents.forEach(content => content.classLis
t.remove('active'));
// Show selected content
const page = document.getElementById(pageI
d);
if (page) {
page.classList.add('active');
}
}
</script>
</body>
</html>
