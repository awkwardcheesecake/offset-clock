function startTime(offset)
{
	var offsetString = new Date( new Date().getTime() + offset * 1000).toUTCString().replace( / GMT$/, "" );

	var today= new Date(offsetString);


	var h=today.getHours();
	var m=today.getMinutes();
	var s=today.getSeconds();
	var ampm = "am";
	var hd = h; // the display of h. Used for 12 hour time format
	if (h > 12){
		ampm = "pm";
		hd = h-12;
	}
	// add a zero in front of numbers<10
	m=checkTime(m);
	s=checkTime(s);
	document.getElementById("clockTxt").innerHTML=hd+":"+m+":"+s+" "+ampm;
	t=setTimeout(function(){startTime(offset)},500);
}

function checkTime(i)
{
	if (i<10) {
		i="0" + i;
	  }
	return i;
}
