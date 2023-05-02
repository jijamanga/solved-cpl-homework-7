Download Link: https://assignmentchef.com/product/solved-cpl-homework-7
<br>
<ol>

 <li>Consider the following procedure in Ada-like syntax (with ​ <u>1-</u><u>​ indexed</u> arrays):<u>​ </u></li>

</ol>

<strong>PROCEDURE</strong> Main ​ <strong>IS</strong>​ i: integer := 3; type vector is array (1..3) of integer; a: vector := (3, 1, 2);

<strong>PROCEDURE</strong> Put (v: vector) ​ <strong>IS</strong>​

<h1>BEGIN</h1>

Put_Line (“A = (“);

<strong>FOR</strong> i ​ <strong>IN</strong>​ v’range ​ <strong>LOOP</strong>​

Put_Line (v(i));

Put_Line (” “);

<h1>                                               END ​ LOOP​ ;​</h1>

Put_Line (“)”);

<strong>END</strong> Put;​

<strong>PROCEDURE</strong> Do_Something (t: mode integer) ​ <strong>IS</strong>​

<strong>BEGIN </strong>i := i – 1; t := i + 1; a(t) := a(i) + 1; a(i) := a(t) + 1; i := i – 1; a(t) := t – 1; a(i) := a(t) – 1; <strong>END</strong> Do_Something;​

<h1>BEGIN</h1>

Do_Something(a(i));

Put (a);

<strong>END</strong> Main;​

<strong> </strong>

<strong> </strong>

What would be the output, assuming the parameter passing mode is pass by:




<table width="672">

 <tbody>

  <tr>

   <td width="672"><strong><em>e.g. copy: value</em></strong>A = (1 3 2)</td>

  </tr>

  <tr>

   <td width="672"><strong>a. reference </strong>A = (? ? ?)</td>

  </tr>

  <tr>

   <td width="672"><strong>b. copy: value-result </strong>A = (? ? ?)</td>

  </tr>

  <tr>

   <td width="672"><strong>c. name </strong>A = (? ? ?)</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<ol start="2">

 <li> Write a Prolog program to answer questions about moving throughout a house.​ You should describe the access via doors with the ‘door_between’ relation. Describe your house and the relation ‘path_from’ as follows.</li>

</ol>




% facts about your house, real or imaginary door_between(bed_room, hidden_chamber). door_between(hidden_chamber, basement).

% how do I get from the bed_room to the basement?

?- path_from(bed_room, basement, Y).​

% go from bed_room to hidden_chamber to the basement

<ul>

 <li>= [bed_room, hidden_chamber, basement] % where can I go from the basement and how do I get there?</li>

</ul>

?- path_from(Y, basement, Z).​

<strong> </strong>

Requirements:

<ul>

 <li>All doors are bidirectional, but the fact will only provide one direction for each pair.</li>

 <li>There could be loops of room design, but each room would be accessed at most once in a path.</li>

 <li>You may only use “=”, “==”, ”+”, “member/2”, “append/3”.</li>

 <li><a href="https://docs.google.com/document/d/1JjCeEE94BlD-LiapP3BCY90y0plSz8-R7TtGHTbLgdQ/edit?usp=sharing"><strong>Test Cases</strong></a></li>

</ul>

<strong> </strong>

<strong>YOUR CODE: </strong>

<strong> </strong>

<strong> </strong>

<ol start="3">

 <li>Klefstad is hosting a party of an international organization. Not everybody speaks​ the same language, and some of them speak more than 1 language. He invited 10</li>

</ol>

guests and – including himself – he plans to have a ROUND TABLE CHATTING SESSION. To make everybody comfortable, he sets the following rules:

○   Each person must be able to have a conversation with both people they are seated next to (in some language).

○    No two females sit next to each other.

○   You can use the following information about the invitees and the host for testing your solution to the problem but ​<strong><u>DO NOT</u></strong><u>​</u> include these in the final code you submit. I will provide you with guests and the languages they speak (in the form of male(name). (or female) and speaks(name, language). If you include the below information in your final submission it is likely you will not get the correct answer on gradescope:

■    <strong>Klefstad</strong>​, ​<strong>Bill</strong>​, ​<strong>Emily</strong>​, ​<strong>Heidi</strong>​, and ​<strong>Isaac</strong>​ speak ​<strong>English</strong>​.

■    <strong>Beth</strong>​, ​<strong>Mark</strong>​, ​<strong>Susan</strong>​, and ​<strong>Isaac</strong>​ can speak ​<strong>French</strong>​.

■    <strong>Klefstad</strong>​, ​<strong>Bill</strong>​, ​<strong>Susan</strong>​, ​<strong>Fred</strong>​, and ​<strong>Jane</strong>​ speak ​<strong>Spanish</strong>​.

■    <strong>Klefstad</strong>​, ​<strong>Bill</strong>​, ​<strong>Mark</strong>​, ​<strong>Isaac</strong>​, and ​<strong>Fred</strong>​ identify as ​<strong>Male</strong>​.

■    <strong>Emily</strong>​, ​<strong>Heidi</strong>​, ​<strong>Beth</strong>​, ​<strong>Susan</strong>​, and ​<strong>Jane</strong>​ identify as ​<strong>Female</strong>​.

<strong> </strong>

Your program should be able to come up with a seating in a ring (around a round table) to satisfy the constraints described above. e.g.

<strong> </strong>

?- ​party_seating(L).

L = [jane, klefstad, susan, bill, emily, isaac, heidi, fred, beth, mark].




This is a made-up sample answer, not a correct answer, but shows how your program should show correct seating.

<strong> </strong>

<strong>YOUR CODE: </strong>

<strong> </strong>

<ol start="4">

 <li><strong>[30] </strong>​Write a Prolog program to do symbolic differentiation of polynomials with respect to</li>

 <li>Fun fact, this was the first program I wrote in Prolog. My second program was symbolic integration which is harder.

  <ul>

   <li>What you are allowed to use:</li>

  </ul></li>

</ol>

○    you only need “=”, “+”, “-”, “*”, “/”,“^”, “is”, “atomic/1”, “number/1”

○    you may use the cut symbol, “!”, only after it finds an answer, so prevents it from returning the same answer again.

<ul>

 <li>For any symbol times a constant, put the constant in the front: 2*x instead of x*2 ● Simplify as much as you can</li>

</ul>

<strong> </strong>

<strong>Use the following test cases: </strong>

<strong> </strong>

?- deriv(x^2, Y).​        Y = 2*x.

?- deriv((x*2*x)/x, Y).​    Y = 2.

?- deriv(x^4+2*x^3-x^2+5*x-1/x, Y).​ Y = 4*x^3+6*x^2-2*x+5+1/x^2.

?- deriv(4*x^3+6*x^2-2*x+5+1/x^2, Y).​      Y = 12*x^2+12*x-2-2/x^3.

?- deriv(12*x^2+12*x-2-2/x^3, Y).​

<ul>

 <li>= 24*x+12+6/x^4.</li>

</ul>

<strong> </strong>

<strong>YOUR CODE: </strong>