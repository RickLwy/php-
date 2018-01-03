<?php
function pd($pm1, $pm2 = 'aaaaa2', $pm3 = 'bbbbb3', $pm4 = 'ccccc4', $pm5 = 'ddddd5')
{
    header("Content-type: text/html; charset=utf-8");
    echo '<div style="color: red">-----------------参数1打印--------------------</div>';
    echo '<hr>';
    echo '<pre>';
    dump($pm1);
    echo '</pre>';
    if ($pm2 != 'aaaaa2') {
        echo '<hr>';
        echo '<div style="color: red">-----------------参数2打印--------------------</div>';
        echo '<hr>';
        echo '<pre>';
        dump($pm2);
        echo '</pre>';
    }
    if ($pm3 != 'bbbbb3') {
        echo '<hr>';
        echo '<div style="color: red">-----------------参数3打印--------------------</div>';
        echo '<hr>';
        echo '<pre>';
        dump($pm3);
        echo '</pre>';
    }
    if ($pm4 != 'ccccc4') {
        echo '<hr>';
        echo '<div style="color: red">-----------------参数4打印--------------------</div>';
        echo '<hr>';
        echo '<pre>';
        dump($pm4);
        echo '</pre>';
    }
    if ($pm5 != 'ddddd5') {
        echo '<hr>';
        echo '<div style="color: red">-----------------参数5打印--------------------</div>';
        echo '<hr>';
        echo '<pre>';
        dump($pm5);
        echo '</pre>';
    }
    die;
}
function dump($data)
{
    if (is_object($data) || is_array($data)) {
        print_r($data);
    } else {
        var_dump($data);
    }
}
pd(array(1,2,3),222,3,4,false);
