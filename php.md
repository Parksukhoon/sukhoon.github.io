

# PHP

[toc]

## 1) PHP의 원리

```html
<!doctype html>
<html>
  <body>
    2018-01-20 18:36:01
  </body>
</html>
```

```php+HTML
<!doctype html>
<html>
  <body>
    <?php
      echo date('Y-m-d H:i:s');
    ?>
  </body>
</html>
```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_principle.png)



html과 php의 가장 큰 차이점은, html은 정적인 반면 php는 동적이라는 점이다. 웹 브라우저는 php가 없는 순수한 html 코드만을 받을 수 있다(즉 php가 있는지 인지하지 못한다). php는 웹페이지를 찍어낼 수 있는(양산할 수 있는) 프로그래밍 능력을 가지고 있다.



## 2) PHP의 데이터 타입(숫자와 문자)

검색어 : php data types(PHP 공식문서 확인 가능)

php에서 숫자를 표현하는 방법과 연산하는 방법

```php+HTML
<!doctype html>
<html>
<body>
  <h1>Number & Arithmetic Operator</h1>
  <h2>1+1</h2>
  <?php
  echo 1+1;
  ?>
  <h2>2-1</h2>
  <?php
  echo 2-1;
 ?>
 <h2>2*2</h2>
 <?php
 echo 2*2;
 ?>
 <h2>4/2</h2>
 <?php
 echo 4/2;
 ?>
</body>
</html>
```

```php+HTML
<!doctype html>
<html>
<body>
  <h1>String & String Operator</h1>
<?php
echo "Hello \"w\"ord";
?>

<?php
echo "Hello 'w'ord";
?>

<?php
echo 'Hello "w"ord';
?>
  <h2>concatenation operator</h2>
  <?php
  echo "Hello "."world";
  ?>
  <h2>String length function</h2>
  <?php
  echo strlen("Hello world");
   ?>
</body>
</html>

```

/ escape을 통해서 ""을 표현할 수 있다.

큰 따옴표("") 안에서 ''를 살리거나, 반대로 작은 따옴표("")안에서 ""을 살릴 수 있다.

.을 통해서 문자열을 결합해서 하나의 문자열로 만들 수 있다(concatenation operator)

strle()을 통해서 몇 개의 문자열로 이루어져 있는지 확인할 수 있다. 단 공백을 포함한다(5 + 1 + 5).



## 3) PHP의 변수

```php+HTML
<!DOCTYPE html>
<html>
  <body>
    <h1>Variable</h1>

    <?php
    $a = 10;
    echo $a + 1;
    ?>
    
    <?php
    $name = "leezche";
    echo "Lorem ipsum dolor sit amet, consectetur ".$name." adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco ".$name." laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore egoing eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. by ".$name;
    ?>
  </body>
</html>

```



![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_variable.png)

변수명을 지정해주기 위해서는 앞에 $표시를 붙인다.

앞에 문자열이 있기 때문에 결합하기 위해 .을 추가해야 한다. ex. ".name." 저렇게 변수명을 통해서 하면, 나중에 이름만 바꾸거나 할 때 하나씩 들어가서 바꾸지 않아도 되는, 편리함을 누릴 수 있다.



## 4) PHP의 URL 파라미터

.php뒤에 ?name = sukhoon이라고 설정하는 방식을 통해서 접속 가능

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    안녕하세요. <?php echo $_GET['address']; ?>에 사시는
     <?php echo $_GET['name']; ?>님 
  </body>
</html>
```

안녕하세요. <?php echo $_get['name']; ?> 과 같이 표기.

입력값과 입력값을 구분하는 & 기호.

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>WEB</h1>
    <ol>
      <li><a href = "index.php?id=HTML">HTML</a></li>
      <li><a href = "index.php?id=CSS">CSS</a></li>
      <li><a href = "index.php?id=JavaScript">JavaScript</a></li>
    </ol>
    <h2>
      <?php
          echo $_GET['id'];
      ?>
    </h2>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.  
  </body>
</html>
```

 index.php에서 id 값에 따라서 각 제목을 클릭할 때, 본문의 이름이 바뀌도록 할 수 있다.

 아직 배우지 않았지만, <?php> 안에 있는 echo $_GET['id']; 코드 덕에 동적으로 자유롭게 변경이 가능하다.

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_parameter.png)`

## 5) PHP 함수의 사용

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>function</h1>
      <?php
      $str = "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.";
      echo $str;
       ?>
       <h2>strlen()</h2>
       <?php
       echo strlen($str);
        ?>
  </body>
</html>
```

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>function</h1>
      <?php
      $str = "Lorem ipsum dolor sit amet, consectetur adipisicing elit,

       sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident,

        sunt in culpa qui officia deserunt mollit anim id est laborum.";
      echo $str;
       ?>
       <h2>strlen()</h2>
       <?php
       echo strlen($str);
        ?>
        <h2>nl2br</h2>
        <?php
        echo nl2br($str);
         ?>
  </body>
</html>

```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\function.php.png)

코드에서 줄바꿈을 br 태그 없이 하면, 당연히 웹 페이지에는 반영이 되지 않는다. 하지만 php에서 nl2br을 이용하면 br 태그를 이용하지 않고도 그림 하단에 보이는 것처럼 줄바꿈이 반영됨을 알 수 있다. 뒤는 nl2br 태그가 없이 일반적인 경우에 출력되는 텍스트.

strlen()을 통해 ()안의 변수가 총 몇 글자인지 자동으로 카운트할 수 있다.



```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>WEB</h1>
    <ol>
      <li><a href="index.php?id=HTML">HTML</a></li>
      <li><a href="index.php?id=CSS">CSS</a></li>
      <li><a href="index.php?id=JavaScript">JavaScript</a></li>
    </ol>
    <h2>
      <?php
        echo $_GET['id'];
      ?>
    </h2>
    <?php
    echo file_get_contents("data/".$_GET['id']);
     ?>
  </body>
</html>
```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_function_2.png)

id(HTML, CSS, JavaScript)에 따라서 본문 내용 역시 바뀌게 할 수 있다.

file_get_contents()를 통해서 가능하며, 해당 디렉토리를 미리 생성하여(위 사진의 경우 data 디렉토리) 파일명을 ID명과 같게 한 후, 다음과 같은 코드를 실행하면, 제목과 본문 모두 바뀌게끔 만들 수 있다.



## 6) PHP의 Boolean과 비교연산자

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <h1>Comparison Operators &amp;
    Boolean data type </h1>
    <?php
    var_dump('11');
    ?>
    <?php
    var_dump(1==2);
    ?>
    <h2>1>1</h2>
    <?php
    var_dump(1>1);
    ?>
    <h2>1>=1</h2>
    <?php
    var_dump(1>=1);
    ?>
  </body>
</html>

```

문자열이고 2개의 문자로 이루어져 있다는 것을 알려주는 var_dump(나중에 개발을 할 때 유용하게 사용할 수 있음)



## 7) PHP의 조건문의 형식

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>Conditional</h1>
    <h2>if</h2>
    <?php
    echo '1<br>';
    if(false){
      echo '2-1<br>';
    } else{
      echo '2-2<br>';
    }
    echo '3<br>';
    ?>

    <?php
    echo '1<br>';
    if(true){
      echo '2<br>';
    }
    echo '3<br>';
    ?>
  </body>
</html>
```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\conditional_php.png)



<?php> 구문에서 echo '1' '2' '3' 들만 입력한 후 출력하면, 자연스럽게 순서대로 1 2 3이 뜬다. 만약 조건문(if)를 활용해서 if() 괄호 안의 내용이 참이면 아래의 내용을, 거짓이면 건너뛰고 그 다음의 내용을 실행하도록 할 수 있다. ()안의 내용이 참일 때의 코드는 상단 코드의 아래쪽과 같다. 만약 else 구문을 넣어서, 참이면 ()를 실행하고 그렇지 않으면 else {} 에서 괄호 안의 내용을 실행하게끔 할 수도 있다. 그 경우 2-1이 아닌 2-2가 출력되는데, 그 이유는 if() 괄호 안의 내용이 False이기 때문이다.

## 10) PHP의 조건문 활용

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>WEB</h1>
    <ol>
      <li><a href="index.php?id=HTML">HTML</a></li>
      <li><a href="index.php?id=CSS">CSS</a></li>
      <li><a href="index.php?id=JavaScript">JavaScript</a></li>
    </ol>
    <h2>
    <?php
    if(isset($_GET['id'])){
      echo file_get_contents("data/".$_GET['id']);
    } else {
      echo "Hello, PHP";
    }
     ?>
   </h2> 
  </body>
</html>

```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_isset.png)

이전까지는 index.php에 ?name=HTML 주소에서는 HTML 설명이, ?name=CSS에서는 CSS 설명이 나오도록 했다. 즉 상단 사진에서 각각을 클릭할 때마다 내용이 동적으로 바뀌게끔 설정할 수 있었다. 해당 배너를 클릭하지 않은 상태에서 내용을 출력하고 싶다면, if - else 문을 통해서 표현할 수 있다.

isset() 함수는 ()안의 내용이 실제로 설정이 된 것인지 아닌지를 확인해서 그 결과값에 따라 설정되어있으면 TRUE, 아니면 FALSE를 반환하는 함수이다. 상단 코드에서는 id가 있으면 data 디렉토리에 있는 것을 출력하고, 아니면 "Hello, PHP"를 출력하도록 되어있다. 

## 11) PHP의 반복문 형식

검색어 : php loop statements

공식문서만 보고싶으면 site : php.net php loop statements 이런식으로 검색하면 됨. php.net 내에 검색 결과만 알려줄 수 있도록 해줌.



```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>while</h1>
    <?php
    echo '1<br>';
    $i = 0;
    while($i < 3){
      echo '2<br>';
      $i = $i + 1;
    }
    echo '3<br>';
    ?>
  </body>
</html>
```

 while문을 사용해서 반복문을 사용할 수 있는데, while()에서 ()안에 조건을 충족할 때까지만 조건이 돌기 때문에, 무한 loop에 빠지지 않을 수 있다. 저기다가 while(true) 해버리면....무한 loop가 되어버리면서 컴퓨터가 뻗는다. i라는 변수가 3보다 작을때까지만 실행하기 때문에, 해당 코드의 출력결과는 다음과 같다.

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_while.png)



## 12) PHP 배열의 형식

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>array</h1>
    <?php
    $coworkers = array('sukhoon', 'seoul', 'nation', 'park');
    echo $coworkers[1]. '<br>';
    echo $coworkers[3]. '<br>';
    var_dump(count($coworkers));
    array_push($coworkers, 'graphittie');
    var_dump($coworkers);
    ?>
  </body>
</html>
```

배열을 의미하는 array

하지만 특정 배열에 값을 추가하고 싶다면? array_push() 함수를 사용한다. 기존 coworkers에 'graphittie'라는 것을 추가하는 것.

```html

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>array</h1>
    seoul<br>park<br>int(4)
array(5) {
  [0]=>
  string(7) "sukhoon"
  [1]=>
  string(5) "seoul"
  [2]=>
  string(6) "nation"
  [3]=>
  string(4) "park"
  [4]=>
  string(10) "graphittie"
}
  </body>
</html>
```

출력결과의 페이지 소스 보기

## 13) PHP의 반복문과 배열의 활용

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
        $list = scandir('./data');
        $i = 0;
        while($i < count($list)){
          if($list[$i] != '.') {
            if($list[$i] != '..') {
              echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
            }
          }
          $i = $i + 1;
        }

        /*
        echo "<li>$List[0]</li>\n";
        echo "<li>$List[1]</li>\n";
        echo "<li>$List[2]</li>\n";
        echo "<li>$List[3]</li>\n";
        echo "<li>$List[4]</li>\n";
        echo "<li>$List[5]</li>\n";

        */
        
      ?>
    </ol>
    <h2>
      <?php
      if(isset($_GET['id'])){
        echo $_GET['id'];
      } else {
        echo "Welcome";
      }
      ?>
    </h2>
    <?php
    if(isset($_GET['id'])){
      echo file_get_contents("data/".$_GET['id']);
    } else {
      echo "Hello, PHP";
    }
     ?>
  </body>
</html>
```



/* */ 안에 있는 코드는 실행되지 않는다. 해당 생략 코드들처럼 하나씩 해도 되는데, 줄이 몇백개가 있다면...?

$i < 6 이라는 정적인 형태 대신에, $i < count($list)와 같이 파일의 숫자에 따라 동적으로 실행할 수 있도록 만들어줄 수 있다.

"<li><a href = \"index.php\"> 에서 \을 입력함으로써 큰따옴표를 그대로 알려줄 수 있게 한다. 문자열 큰따옴표의 의미를 갖게 됨.

if($list[$i] != '.')에서 .이 하나인 경우를 제외할 수 있다. 

(참고 : 현재 디렉토리 = . 하나 부모 디렉토리 = .2개)

## 14) PHP 함수의 형식

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
  <h1>Function</h1>
  <h2>Basic</h2>
  <?php
  function basic(){
      print("Lorem ipsum dolor1<br>");
      print("Lorem ipsum dolor2<br>");
  }
  basic();
  basic();
  basic();
  ?>

  <h2> parameter &amp; argument </h2>
  <?php

  function sum($left, $right){
    print($left+$right);
    print("<br>");
  }
  sum(2,4);
  sum(4,6);
  ?>

  <h2>return</h2>
  <?php
  function sum2($left, $right){
    return $left + $right;
  }
  print(sum(2, 4));
  file_put_contents('result.txt', sum(2, 4));
  //email('easygoing_1@naver.com', sum2(2, 4));
  //upload(easygoing.net', sum2(2, 4));
  ?>
  </body>
</html>
```

상단 코드는 basic()이라는 함수(function)에 대한 코드이다. basic(){}에 내용을 넣고, basic() 코드를 입력해주면, 프로그램이 해당 함수를 실행하라는 뜻으로 파악하고, print()를 실행해서 결과를 출력시켜준다.

sum()이라는 함수는 left 변수와 right 변수를 인자로 갖는다. 그러니까 자연스럽게 6과 10이 아래 그림에서 보듯 출력된다.

sum2()라는 함수 역시 같은 변수를 인자로 갖지만, result.txt에 해당 결과값을 넣을 수 있게 하는 함수이다. 새로운 txt 파일을 생성한 것 이외에도 메일로 보내거나 .net에 게재하는 등 응용이 가능하다.

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_function2.png)



## 15) PHP 함수의 활용

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <h2>
      <?php
      print_title();
      ?>
    </h2>
    <?php
    print_description();
     ?>
  </body>
</html>
```

이전 index.php 파일의 경우, 코드가 너무 번잡?한 단점이 있었다(물론 나는 저런 코드도 구현하지 못하지만). 그보다 더 큰 문제는 다른 파일에 대해서도 같은 코드를 입력해야 할 때, 발생한다. 그리고 여러 개의 파일에서 각 코드가 제대로 쓰여졌는지 확인할 때 본문에 코드를 쭉 늘여놓으면 비교가 불가능하다(몇 줄 정도의 코드는 괜찮지만, 몇백 줄의 코드라면?).

따라서 코드 상단에 <?php?에 코드들을 넣고, 이름을 붙여준 다음에 본문에 print_list();와 같이 해준다면, 다른 사람들이 봐도 해당 코드가 제대로 쓰여졌는지, 그리고 그 코드가 무엇인지 쉽게 파악할 수 있다(적절한 이름을 붙이는 것의 중요성은 말해주지 않았지만, 당연히 중요할 것 같다.)

## 16) PHP에서 FORM과 POST

```html
<!doctype html>
<html>
  <body>
    <form action="form.php" method="post">
      <p><input type="text" name="title" placeholder="Title"></p>
      <p><textarea name="description"></textarea></p>
      <p><input type="submit"></p>
    </form>
  </body>
</html>

```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_form_html..png)

주의할 것은 이전과는 달리 method = "post"로 post 방식으로 해야한다는 점.

placeholder = ""는 아무것도 입력되지 않았을 때, 처음 사용자에게 보여주는 빈칸 속의 문구?를 의미. 상단 그림처럼 저렇게 입력할 경우, data라는 디렉토리에 title명(rdfsda)에 해당하는 파일명이 만들어지고, 내용은 fd..뭐시기로 입력된다. 저렇게 유저들이 보낸 정보를 저장하는 것이 가능해졌을 때부터 웹이라는 것이 또 성장하고 복잡해졌다.

```php
<?php
file_put_contents('data/'.$_POST['title'], $_POST['description']);
?>
```





## 17) PHP에서 글생성 기능 구현하기



index.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <a href="create.php">create</a>
    <h2>
      <?php
      print_title();
      ?>
    </h2>
    <?php
    print_description();
     ?>
  </body>
</html>

```

create.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <a href="create.php">create</a>
    <form action="create_process.php" method="post">
      <p>
        <input type="text" name="title" placeholder="Title">
      </p>
      <p>
        <textarea name="description" placeholder="Description"></textarea>
      </p>
      <p>
        <input type="submit">
      </p>
    </form>
  </body>
</html>

```

```php+HTML
<?php
file_put_contents('data/'.$_POST['title'], $_POST['description']);
header('Location: /index.php?id='.$_POST['title']);
?>
```

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_create.png)

create.php를 통해 title, description에 적절한 정보를 넣고  제출(submit)할 경우, 목차가 추가되고, 해당 목차를 클릭할 경우 내용이 표시되게끔 할 수 있다. 

header()를 통해 코드를 실행했을 때 ()안에 있는 주소(Location 이하 부분)가 뜨도록 함으로써, 공백 혹은 사용자가 또 다른 웹페이지를 클릭하지 않도록 할 수 있다. 해당 코드의 경우, index.php?id=create와 같이 이동하게 함으로써, create의 내용이 생성 즉시 바로 보이게끔 설정하는 코드이다.



## 18) PHP에서 글수정 기능 구현하기



index.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <a href="create.php">create</a>
    <?php if(isset($_GET['id'])) { ?>
      <a href="update.php?id=<?=$_GET['id']?>">update</a>
    <?php } ?>
    <h2>
      <?php
      print_title();
      ?>
    </h2>
    <?php
    print_description();
     ?>
  </body>
</html>
```



update.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <a href="create.php">create</a>
    <?php if(isset($_GET['id'])) { ?>
      <a href="update.php?id=<?=$_GET['id']?>">update</a>
    <?php } ?>
    <h2>
     <form action="update_process.php" method="post">
       <input type="hidden" name="old_title" value="<?=$_GET['id']?>">
       <p>
         <input type="text" name="title" placeholder="Title" value="<?php print_title(); ?>">
       </p>
       <p>
         <textarea name="description" placeholder="Description"><?php print_description(); ?></textarea>
       </p>
       <p>
         <input type="submit">
       </p>
     </form>
  </body>
</html>
```

update_process.php

```php
<?php
rename('data/'.$_POST['old_title'], 'data/'.$_POST['title']);
file_put_contents('data/'.$_POST['title'], $_POST['description']);
header('Location: /index.php?id='.$_POST['title']);
?>
```



![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_update1.png)



![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_update2.png)



value="<?=$_GET['id']?>" 는 기본 값을 설정하는 것.

rename(오래된 이름, 새로운 이름 [나머지 꼭 필요하지 않은 것])

create를 통해서 title과 description에 적절한 텍스트를 입력하면, 출력결과 상단처럼, update haeboja가 생김과 동시에 내용까지 같이 출력되게 할 수 있다. 이후, update 버튼을 누르면 그것을 어떻게 바꿀 것인지 입력할 수 있는데, 사용자가 원하는 텍스트(update wanryo)로 바꿔줄 수 있다.



## 19) PHP에서 글삭제 기능 구현하기

index.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
    <a href="create.php">create</a>
    <?php if(isset($_GET['id'])) { ?>
      <a href="update.php?id=<?=$_GET['id']?>">update</a>
      <form action="delete_process.php" method="post">
        <input type="hidden" name="id" value="<?=$_GET['id']?>">
        <input type="submit" value="delete">
      </form>
    <?php } ?>
    <h2>
      <?php
      print_title();
      ?>
    </h2>
    <?php
    print_description();
     ?>
  </body>
</html>
```

delete_process.php

```php+HTML
<?php
unlink('data/'.$_POST['id']);
header('Location: /index.php');
?>
```



delete 기능을 구현할 때에는 반드시 post 방식(get방식이 아니라)으로 해줘야 한다. 그냥 링크로 보내줄 경우, 링크를 누르자마자 삭제가 바로 되어버리기 때문. delete는 데이터를 삭제하는 거고, 이걸 누르자마자 삭제가 되어버리면 그 링크를 복사해서 보내주자 마자 그게 바로 삭제가 되어버리는 문제가 생김. update에서 post방식으로 하듯이, get 방식이 아니라 post 방식으로 구현할 것(delete_process.php에서도 get이 아니라 post로 바꾸기). id 값을 hidden으로 설정함으로써, 사람들이 안보이도록 할 수도 있음.



![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_delete1.png)

![](C:\Users\parks\OneDrive - pusan.ac.kr\바탕 화면\php\php_delete2.png)



update wanryo를 클릭하면, 제목과 내용을 확인할 수 있으며, delete 버튼을 눌러서 제거할 수 있다.



## 20) PHP 파일로 모듈화 - require

리팩토링(효율적으로 만드는 과정)을 반복하면서 코드를 효율적으로 만들기.

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo $_GET['id'];
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo file_get_contents("data/".$_GET['id']);
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$list[$i]\">$list[$i]</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
```

view/top.php



```php+HTML
<?php
require_once('lib/print.php');
?>
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>
      <?php
      print_title();
      ?>
    </title>
  </head>
  <body>
    <h1><a href="index.php">WEB</a></h1>
    <ol>
      <?php
      print_list();
      ?>
    </ol>
```

관용적으로 별도의 폴더를 만들어서 저장한다.(view)



view/bottom.php(2줄 짜리지만, 나중에 더 추가될 수도 있으니)

```php+HTML
</body>
</html>
```



require을 통해서 리팩토링을 한 결과, 코드가 훨씬 간결해졌음을 확인할 수 있다.

```php+HTML
<?php
require_once('lib/print.php');
require_once('view/top.php');
?>
    <a href="create.php">create</a>
    <?php if(isset($_GET['id'])) { ?>
      <a href="update.php?id=<?=$_GET['id']?>">update</a>
      <form action="delete_process.php" method="post">
        <input type="hidden" name="id" value="<?=$_GET['id']?>">
        <input type="submit" value="delete">
      </form>
    <?php } ?>
    <h2>
      <?php
      print_title();
      ?>
    </h2>
    <?php
    print_description();
     ?>
<?php
require_once('view/bottom.php');
?>
```



create.php, update.php 등 수많은 php에서 생성했던 function 들은 모두 '중복'되어 있다. 즉 이것들은 모두 리팩토링의 대상이다.

print.php로 중복되는 코드들을 다 복사해두고, 

<?php

require('lib/print.php');

?> 를 상단에 추가함으로써, 수많은 중복된 함수 코드들을 줄일 수 있다.



php에서는 한 번 정의된 함수를 다시 불러오지 못하도록 되어있으며, 이걸 방지하는 require_once();가 있다. 불러왔던 함수를 또 부를 경우, 에러가 뜨기 때문에 그런 에러를 없애기 위해서는 처음부터 require_once()로 하는 것 역시 방법이다.

## 21) PHP의 보안

<Cross site scripting> (XSS)

cross site scripting을 방지하기 위한 두 가지 방법

1) echo htmlspecialchars(); 안에 감싸면서 자바스크립트를 무력화시킬 수 있음

-> 이미지 등 특별한 태그를 활용하지 못할 수 있음.

2) strip 태그를 이용해서 태그를 다 날리고, 특정 태그를 활용할 수 있는 옵션을 지정할 수도 있음.



* 사용자가 입력한 정보를 무조건 불신하라

XSS.php

```php+HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>XSS</title>
  </head>
  <body>
    <h1>Cross site scripting</h1>
    <?php
    echo htmlspecialchars('<script>alert("babo");</script>');
    ?>
  </body>
</html>
```



lib/print.php

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo htmlspecialchars($_GET['id']);
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    echo htmlspecialchars(file_get_contents("data/".$_GET['id']));
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    $title = htmlspecialchars($list[$i]);
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$title\">$title</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
```



<파일 경로 보호>

```php+HTML
<?php
function print_title(){
  if(isset($_GET['id'])){
    echo htmlspecialchars($_GET['id']);
  } else {
    echo "Welcome";
  }
}
function print_description(){
  if(isset($_GET['id'])){
    $basename = basename($_GET['id']);
    echo htmlspecialchars(file_get_contents("data/".$basename));
  } else {
    echo "Hello, PHP";
  }
}
function print_list(){
  $list = scandir('./data');
  $i = 0;
  while($i < count($list)){
    $title = htmlspecialchars($list[$i]);
    if($list[$i] != '.') {
      if($list[$i] != '..') {
        echo "<li><a href=\"index.php?id=$title\">$title</a></li>\n";
      }
    }
    $i = $i + 1;
  }
}
?>
```

basename()을 통해서 부모 디렉토리로 못가게끔 할 수도 있다. 해커들이 비밀번호 혹은 다른 개인정보가 들어있는 파일이 있다는 것을 알게될 경우, 얼마든지 접속해서 내용들을 뜯어내갈 수 있다.

저렇게 하지 않고, 원래대로 할 경우, ../을 통해 부모 디렉토리로 이동한 다음에 특정한 파일을 불러내서, 안에 있는 정보를 추출할 수 있다. 즉, basename에 파일명만 들어갈 수 있도록 함으로써, 어느 디렉토리에 있는지 알지 못하게끔 만들 수 있다.