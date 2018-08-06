# nocopy

<!DOCTYPE html>
<html>
<head>
	<title>not to copy</title>
	<style type="text/css">
		.disablecopypaste {
 -webkit-user-select: none; Chrome/Safari/Opera 
 -moz-user-select: none; Firefox

-ms-user-select: none; Internet Explorer/Edge

-webkit-touch-callout: none; iOS Safari}
	</style>
	<script src="jquery.min.js"></script>
<script type="text/javascript">
$(document).ready(function () {
    //Disable full page
    $("body").on("contextmenu",function(e){
        return false;
    });
    
    //Disable part of page
    $("#id").on("contextmenu",function(e){
        return false;
    });
});
function disableselect(e){
	return false
} 
function reEnable(){
	return true
} 
//if IE4+
document.onselectstart=new Function ("return false") 
//if NS6
if (window.sidebar){
document.onmousedown=disableselect
document.onclick=reEnable
}
</script>
</head>
<body>
	<p class="disablecopypaste">
 these contents can’t be copied.
</p>
</body>
</html>
