# library

---


## php lang

### 1 function diff date time

```php
    
    <?php

    function datediff( $date1, $date2 )
    {
        $diff = abs( strtotime( $date1 ) - strtotime( $date2 ) );

      return array(
          "day"=>intval( $diff / 86400 ),
          "hours"=>intval( ( $diff % 86400 ) / 3600),
          "mins"=> intval( ( $diff / 60 ) % 60 ),
          "seconds" =>intval( $diff % 60 )
        );

    }

    // use
    var_dump(datediff( date('Y-m-d H:i:s'), "2018-03-05 18:11:44"));
 ```
