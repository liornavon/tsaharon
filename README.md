<html> 
<head>
    <title>Greeting Message</title> 
    <style>
#lbl {
    font-family: monospace;
    font-size: xx-large;
    color: #626262;
    padding: 5px;
    border: 1px solid #ececec;
    text-align: center;
    line-height: 1.5;
    height:85%


}
#date{
    font-size:large;
}
body{
    background-color: aliceblue;
}
    </style>
</head>
<body>
    <div id="lbl"></div>
</body>

<script>
    var weekday = new Array(7);
    weekday[0] = "ראשון";
    weekday[1] = "שני";
    weekday[2] = "שלישי";
    weekday[3] = "רביעי";
    weekday[4] = "חמישי";
    weekday[5] = "שישי";
    weekday[6] = "שבת";

    
    var today = new Date();
    var hrs = today.getHours();
    var dayOfWeek = weekday[today.getDay()];
    var date = dayOfWeek+" " + today.getDate() + "/" +(today.getMonth()+1) +'/'+today.getFullYear()  ;

    var greet;

    if (hrs < 12)
        greet = 'בוקר טוב  ';
    else if (hrs >= 12 && hrs <= 17)
        greet = 'צהריים טובים ';
    else if (hrs >= 17 && hrs <= 24)
        greet = 'ערב טוב  ';

    document.getElementById('lbl').innerHTML =
        greet+= "צהרון דמוקרטי " `<div id="date"> It's ${date}</div>`;
</script> 
</html>
