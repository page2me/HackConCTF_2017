

<h2>Task : WEB (50) Noobcoder <br></h2>
link : http://defcon.org.in:6062/ <br>
It says that user was using gedit, we know that gedit has some problems when saving files, like creating another file~ 
<br>We look for index.php~ : we see source code<br>
now we just need to verify the condition, by sending 1e2 as username, and 100 as password ( it gets interpreted as equal values)  <br>
but not same type
Bingo we get the flag :  congratulations the flag is d4rk{l0l_g3dit_m4ster_roxx}c0de 


<h2>Task : WEB (50) Magic  <br></h2>
link : http://defcon.org.in:6060/index.php/ <br>
Looked like an injection in the begining, but nope, just magic if we fire burp or examine element and refresh page we see <br>
set cookie parameter with some values like : "269=%2B; expires=Thu, 01-Jan-1970 00:00:10 GMT; Max-Age=0; path=/"<br>
all you need is script this and reconstruct the text and url decode it hmm we get something now <br>

<b>
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>>+++++++++++++++++.--.--------------.+++++++++++++.----.-------------.++++++++++++.--------.<------------.<++.>>----.+.<+++++++++++.+++++++++++++.>+++++++++++++++++.---------------.++++.+++++++++++++++.<<.>>-------.<+++++++++++++++.>+++..++++.--------.+++.<+++.<++++++++++++++++++++++++++.<++++++++++++++++++++++.>++++++++++++++..>+.----.>------.+++++++.--------.<+++.>++++++++++++..-------.++</b><br>
 that looks like brainfuck language let's decode it <br>
  we get "username: abERsdhw password: HHealskdwwp " <br>
  use them as creds then login and get your flag! easy
  <br>
  
  
<h2>Task : WEB (75) Dictator  <br></h2>
