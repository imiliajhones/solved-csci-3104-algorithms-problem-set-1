Download Link: https://assignmentchef.com/product/solved-csci-3104-algorithms-problem-set-1
<br>
<em>Advice 1</em>: For every problem in this class, you must justify your answer: show how you arrived at it and why it is correct. If there are assumptions you need to make along the way, state those clearly.

<em>Advice 2</em>: Verbal reasoning is typically insufficient for full credit. Instead, write a logical argument, in the style of a mathematical proof.

<ol>

 <li>(10 pts total) For each of the following claims, determine whether they are true or false. Justify your determination (show your work). If the claim is false, state the correct asymptotic relationship as <em>O</em>, Θ, or Ω.</li>

</ol>

(a)

<ul>

 <li>2</li>

 <li>2</li>

 <li>1 =</li>

 <li>3</li>

 <li>2</li>

</ul>

(i)

(j)                10

<ol start="2">

 <li>(15 pts) Professor Dumbledore needs your help optimizing the Hogwarts budget. You’ll be given an array <em>A </em>of exchange rates for muggle money and wizard coins, expressed at integers. Your task is help Dumbledore maximize the payoff by buying at some time <em>i </em>and selling at a future time <em>j &gt; i</em>, such that both <em>A</em>[<em>j</em>] <em>&gt; A</em>[<em>i</em>] and the corresponding difference of <em>A</em>[<em>j</em>] − <em>A</em>[<em>i</em>] is as large as possible.</li>

</ol>

For example, let <em>A </em>= [8<em>,</em>9<em>,</em>3<em>,</em>4<em>,</em>14<em>,</em>12<em>,</em>15<em>,</em>19<em>,</em>7<em>,</em>8<em>,</em>12<em>,</em>11]. If we buy stock at time <em>i </em>= 2 with <em>A</em>[<em>i</em>] = 3 and sell at time <em>j </em>= 7 with <em>A</em>[<em>j</em>] = 19, Hogwarts gets in income of 19 − 3 = 16 coins.

(a) Consider the pseudocode below that takes as input an array <em>A </em>of size <em>n</em>:

makeWizardMoney(A) : maxCoinsSoFar = 0 for i = 0 to length(A)-1 { for j = i+1 to length(A) {

1

coins = A[j] – A[i] if (coins &gt; maxCoinsSoFar) { maxCoinsSoFar = coins }

}}

return maxCoinsSoFar

What is the running time complexity of the procedure above? Write your answer as a Θ bound in terms of <em>n</em>.

<ul>

 <li>Explain (1–2 sentences) under what conditions on the contents of <em>A </em>the makeWizardMoney algorithm will return 0 coins.</li>

 <li>Dumbledore knows you know that makeWizardMoney is wildly inefficient. With a wink, he suggests writing a function to make a new array <em>M </em>of size <em>n </em>such that <em>M</em>[<em>i</em>] = min <em>A</em>[<em>j</em>] <em>.</em></li>

</ul>

0≤<em>j</em>≤<em>i</em>

That is, <em>M</em>[<em>i</em>] gives the minimum value in the subarray of <em>A</em>[0<em>..i</em>].

What is the running time complexity of the pseudocode to create the array <em>M</em>? Write your answer as a Θ bound in terms of <em>n</em>.

<ul>

 <li>Use the array <em>M </em>computed from (2c) to compute the maximum coin return in time Θ(<em>n</em>).</li>

 <li>Give Dumbledore what he wants: rewrite the original algorithm in a way thatcombine parts (2b)–(2d) to avoid creating a new array <em>M</em>.</li>

</ul>

<ol start="3">

 <li>(15 pts) Consider the problem of linear search. The input is a sequence of <em>n </em>numbers <em>A </em>= h<em>a</em><sub>1</sub><em>,a</em><sub>2</sub><em>,…,a<sub>n</sub></em>i and a target value <em>v</em>. The output is an index <em>i </em>such that <em>v </em>= <em>A</em>[<em>i</em>] or the special value NIL if <em>v </em>does not appear in <em>A</em>.

  <ul>

   <li>Write pseudocode for a simple linear search algorithm, which will scan throughthe input sequence <em>A</em>, looking for <em>v</em>.</li>

   <li>Using a loop invariant, prove that your algorithm is correct. Be sure that yourloop invariant and proof covers the initialization, maintenance, and termination</li>

  </ul></li>

</ol>

conditions.

<ol start="4">

 <li>(15 pts) Crabbe and Goyle are arguing about binary search. Goyle writes the following pseudocode on the board, which he claims implements a binary search for a target value v within input array A containing <em>n </em></li>

</ol>

bSearch(A, v) { return binarySearch(A, 1, n-1, v)

}

binarySearch(A, l, r, v) { if l &lt;= r then return -1 p = floor( (l + r)/2 ) if A[p] == v then return p if A[p] &lt; v then

return binarySearch(A, p+1, r, v) else return binarySearch(A, l, p-1, v)

<ul>

 <li>Help Crabbe determine whether this code performs a correct binary search. If itdoes, prove to Goyle that the algorithm is correct. If it is not, state the bug(s), give line(s) of code that are correct, and then prove to Goyle that your fixed algorithm is correct.</li>

 <li>Goyle tells Crabbe that binary search is efficient because, at worst, it dividesthe remaining problem size in half at each step. In response Crabbe claims that four-nary search, which would divide the remaining array <em>A </em>into fourths at each step, would be <em>way more </em> Explain who is correct and why.</li>

</ul>

<ol start="5">

 <li>(10 pts extra credit) You are given two arrays of integers <em>A </em>and <em>B</em>, both of which are sorted in ascending order. Consider the following algorithm for checking whether or not <em>A </em>and <em>B </em>have an element in common.</li>

</ol>

findCommonElement(A, B) :

# assume A,B are both sorted in ascending order

for i = 0 to length(A) {              # iterate through A for j = 0 to length(B) {             # iterate through B if (A[i] == B[j]) { return TRUE } # check pairwise

} } return FALSE

<ul>

 <li>If arrays <em>A </em>and <em>B </em>have size <em>n</em>, what is the worst case running time of the procedure findCommonElement? Provide a Θ bound.</li>

 <li>For <em>n </em>= 5, describe input arrays <em>A</em><sub>1</sub>, <em>B</em><sub>1 </sub>that will be the best case, and arrays <em>A</em><sub>2</sub>, <em>B</em><sub>2 </sub>that will be the worst case for findCommonElement.</li>

 <li>Write pseudocode for an algorithm that runs in Θ(<em>n</em>) time for solving the problem.</li>

</ul>

Your algorithm should use the fact that <em>A </em>and <em>B </em>are sorted arrays.

(Hint: repurpose the merge procedure from MergeSort.)