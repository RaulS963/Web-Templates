# Web-Templates

**Important Bootstrap and Jquery links**
```html
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
```
----

## [fa fa-icons](https://fontawesome.com/v4.7.0/icons/)
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
```


## Responsive Navbar
Responsive bootstrap navbar. collapse when screen size is small.
```html
<div class="navbar-content">
                <nav class="navbar navbar-inverse">

                    <div class="container-fluid">
                        <div class="navbar-header">
                            <a class="navbar-brand" href="#"><span style="font-family:'cursive',font-size:'25px'">picto</span></a>
                            <div class="nav-bar-toggle-btn">
                                <button class="navbar-toggler" data-toggle="collapse" data-target="#collapse_target" style=" background-color: 'Transparent', border: '0px' ">
                                    <span class="glyphicon glyphicon-menu-hamburger" style="color: 'white', fontSize: '20px'"></span>
                                </button>
                            </div>
                        </div>
                        <div class="collapse navbar-collapse" id="collapse_target">
                            <ul class="nav navbar-nav">
                                <li ><a href="#">Home</a></li>
                                <li class="dropdown"><a class="dropdown-toggle" data-toggle="dropdown" href="#">Page 1 <span class="caret"></span></a>
                                    <ul class="dropdown-menu">
                                        <li><a href="#">Page 1-1</a></li>
                                        <li><a href="#">Page 1-2</a></li>
                                        <li><a href="#">Page 1-3</a></li>
                                    </ul>
                                </li>
                                <li><a href="#">Page 2</a></li>
                            </ul>
                            <ul class="nav navbar-nav navbar-right">
                                <li><a href="#"><span class="glyphicon glyphicon-user"></span> Sign Up</a></li>
                                <li><a href="#"><span class="glyphicon glyphicon-log-in"></span> Login</a></li>
                            </ul>
                        </div>

                    </div>

                </nav>
            </div>
```
CSS:
```css
.nav-bar-toggle-btn{
  padding-top: 15px;
  margin-right: 15px;
  float: right;
}
@media (min-width:768px){
  .nav-bar-toggle-btn{
    display: none;
  }
}
```
- - - -
