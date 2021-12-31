# Welcome to my github page

Currently this only has a calculator to convert RPM and time on an exercise bike into distance, but maybe it'll have more in the future.

## RPM to Miles Converter

<form action="" method="post" id="rpm-calc">
 RPM:
 <input type="number" name="rpm" />
 Time in minutes:
 <input type="number" name="time" />
 <input type="submit" value="Submit" onClick="calcMiles()">
</form>

<script>
    function calcMiles() {
        var rpm = document.getElementById("rpm").value;
        var time = document.getElementById("time").value;
        var diameter = 18;

        var circumfrance = Math.Pi * diameter;
        var distance = time * circumfrance * rpm;

        var INCHES_IN_A_MILE = 63360;

        alert(distance / INCHES_IN_A_MILE)
    }
</script>
