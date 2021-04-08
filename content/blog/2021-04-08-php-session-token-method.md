---
title: php session token
date: 08-04-2021
category: Php
---



###php

```php+HTML
<?php

$_SESSION[“token”] = sha1(rand());
echo'<a href="abc.php?giris=dogru&token=.'$_SESSION["token"]."';
abc.php dosyasındaki session kontrolü ise şu şekilde olmalıdır:
?>

<?php

    if($_GET[“giris”]==dogru){

    if(isset($_GET[“token”])&&$_GET[“token”]==$_SESSION[“token”])
    {
	    session_start();//Dogruysa oturumu baslat
    }       
    else
    {
        echo “token yanlış!”;
    }

}
?>
```

