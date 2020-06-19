# group-an-array-of-associative-arrays-by-key-in-PHP
How to group an array of associative arrays by key in PHP

```php 



<?php

/**
 * Function that groups an array of associative arrays by some key.
 * 
 * @param {String} $key Property to sort by.
 * @param {Array} $data Array that stores multiple associative arrays.
 */
function group_by($key, $data) {
    $result = array();

    foreach($data as $val) {
        if(array_key_exists($key, $val)){
            $result[$val[$key]][] = $val;
        }else{
            $result[""][] = $val;
        }
    }

    return $result;
}


```


# Convert object to array 

```php

public  function object_to_array($data)
{
    if (is_array($data) || is_object($data))
    {
        $result = array();
        foreach ($data as $key => $value)
        {
            $result[$key] = $this->object_to_array($value);
        }
        return $result;
    }
    return $data;
}


```
