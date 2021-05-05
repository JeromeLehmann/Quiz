## Unix Shell (bash) Learning Quiz

#### (3pt) Q1. How can you print out "foo" from the variable b?

```bash
a=foo
b=a
```

- [ ] eval echo $$b
- [ ] eval echo ${$b}
- [x] eval echo \$$b
- [x] eval echo '$'$b
- [ ] This is not possible

Explanation:
  - $$ gives the PID, so "echo $$b" or "eval echo $$b" returns for example: 6139b
  - ${$var} is incorrect, so "echo ${$b}" or "eval echo ${$b}" will raise: "bash: ${$b}: bad substitution"
  + But "eval echo \$$b" means "eval echo $a" which returns "foo"
  ! Warning: This may look particular comparing to the above, but "echo $b" returns "a", and "echo \$$b" returns "$a"

Further reading: https://linuxhint.com/bash_eval_command

#### (1pt) Q2. What is the result of echo ${t[1]} ?

```bash
t[0]=1
t[2]=1
```

- [ ] bash: error
- [ ] NaN
- [ ] 0
- [x] empty line
- [ ] Cannot do: tab[2]=1

Explanation:
  + There is no limit in arrays. Even newt[10**10**10]=1 is working (** is for raising to power sign)
  + t[0]=1;t[2]=1 is similar to: t=(1 '' 1)

Further reading:
  Easy:     https://www.tutorialspoint.com/unix/unix-using-arrays.htm
  Medium:   https://opensource.com/article/18/5/you-dont-know-bash-intro-bash-arrays
  Advanced: https://www.geeksforgeeks.org/array-basics-shell-scripting-set-1/

#### Q3. (2pt) How can you make an infinite loop?

  - [ ] while 1
  - [x] while :
  - [x] while true   ,OR   while /bin/true ,OR   while /usr/bin/true
  - [ ] while (1==1) ,OR   while ((1==1))
  - [x] while [1==1] ,OR   while [[1==1]]

  Explanation:
    - Result of while 1 is "1: command not found"
    - Result of while (1==1) is "1==1: command not found"
    + Everything else is working

Further reading: https://ss64.com/bash/syntax-brackets.html

#### (1pt) Q4. What are correct Hashplings?

- [x] #!/bin/sh
- [x] #!/bin/ksh
- [x] #!/bin/csh
- [x] #!/bin/ash
- [x] #!/bin/tcsh

Explanation:
  + Hashplings (or Shebangs) are used to tell the script where is the interpreter.
  + Starts with # makes it to be ignored by most of non-Unix scripts, but Unix recognizes the first #! (0x23 0x21) combination as the Hashplings mark
  + The fist above is for: Shell, Korn shell (from David Korn), C shell (written in C), Almquist shell (from Kenneth Almquist), TENEX OS C shell
  + There are 16 main shells (listed on Wikipedia), but there is more as some of them have other sub-variations

Further reading: http://dcjtech.info/topic/types-of-linux-executables/
More details: https://www.in-ulm.de/~mascheck/various/shebang/
