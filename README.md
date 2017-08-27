

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

<b><code>
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>>+++++++++++++++++.--.--------------.+++++++++++++.----.-------------.++++++++++++.--------.<------------.<++.>>----.+.<+++++++++++.+++++++++++++.>+++++++++++++++++.---------------.++++.+++++++++++++++.<<.>>-------.<+++++++++++++++.>+++..++++.--------.+++.<+++.<++++++++++++++++++++++++++.<++++++++++++++++++++++.>++++++++++++++..>+.----.>------.+++++++.--------.<+++.>++++++++++++..-------.++</code></b><br>
 that looks like brainfuck language let's decode it <br>
  we get "username: abERsdhw password: HHealskdwwp " <br>
  use them as creds then login and get your flag! easy
  <br>
  
  
<h2>Task : WEB (75) Dictator  <br></h2>
Link: http://defcon.org.in:6063/<br>
This one wasn't solved by many people although it was easy, so the description says you need to be from same country (North korea)<br>
first it shows access denied as default <br>
we change the X-Forwarded header we add a korean public ip  like :<br>
<code>X-Forwarded-For	
175.45.176.0</code>
<br>Now we get an interesting message  : "You are not following the instructions given by the supreme-leader"
<br>After changing a lot of stuff, what worked is changing user agent to a north korean user agent which is "Naenara"<br>
change user agent value with : <code>Mozilla/5.0 (X11; U; Linux i686; en-US; rv:1.9.1b4) Gecko/20130508 Fedora/1.9.1-2.5.rs3.0 NaenaraBrowser/3.5b4</code><br>
and we get our flag d4rk{Welcome_To_DictatorRuling.TogetherweshalltkeWorld}c0de

<h2>Task : Bachhe (25) Xrrr <br></h2>
obvious title it's a xor encryption, from the text it's look like hex values, let's decode that, and run a tool that cracks xor<br>
Easy task we get the key : bharat <br>
decrypting everything we get an embeded flag inside some text d4rk{Try_r34ding_mahabharata_s0met1me}c0de  <br>
<h2>Task : CRYPTO (50) RSA - 2 <br></h2>
we are provided with : <br>
<code>n = 109676931776753394141394564514720734236796584022842820507613945978304098920529412415619708851314423671483225500317195833435789174491417871864260375066278885574232653256425434296113773973874542733322600365156233965235292281146938652303374751525426102732530711430473466903656428846184387282528950095967567885381

e = 49446678600051379228760906286031155509742239832659705731559249988210578539211813543612425990507831160407165259046991194935262200565953842567148786053040450198919753834397378188932524599840027093290217612285214105791999673535556558448523448336314401414644879827127064929878383237432895170442176211946286617205

c = 103280644092615059984518332609100925251130437801342718478803923990158474621180283788652329522078935869010936203566024336697568861166241737937884153980866061431062015970439320809653170936674539901900312536610219900459284854811622720209705994060764318380465515920139663572083312965314519159261624303103692125635</code><br>
looks like wiener attack on RSA key, let's use some ready to go tools to find d <br>
<code>python RSAwienerHacker.py 
Hacked!
21780352155588618020563641971337344243907391969899764877790673891831527301137
</code><br>
now we just decrypt and get our message<br>
we get 0x6434726b7b315f37306c645f7930755f746831355f776f756c645f38655f6d6f72655f646966666963756c747d63306465L
<br>After decoding the hex we find the flag : d4rk{1_70ld_y0u_th15_would_8e_more_difficult}c0de


