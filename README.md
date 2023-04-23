Download Link: https://assignmentchef.com/product/solved-ada-homework-2-line-of-battle
<br>
<h1>Problem 1 – Line of Battle (Programming)</h1>

<h2>Problem Description</h2>

WillyPillow is recently obsessed with a mobile game called <em>Azure Line</em>, which involves multiple ships lining up and forming fleets. In the game, each ship is characterized by two parameters: a leader<em>ship </em>factor and a team awareness factor. In addition, we define a fleet as a non-empty set of contiguous ships in which the ship that comes first is the flagship. For a fleet to be efficient, the leader<em>ship </em>factor of the flagship has to be no smaller than the sum of the team awareness factors of the other ships in the fleet.

Now, WillyPillow is given a line of <em>N </em>ships, and he wants to calculate how many combinations of fleets he can form such that all fleets are efficient and one ship is assigned to exactly one fleet. Two combinations are considered different if there exists a pair of ships that are in the same fleet in one combination but are in different fleets in the other.

Formally speaking, he has to count the number of ways to partition a list into segments, with every segment [<em>l,r</em>] satisfying, where <em>a<sub>i </sub></em>and <em>b<sub>i </sub></em>are the leadership and team awareness factors, respectively, of the <em>i</em>-th ship.

<h2>Input</h2>

Due to the sheer size of the input data, you are required to use the <em>generator </em>in the link below to generate data on the fly:

https://gitlab.com/snippets/1904475

Specifically, you need to paste the given <em>generator </em>at the beginning of your source file, and use it as follows:

int n = ada::Init(); // Get N for (int i = 0; i &lt; n; i++) leadership[i] = ada::GetLeadership(); for (int i = 0; i &lt; n; i++) team_value[i] = ada::GetTeamValue();

You <strong>may not </strong>interact with the standard input by any other means, e.g., scanf and cin.

Note that in all test groups, the leader<em>ship </em>and team awareness factors are in the range [0<em>,</em>10<sup>9</sup>].

<table width="480">

 <tbody>

  <tr>

   <td width="269"><strong>Test Group 0 (0 %)</strong>•    Sample Input<strong>Test Group 1 (5 %)</strong>•    1 ≤ <em>N </em>≤ 500</td>

   <td width="211"><strong>Test Group 2 (15 %)</strong>•    1 ≤ <em>N </em>≤ 5 × 10<sup>3</sup><strong>Test Group 3 (80 %)</strong>•    1 ≤ <em>N </em>≤ 2 × 10<sup>6</sup></td>

  </tr>

 </tbody>

</table>

<h2>Output</h2>

Please output an integer (to the standard output) indicating the number of ways to form combinations of fleets, modulo the prime 10<sup>9 </sup>+ 7.

<strong>Sample Input 1</strong>

5 20 20 1537688804 584589912 3972715898 2166415565

<strong>Sample Output 1</strong>

2

<strong>Sample Input 2</strong>

10 20 20 4041108152 584535659 2466603739 198973427

<strong>Sample Output 2</strong>

46

<h1>Problem 2 – Chunithm (Programming)</h1>

<h2>Problem Description</h2>

You are playing a game “chunithm”. As the most talented student at NTU CSIE, you want to make sure that you can win the game with the least effort.

In the beginning of the game, you are given a song. The song is <em>N </em>seconds long and there is exactly one note at one second. You have a keyboard with <em>M </em>different notes, and all notes in the song can be played with this keyboard. You play the song with two hands on the keyboard. If the song contains the note <em>j </em>at <em>i</em>-th second, one of your hands must put on the note <em>j </em>of the keyboard at that second. The distance between notes <em>j</em><sub>1 </sub>and <em>j</em><sub>2 </sub>on the keyboard is |<em>j<sub>i </sub></em>− <em>j</em><sub>2</sub>|.

The effort of playing the game is defined as follows:

During the interval between <em>i</em>-th and (<em>i</em>+1)-th seconds, you can move each of your hands for distance <em>K </em>without any effort. (Both of your hands can move at the same time.) If you move a hand for more than distance <em>K </em>in one second, the effort of moving the hand is (the number of steps you moved−<em>K</em>). Initially, you can put your hands at any position without any effort. The effort will accumulate over time and the effort experienced by both hands will add up.

Given the song, the size of the keyboard <em>M</em>, and the distance number you can easily move <em>K</em>, please output the minimum effort you need for finishing playing the song (the hands can start from anywhere on the keyboard).

<h2>Input</h2>

The first line of the input consists of 3 integers <em>N</em>, <em>M</em>, and <em>K</em>. The second line consists of <em>N </em>numbers <em>a</em><sub>0</sub>, <em>a</em><sub>1</sub>, …, <em>a<sub>n</sub></em><sub>−1</sub>. <em>a<sub>i </sub></em>indicates the note of the song at <em>i</em>th second.

<ul>

 <li>1 ≤ <em>N </em>≤ 100000</li>

 <li>1 ≤ <em>M </em>≤ 300</li>

 <li>1 ≤ <em>K </em>≤ <em>M</em></li>

 <li>0 ≤ <em>a<sub>i </sub>&lt; M</em></li>

</ul>

<h2>Output</h2>

An integer indicates the amount of effort.

<strong>Subtask 1 (30 %)</strong>

<ul>

 <li><em>N </em>≤ 100<em>,M </em>≤ 100</li>

</ul>

<strong>Subtask 2 (30 %)</strong>

<ul>

 <li><em>N </em>≤ 3000</li>

</ul>

<strong>Subtask 3 (40 %)</strong>

<ul>

 <li>No other constraints.</li>

</ul>




<h2>Sample Input 1</h2>

7 7 1

0 1 2 6 5 4 0

<strong>Sample Output 1</strong>

0

<h2>Sample Input 2</h2>

8 7 1

0 6 4 3 2 1 5 0

<strong>Sample Output 2</strong>

1




<h1>Problem 3 – Pok´emon GO (Programming)</h1>

<h2>Problem Description</h2>

WillyPillow is a Pok´emon trainer, and he has <em>N </em>Pok´emon. Each Pok´emon has a unique ID from 1 to <em>N</em>, where the Pok´emon with the ID <em>i </em>has three attributes: a attack power <em>A<sub>i</sub></em>, a potential value <em>B<sub>i</sub></em>, and an experience point <em>E<sub>i </sub></em>which is initially set to zero.

The battle between WillyPillow and his rival has <em>K </em>rounds, and both of them have to pick <em>K </em>Pok´emon and arrange their attacking order. Let <em>p<sub>i </sub></em>be the ID of the Pok´emon WillyPillow summons in the <em>i</em>-th round. The Pok´emon will first cause (<em>A<sub>p</sub></em><em><sub>i </sub></em>× <em>E<sub>p</sub></em><em><sub>i</sub></em>) damage to the opponent, then it will use its magic power to increase <em>B<sub>p</sub></em><em><sub>i </sub></em>experience points of all other WillyPillow’s Pok´emon which have not yet be summoned.

Because WillyPillow is busy preparing for the ADA exam, you, who live on Pok´emon betting and have spent all money on this battle, decide to help him choose <em>K </em>Pok´emon and arrange their attacking order such that the maximum total damage can be achieved.

<h2>Input</h2>

The first line of the input contains two integers <em>N </em>and <em>K</em>, indicating the number of Pok´emon WillyPillow has and the number of rounds in the battle, respectively.

<em>N </em>lines follow, the <em>i</em>-th of which contains two integers <em>A<sub>i</sub>,B<sub>i</sub></em>, denoting the attack power and the

potential value of the Pok´emon with ID <em>i</em>.

<ul>

 <li>1 ≤ <em>K </em>≤ <em>N </em>≤ 100</li>

 <li>0 ≤ <em>A<sub>i</sub>,B<sub>i </sub></em>≤ 100</li>

</ul>

<strong>Test Group 0 (10 %) Test Group 2 (80 %) </strong>• <em>K </em>= <em>N     </em>• No other constraints.

<strong>Test Group 1 (10 %)</strong>

<ul>

 <li><em>N </em>≤ 10</li>

</ul>

<h2>Output</h2>

Print an integer indicating the maximum possible total damage that can be achieved if <em>K </em>Pok´emon are chosen and arranged optimally.

<h2>Sample Input 1</h2>

9 4

6 8

0 13

14 14

14 1

14 4

13 5

3 11

5 6

3 12

<strong>Sample Output 1</strong>

994

<h2>Sample Input 2</h2>

6 6

10 7

0 8

5 3

10 7

2 9

1 3

<strong>Sample Output 2</strong>

673

<h1>Problem 4 – Weigh Anchor (Programming) (15 points)</h1>

<h2>Problem Description</h2>

After WillyPillow assembled his fleet in <em>Azure Line</em>, he can now fight the war!

Aiming to win the war, WillyPillow picks three most well-trained ships, which have strengths <em>s</em><sub>1</sub>, <em>s</em><sub>2</sub>, and <em>s</em><sub>3</sub>, respectively.

The war consists of a set of battles. For each battle, he can select any subset of his ships to fight. He wins the battle if and only if the sum of the strengths of his chosen ships is no smaller than the strength of the enemy in this battle. Each ship can only be assigned to fight one battle per hour.

For example, he can fight two battles using ships <em>s</em><sub>1 </sub>+ <em>s</em><sub>2 </sub>and <em>s</em><sub>3 </sub>in an hour, but he can not fight three battles using ships <em>s</em><sub>1 </sub>+ <em>s</em><sub>2</sub>, <em>s</em><sub>2</sub>, and <em>s</em><sub>3 </sub>in an hour, since <em>s</em><sub>2 </sub>is used twice.

Since WillyPillow also needs to train Pok´emon and prepare for the ADA exam (c.f. problem 3), he wants to spend as little time as possible on playing the game. Given the enemy strength of each battle, he wants to find out how much time he needs in order to win all the battles according to the rules above. Note that he can fight the battles in any order.

<h2>Input</h2>

The first line of the input file contains an integer indicating <em>N</em>, the number of battles.

The second line contains three integers separated by spaces, indicating <em>s</em><sub>1</sub><em>,s</em><sub>2</sub>, and <em>s</em><sub>3</sub>, the strengths of WillyPillow’s ships.

The third line contains <em>N </em>integers separated by spaces, with the <em>i</em>-th integer indicating the enemy strength of the <em>i</em>-th battle, denoted by <em>a<sub>i</sub></em>.

<ul>

 <li>1 ≤ <em>N </em>≤ 2 × 10<sup>5</sup></li>

 <li>1 ≤ <em>s</em><sub>1</sub><em>,s</em><sub>2</sub><em>,s</em><sub>3</sub><em>,a<sub>i </sub></em>≤ 10<sup>8</sup></li>

</ul>

<table width="499">

 <tbody>

  <tr>

   <td width="328"><strong>Test Group 0 (5 %)</strong>• <em>N </em>≤ 4</td>

   <td width="171"><strong>Test Group 2 (85 %)</strong>• No other constraints.</td>

  </tr>

 </tbody>

</table>

<strong>Test Group 1 (10 %)</strong>

<ul>

 <li><em>N </em>≤ 10</li>

</ul>

<h2>Output</h2>

Please output an integer indicating the minimum number of hours WillyPillow needs to win all the battles. If it’s impossible to defeat all enemies, output −1 instead.

<h2>Sample Input 1</h2>

8

6 11 7

10 20 13 12 20 3 5 10

<strong>Sample Output 1</strong>

5

<h2>Sample Input 2</h2>

8

7 16 9

4 17 8 4 15 6 13 1

<strong>Sample Output 2</strong>

3

<h1>Problem 5 – Piepie’s Pie Shop (Hand-Written) (16 points)</h1>

Piepie is a genius developer in Coming Spiorad International Enterprise and also a world famous chocolate-pie maker. People are willing to line up for 49 hours in order to purchase the chocolate pie he made, even he can make 1025 chocolate pies per hour. Nevertheless, Piepie felt bored by making delicious chocolate pies after earning his first trillion dollars. Thus, he decided to open a brand new pie shop.

The new pie shop has only one table that can accommodate a group of <em>N </em>customers at the same time. A group of <em>N </em>customers will come to the shop together and leave together. Each customer <em>i </em>will have his/her customized pie that takes Piepie <em>p<sub>i </sub></em>minutes, and the customer will finish eating the pie exactly <em>e<sub>i </sub></em>minutes after the pie is served. Piepie only makes one pie simultaneously, and there is no time gap between two pies.

After opening the shop, he notices that the order of making pies affects the group’s leaving time. In order to make the group leave as fast as possible and make big money, he is seeking the best strategy of arranging the order and the corresponding minimum time needed for finishing serving the group of customers with the given information. Although he is a genius, he is sometimes too lazy to think. Can you please finish the task for him?

For this problem, each customer can be represented by a number from 1 to <em>N</em>.

<em>Note that if you use Greedy or Dynamic Programming in any subproblem of this problem, you should prove their properties.</em>

<ul>

 <li>(2pts) Given the preparation time and eating time of a group of <em>N </em>= 5 customers, [(2, 13), (4, 2), (3, 4), (7, 3), (5, 5)]</li>

</ul>

Please show your arrangement and the minimum time needed.

<ul>

 <li>(4pts) Please design an algorithm to provide your arrangement and calculate the total time needed. Your algorithm should run in <em>O</em>(<em>N </em>lg<em>N</em>) time. Also, you need to explain why your algorithm meets the time complexity requirement.</li>

 <li>(4pts) Please prove the correctness of your algorithm in (2).</li>

 <li>(3pts) To reach the true power of making pie, he decided to learn more in the Ninja School. After he returned, Piepie is able to perform “SHADOW CLONE JUTSU”. To enhance the productivity of his pie shop, he clones himself into piepie00 and piepie01. piepie00 and piepie01 always work separately at the same time; that is, they cannot work on the same pie simultaneously. Furthermore, one can make his next pie only when he finishes making his previous pie. They believe that they can perform the best when following the same strategy used in subproblem</li>

</ul>

(2).

Prove their daring thought or disprove with a counterexample.

<ul>

 <li>(3pts) In addition to “SHADOW CLONE JUTSU”, Piepie also learned “CHIDORI” to kill at most one of the customers. He is wondering who he kills will minimize the time needed. Please give an algorithm that runs in <em>O</em>(<em>N </em>lg<em>N</em>) time complexity and briefly explain the correctness and the time complexity of your algorithm.</li>

</ul>

<em>Note: This subproblem is not related to subproblem 4, there is only one Piepie making Pie &#x1f642;</em>

<h1>Problem 6 – Mobile Diners (Hand-Written) (14 points)</h1>

In an another world of strange dimension, there is a Natural Π University (will be called NΠU in the rest of this problem). The world is so strange that all the classrooms in NΠU are located on the only avenue, “Pineapple Avenue”. NΠU is made up of <em>N </em>classes, to simplify the problem, we assume that each class <em>i </em>locates on <em>x<sub>i</sub></em>, indicating it’s <em>x<sub>i </sub></em>units far from the entry of NΠU.

When it comes to lunch time, the students have no choice but to choose from the mobile diners. Each mobile diner has a delicious rate <em>d</em>, indicating that the students will only move at most <em>d </em>units from their classrooms to have their lunch on that mobile diner.

It’s currently the recruiting stage and there are <em>M </em>mobile diner candidates and the delicious rates are <em>d</em><sub>1</sub><em>,d</em><sub>2</sub><em>,…,d<sub>M</sub></em>, respectively. Due to the property of the strange world, the mobile diner with a smaller index should always be located on the side of a smaller coordinate. In order to reduce the personnel costs, you are asked to make a plan that makes all the students be able to have meal with fewest mobile diners.

In this problem, please assume that <em>x </em>is monotonic increasing, that is, for any <em>i &lt; j</em>, <em>x<sub>i </sub>&lt; x<sub>j</sub></em>.

<em>Note that if you use Greedy or Dynamic Programming in any subproblem of this problem, you should also prove their properties.</em>

<ul>

 <li>(2pts) Please show your plan when there are 5 classes and they locate on <em>x </em>= {1<em>,</em>7<em>,</em>11<em>,</em>12<em>,</em>17} and there are 4 mobile diner candidates and the delicious rates are <em>d </em>= {3<em>,</em>2<em>,</em>5<em>,</em>4}.</li>

 <li>(2pts) In this subproblem, please assume that all the mobile diners are identical and share the same delicious rate <em>d</em><sup>∗</sup>.</li>

</ul>

Please provide an algorithm to find the minimum number of mobile diners needed. Your algorithm should run in <em>O</em>(<em>N </em>+ <em>M</em>) time complexity. Briefly explain the correctness and why your algorithm meets the time complexity requirement.

<em>Note: You can get full credit of this problem if you answer subproblem (3) correctly.</em>

<ul>

 <li>(4pts) The president of NΠU collects dirty money from the mobile diners, and has been using an unfair priority. The priority is exactly the index of the mobile diners!</li>

</ul>

Please consider the following scenario in this subproblem: <em>For any two mobile diners with indices i &lt; j, j is picked only if i is picked.</em>. That is, if <em>K </em>mobile diners are selected, they must be the first <em>K </em>ones.

Please provide an algorithm to find the minimum number of mobile diners needed. Your algorithm should run in <em>O</em>(<em>N </em>+ <em>M</em>) time complexity. Briefly explain the correctness and why your algorithm meets the time complexity requirement.

<ul>

 <li>(6pts) The corruption was revealed and the president is forced to quit. The new president is now open and enlightened. In subproblem (4), there is no priority among the mobile diners anymore. However, the rule that mobile diners with smaller indices should locate on smaller coordinates still remains.</li>

</ul>

Please provide an algorithm to compute the minimum number of mobile diners. Your algorithm should run in <em>O</em>(<em>NM</em>) time complexity. Briefly explain the correctness and why your algorithm meets the time complexity requirement.

<h1>Problem 7 – Rainbow Rarity Rally (Hand-Written)</h1>

“Rainbow Rarity Rally” is an annual flying race held in Cloudsdale, Equestria. There are <em>N </em>≥ 7 magical rainbow candies floating in the sky on the same 2-dimensional plane, indexed from 1 to <em>N</em>. Each candy has a color from one of the seven colors of rainbow, ROYGBIV(red, orange, yellow, green, blue, indigo and violet, indexed from 1 to 7). For each color, there is at least one candy with that color. There is also a start point on the ground. A contestant needs to fly upwards from the start point on the ground to the sky, and then fly downwards back to the start point, collecting all candies in the process.

<table width="265">

 <tbody>

  <tr>

   <td width="38">1</td>

   <td width="38">2</td>

   <td width="38">3</td>

   <td width="38">4</td>

   <td width="38">5</td>

   <td width="38">6</td>

   <td width="38">7</td>

  </tr>

 </tbody>

</table>

Let <em>C </em>be an integer greater than or equal to <em>N</em>. We use <em>N </em>+ 1 points <em>p</em><sub>0</sub><em>,p</em><sub>1</sub><em>,</em>··· <em>,p<sub>N </sub></em>described in Cartesian coordinate system to represent a race. <em>p<sub>i </sub></em>= (<em>x<sub>i</sub>,y<sub>i</sub></em>), where <em>y<sub>i </sub></em>represents the vertical height of the point.(<em>x<sub>i</sub>,y<sub>i </sub></em>∈ Z<em>,</em>0 ≤ <em>x<sub>i</sub>,y<sub>i </sub></em>≤ <em>C</em>). The start point is <em>p</em><sub>0</sub>, where <em>y</em><sub>0 </sub>= 0. The <em>i</em>-th candy is on the point <em>p<sub>i</sub></em>, and has color <em>c<sub>i</sub></em>(<em>c<sub>i </sub></em>∈ Z<em>,</em>1 ≤ <em>c<sub>i </sub></em>≤ 7). In order to uphold the holy tradition of the great pegasi race, <em>y<sub>i </sub>&lt; y<sub>i</sub></em><sub>+1 </sub>for all <em>i </em>∈ {0<em>,</em>1<em>,</em>··· <em>,N </em>− 1}.

Since Equestria is a magical kingdom ruled by chromatic sapient ponies who speak English, law of physics from our world don’t apply there. Therefore, it takes a pegasus <em>f</em>(<em>i,j</em>) = (<em>x<sub>i </sub></em>−<em>x<sub>j</sub></em>)<sup>2</sup>+(<em>y<sub>i </sub></em>−<em>y<sub>j</sub></em>)<sup>2 </sup>units of time to fly from <em>p<sub>i </sub></em>to <em>p<sub>j</sub></em>.

Each contestant has to design his/her own route that satisfy the following conditions. A route consists of two parts.

<ul>

 <li>Part 1. Contestants start from <em>p</em><sub>0 </sub>and fly upwards in the sky, stopping at <em>p<sub>N</sub></em>.</li>

 <li>Part 2. Continued from part 1, contestants start from <em>p<sub>N </sub></em>and fly downwards, stopping at <em>p</em><sub>0</sub>.</li>

 <li>In order to collect all candies, for all <em>i </em>∈ {1<em>,</em>2<em>,</em>·· <em>,N</em>}<em>,p<sub>i </sub></em>is visited exactly once in the route.</li>

 <li>Contestants can fly through a candy without collecting it. For example, let <em>a </em>= (0<em>,</em>0)<em>,b </em>= (1<em>,</em>1)<em>,c </em>= (2<em>,</em>2)<em>,d </em>= (3<em>,</em>3). Both (<em>a </em>→ <em>c </em>→ <em>d </em>→ <em>b </em>→ <em>a</em>) and (<em>a </em>→ <em>b </em>→ <em>c </em>→ <em>d </em>→ <em>a</em>) are allowed.</li>

</ul>

Rainbow Dash is an ambitious pegasus athlete who aims for the trophy. She want to know the smallest amount of time required to finish the race. She has a special aerobatics called ”Sonic Rainboom” that can only be performed if for each color she collects at least one candy with that color in ”part 1” of her route. We call a route a ”Sonic-Rainboomable route” if it allows Rainbow Dash to perform ”Sonic Rainboom”. Rainbow Dash is not an egghead! She doesn’t have time to do the math! Please help her!

Formally speaking:

<ul>

 <li>A route is an integer sequence <em>a </em>of length <em>N </em>+ 2.</li>

 <li><em>a</em><sub>0 </sub>= <em>a<sub>N</sub></em><sub>+1 </sub>= 0 and each <em>i </em>∈ {1<em>,</em>2<em>,</em>·· <em>,N</em>} appears in <em>a </em>exactly once.</li>

 <li>Let <em>q </em>be an index of <em>N </em>in <em>a</em>.</li>

 <li>∀<em>i </em>∈ [0<em>,q </em>− 1]<em>,y<sub>a</sub></em><em><sub>i </sub>&lt; y<sub>a</sub></em><em><sub>i</sub></em><sub>+1</sub>.</li>

 <li>∀<em>i </em>∈ [<em>q,N</em>]<em>,y<sub>a</sub></em><em><sub>i </sub>&gt; y<sub>a</sub></em><em><sub>i</sub></em><sub>+1</sub>.</li>

 <li><em>a</em><sub>0</sub><em>,a</em><sub>1</sub><em>,</em>·· <em>,a<sub>q </sub></em>is called ”part 1” of the route.</li>

 <li><em>a<sub>q</sub>,a<sub>q</sub></em><sub>+1</sub><em>,</em>·· <em>,a<sub>N</sub></em><sub>+1 </sub>is called ”part 2” of the route.</li>

 <li>The time required to fly through a route is Σ</li>

 <li>A route is Sonic-Rainboomable if |{<em>c<sub>a</sub></em><em><sub>i </sub></em>| <em>i </em>∈ [1<em>,q</em>]}| = 7</li>

</ul>

(Task 1) (8 points) What’s the smallest amount of time required to finish the race? Please design a dynamic programming algorithm that calculates it with <em>O</em>(<em>N</em><sup>2</sup>) time complexity.

(Task 2) (6 points) Please design a dynamic programming algorithm that solves (Task 1) with <em>O</em>(<em>N</em><sup>2</sup>) time complexity and <em>O</em>(<em>N</em>) space complexity.

(Task 3) (4 points) What’s the smallest amount of time required to finish the race if Rainbow Dash wants to perform Sonic Rainboom? Please design a dynamic programming algorithm that calculates it with <em>O</em>(<em>N</em><sup>2</sup>) time complexity.

(Task 4) (2 points) Please design a dynamic programming algorithm that solves (Task 3) with <em>O</em>(<em>N</em><sup>2</sup>) time complexity and <em>O</em>(<em>N</em>) space complexity.

(Bonus) (6 points) Let <em>t<sub>OPT </sub></em>be ”the smallest amount of time required to finish the race if Rainbow Dash wants to perform Sonic Rainboom”. Let <em>a<sub>OPT </sub></em>be a route (an integer sequence) that the time required to fly through it is <em>t<sub>OPT</sub></em>. If your algorithm in (Task 4) can find <em>a<sub>OPT </sub></em>with the same time and space complexity, you get extra 6 points!

<h2>Example</h2>

An instance of the problem with <em>N </em>= 10<em>,C </em>= 50.

<table width="382">

 <tbody>

  <tr>

   <td width="29"><em>i</em></td>

   <td width="49">0</td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td width="30">4</td>

   <td width="30">5</td>

   <td width="30">6</td>

   <td width="30">7</td>

   <td width="30">8</td>

   <td width="30">9</td>

   <td width="30">10</td>

  </tr>

  <tr>

   <td width="29"><em>x<sub>i</sub></em></td>

   <td width="49">25</td>

   <td width="30">32</td>

   <td width="30">40</td>

   <td width="30">45</td>

   <td width="30">1</td>

   <td width="30">50</td>

   <td width="30">49</td>

   <td width="30">5</td>

   <td width="30">10</td>

   <td width="30">32</td>

   <td width="30">25</td>

  </tr>

  <tr>

   <td width="29"><em>y<sub>i</sub></em></td>

   <td width="49">0</td>

   <td width="30">1</td>

   <td width="30">5</td>

   <td width="30">10</td>

   <td width="30">18</td>

   <td width="30">25</td>

   <td width="30">32</td>

   <td width="30">40</td>

   <td width="30">45</td>

   <td width="30">49</td>

   <td width="30">50</td>

  </tr>

  <tr>

   <td width="29"><em>c<sub>i</sub></em></td>

   <td width="49">None</td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td width="30">4</td>

   <td width="30">5</td>

   <td width="30">6</td>

   <td width="30">7</td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

  </tr>

 </tbody>

</table>

(a) {0<em>,</em>5<em>,</em>7<em>,</em>8<em>,</em>6<em>,</em>3<em>,</em>2<em>,</em>9<em>,</em>1<em>,</em>4<em>,</em>10<em>,</em>0} is not (b) {0<em>,</em>1<em>,</em>2<em>,</em>3<em>,</em>5<em>,</em>6<em>,</em>9<em>,</em>10<em>,</em>8<em>,</em>7<em>,</em>4<em>,</em>0} is a (c) {0<em>,</em>1<em>,</em>2<em>,</em>3<em>,</em>4<em>,</em>5<em>,</em>6<em>,</em>7<em>,</em>8<em>,</em>9<em>,</em>10<em>,</em>0} is a a route. Pink arrow means flying up- route, but not a Sonic-Rainboomable Sonic-Rainboomable route. wards and blue arrow means flying route.

downwards.

<h2>Note</h2>

<ol>

 <li>You have to prove the correctness and complexity of your algorithm!</li>

 <li><strong>If you solved task 2, you get score from task 1 automatically. If you solved task 3, you get score from task 1 automatically. If you solved task 4, you get score from task 1,2,3 automatically. Start saving ink today! Save our Earth!</strong></li>

 <li><em>O</em>(1) = <em>O</em>(2) = <em>O</em>(7) = <em>O</em>(127). We all love 127 &#x1f642;</li>

</ol>

<h2>Time and Space Complexity and Computational Model</h2>

<ol>

 <li>We use Word RAM (Wikipedia contributors, 2019b) as the computational model in this problem. It is a kind of Random-access machine(Wikipedia contributors, 2019a). If you don’t want to read long articles or the following descriptions, just think of it as a single thread C program running on your personal computer.</li>

 <li>Let <em>K </em>= 2<em>C</em><sup>2</sup>(<em>N </em>+1). Let <em>T </em>be the set of integers in range [−<em>K,K</em>]. Let <em>w </em>= 1+dlog<sub>2</sub>(<em>K </em>+1)e.</li>

 <li>A <em>w</em>-bits signed integer using the two’s complement representation is the basic data structure in this problem. Let’s call it word . Obviously, we can store any <em>x </em>∈ <em>T </em>in a word .</li>

 <li>In this problem, we assumed that a word takes <em>O</em>(1) space.</li>

 <li>Assignment of a word takes <em>O</em>(1) time.</li>

 <li>Arithmetic operations (addition, subtraction, multiplication, bitwise NOT, bitwise AND, bitwise OR, bitwise XOR, bitwise left shift, bitwise right shift) of two word take <em>O</em>(1) time.</li>

 <li>Comparison operations (equal to, not equal to, greater than, less than, greater than or equal to, less than or equal to) of two word take <em>O</em>(1) time.</li>

</ol>

<h1>References</h1>

Wikipedia contributors. (2019a). <em>Random-access machine — Wikipedia, the free encyclopedia. </em>https://en.wikipedia.org/w/index.php?title=Random-access machine&amp;oldid= 915665148. ([Online; accessed 15-October-2019])

Wikipedia contributors. (2019b). <em>Word ram — Wikipedia, the free encyclopedia. </em>https:// en.wikipedia.org/w/index.php?title=Word RAM&amp;oldid=883343686. ([Online; accessed 15October-2019])