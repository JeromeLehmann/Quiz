## Java Quiz

#### (1pt) Q1. What is the result of this zero division?

```java
System.out.println((double)-5 / (double)0);
```

- [ ] Exception in thread "main" java.lang.ArithmeticException: / by zero
- [ ] NEGATIVE_INFINITY
- [ ] NaN
- [ ] MIN_VALUE
- [x] -Infinity

Explanation:
  - 5/0 returns Exception
  + (float)5/0  or 5/(float)0  returns Infinity
  + (double)5/0 or 5/(double)0 returns Infinity

Further reading: https://www.baeldung.com/java-division-by-zero

#### (1pt) Q2. Which of the following is/are NOT correct?

- [x] char a = '';
- [x] char b='b'; if(b.equals('b')){return true};
- [x] Character c = new Character(''); if(c.equals('c')){return true;}
- [ ] Character c = new Character('c'); if(c.equals('c')){return true;}
- [ ] Character c = new Character('c'); if(c.equals("c")){return true;}

Explanation:
  - A character can never be empty (it is and must be of length 1). Note: as a consequence: char, or class Character, DON'T accept the method .length()
  - char DOESN'T accept the method .equals(), but uses == instead
  + c.equals("c") => is accepted by compiler, but will return false

Further reading: https://www.tutorialspoint.com/java/lang/character_equals.htm

#### (1pt) Q3. Which of the following will NOT compile?

- [ ] if(1==1){}
- [ ] if(1==1){;}
- [ ] if(1==1){};
- [x] if(1==1){null;}
- [x] if(1==1){true;}

Explanation:
  + Empty statements are allowed (you can add as many ; as you want)
  - But instructions out of any treatment will raise a compilation error ("error: not a statement")
