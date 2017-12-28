# Christmas-hack-CTF

```
<html>
<head>
<title>Christmas hack</title>
<style>
body {
    background-image: url("https://christmaswebmaster.com/wp-content/uploads/2012/09/christmas-background-tiles170.png");
    background-repeat: repeat;

}
</style>
<?php
  $c = 'This little hacker has been naughty';
  $c = str_rot13($c);
  $c = base64_encode($c);
  setcookie("Santa", $c);
?>
</head>
<body>
</body>
<center>
        <img src="https://vignette.wikia.nocookie.net/glee/images/8/8a/Christmas-present-01.png/revision/latest?cb=20131125004106">
        <br><br>
        <?php
                $c = base64_decode($_COOKIE['Santa']);
                $c = str_rot13($c);
                if($c === "This little hacker has been naughty")
                {
                        print '<h2 style="color:white;">Just <u><i style="color:#00ffff";>nice</i></u> hackers gets a Christmas present</h2>>';
                        die();
                }
                if($c === "This little hacker has been nice")
                {
                        print '<h3 style="color:white;">Jay, you seems like one of the nice guys, here is the flag:<br><br>flag{chr157m45_c4rd_fr0m_4_h00k3r_1n_m1nn34p0l15}<br><br>And merry christmas!</h3>';
			print '<iframe width="560" height="315" src="https://www.youtube.com/embed/mxVo5mjK4eg" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>';
			die();
                }
                else
                {
                        print '<h3 style="color:white;">Merry christmas!</h3>';
                        die();
                }
        ?>
</center>
</html>

```
