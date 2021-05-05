## PHP Quiz

#### Q1. What is the key value for "B" and "C"?

```php
$array = array(2 => "A", "B", "C");

foreach( $array as $key => $value ){
    echo $key." => ".$value."  ";
}
```

- [ ] 0 => B  1 => C
- [ ] 1 => B  2 => C
- [ ] 1 => B  3 => C
- [X] 3 => B  4 => C
- [ ]  => B   => C

Explanation:
  - Will be in this order:  2 => A  3 => B  4 => C

#### Q2. What is the type of the keys and the values in an array? ie.:

  ```php
  $array = array("-1" => "2");

  echo gettype(array_keys($array)[0]); echo " => ";
  echo gettype($array["-1"]); echo ", ";

  foreach($array as $key => $value ){
      echo gettype($key); echo " => ";
      echo gettype($value); echo " ";
  }
  ```

  - [ ] string => string, string => string
  - [ ] integer => integer, integer => integer
  - [X] integer => string, integer => string
  - [ ] string => integer, string => integer
  - [ ] integer => string, string => string

  Explanation:
    - The keys are automatically converted to integer whenever possible.
    - The value type doesn't change.

#### Q3. What does this do?

      ```php
      <?=0?>
      ```

      - [ ] Nothing (will be ignored by PHP)
      - [ ] Raises an error
      - [ ] Initialize global variables
      - [ ] Sets 0 for false
      - [X] Displays 0

      Explanation:
        - The following <?= 'Hello' ?> displays 'Hello' (a short way for echo)
        - It has to be located outside any other <? ... ?> PHP tag

      Reading further: https://www.php.net/manual/en/language.basic-syntax.phptags.php

#### Q4. Which one(s) of the following is/are incorrect, so will cause the error (0 to 5 choices possible)?

      ```php
      class User
      {
          static public $a = 1; // 1
          public static $b = 2; // 2
          const $c = 3; // 3
          const d = 4; // 4
          const E = 5; // 5
      }
      echo User::$a." ";
      echo User::$b." ";
      echo User::$c." ";
      echo User::d." ";
      echo User::E." ";
      ```

      - [ ] 1
      - [ ] 2
      - [X] 3
      - [ ] 4
      - [ ] 5

      Explanation:
        - Constants NEVER have the '$' sign prefix
        - For all the rest, the language is flexible

      Further reading: https://php5-tutorial.com/classes/constants/
