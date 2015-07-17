--------------------------------------------------------------------------------------
1. SASS is updated automatically from .sass-cache
Change 
	@import "bower_components/bootstrap-sass/assets/stylesheets/_bootstrap.scss";
To 
	@import "../../bower_components/bootstrap-sass/assets/stylesheets/_bootstrap.scss";

Solution:
Remove .sass-cache and run grunt serve again

--------------------------------------------------------------------------------------
2. Add spacing to sprite image with Compass
http://www.codechewing.com/library/automatically-generate-css-sprites-with-sass/

add 
	$grey-icon-spacing: 10px;
before
	@import "grey-icon/*.png";

+ Add width, height to icons image css
$icons-sprite-dimensions: true;
--------------------------------------------------------------------------------------
3. Extend an icon from sprite
http://www.codechewing.com/library/automatically-generate-css-sprites-with-sass/

.my-cart-blue-icon-extended {
  @include grey-icon-sprite(cart-blue);
}

4. If you just want your layout to stretch to 100% height of the browser

<<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>
	<div class="wrapper"></div>
</body>
</html>

html, body {
	width: 100%;
	height: 100%;
}

.wrapper {
	min-height: 100%;
}