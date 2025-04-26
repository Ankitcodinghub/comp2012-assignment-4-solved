# comp2012-assignment-4-solved
**TO GET THIS SOLUTION VISIT:** [COMP2012 Assignment 4 Solved](https://www.ankitcodinghub.com/product/comp2012-solved-5/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124252&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP2012 Assignment 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
FireBall

IceBall

LightningBall

FireStorm

FireCow

IceWind

LightningWind

FireRain LightningRain

The magic shop

Your system will basically have two functions. It can stock up magic (adding some quantity of it to the inventory with a price tag). It can also sell magic (removing some quantity of it, and also calculate the profit gained for your shop). The inventory system will use hashing for quick lookup of the magic. For simplicity, in this assignment, we only consider the following three collision handling strategies which are all in the open-addressing category: linear probing, quadratic probing, and double hashing. However, our design of the classes is made to be easily extensible if other collision handling strategies (e.g., separate chaining) are to be added later.

Read the manuals

Respectable computer wizards should be careful with reading the manuals and description. So please do read all the description and examples carefully. 🙂

If you need further clarifications of the requirements, please feel free to post on the Piazza (via Canvas) with the pa4 tag. However, to avoid cluttering the forum with repeated/trivial questions, please do read all the given code, webpage description, sample output, and the latest FAQ (refresh this page regularly) carefully before posting your questions. Also, please be reminded that we won’t debug any student’s assignment for the sake of fairness.

Download

Skeleton code: skeleton.zip

Please download it now, as we will refer to it from time to time in the description below. Your task is to complete the missing implementation in the given skeleton code for 5 classes:

OpenAddressingHashTable to be implemented in openAddressingHashTable.cpp

LinearProbingHashTable to be implemented in linearProbingHashTable.cpp

QuadraticProbingHashTable to be implemented in quadraticProbingHashTable.cpp

DoubleHashingHashTable to be implemented in doubleHashingHashTable.cpp

Shop to be implemented in shop.cpp

and submit them to ZINC in a zip file.

It is the destructor. You should delete the table, and all the magic stored inside.

void print() const override;

It prints the hash table. Its implementation is given. It is your task to read and understand it yourself. We are not going to explain what it does for you. Please do it now before you proceed to reading the following description as we will use it to demonstrate various operations – the hash tables you see in the examples are simply generated by this function.

Note that we always use the magic suffix string as the key for this assignment. Whenever we say key, we mean the suffix string for the magic.

bool add(Magic* magic) override;

Add the magic using its suffix as the key. Deep copy of the given magic should not be performed. That is, simple pointer assignment should be done when you add the magic to the corresponding cell.

Perform rehashing first if needed (to be described in the Hashing Example section) by calling the private function performRehashing which is to be implemented by yourself for this class as well.

You should record the number of comparisons needed to locate an available cell, namely C.

A comparison is defined as an operation that happens exactly once whenever you visit a cell for whatever. For example, for adding without any collision happening, it takes one comparison to locate an available cell (i.e., an EMPTY or DELETED cell) to add an item to it. Generally, if R collisions happen before an available cell is found, then C is simply R+1 (because one more comparison is needed to confirm/check that the available cell is actually available). Check the Hashing Example and the given test cases to better understand what a comparison is.

If the number of collisions is less than m, the addition is successful (i.e. we can find an EMPTY/DELETED cell to store the data with no more than m comparisons), so do the insertion, add C to comparisonCount, and return true. Otherwise, add m to comparisonCount and return false.

Assume all keys (i.e. the suffixes) provided in our test cases are unique.

bool remove(string key) override;

Remove the entry, according to the given key, from the table.

We always perform lazy deletions. That is, we just need to set the cell status to DELETED. Also remember to deallocate the magic stored.

You should record the number of comparisons needed to locate the cell to remove, namely C.

Similar to add, if the number of collisions is less than m, the removal is successful, so do the removal, add C to comparisonCount, and return true.

(If you encounter an EMPTY cell early during your search, you should terminate the search early and return false immediately. In that case you don’t need to wait for the number of collisions to reach m, and you should add the number of comparisons needed to reach the EMPTY cell to comparisonCount.)

Otherwise, add m to comparisonCount and return false.

Please study our examples later.

2. The getClusterSizeSortedList function should return “2,1” which has no extra spaces and no newlines in it.

Friendly reminder: if you are using input methods that have full-width characters (such as some Chinese input methods), you should make sure the comma you output is a simple English comma “,” which is different from some Chinese/full-width comma.

Example 2:

0: [Empty] | 1: [Active]

(key=Ball;hash=1;name=FireBall;price=$100;quantity=1) | 2: [Active]

(key=Storm;hash=2;name=FireStorm;price=$200;quantity=2) | 3: [Deleted] | 4: [Active](key=Rain;hash=4;name=FireRain;price=$300;quantity=3) | 5:

[Empty]

has 2 clusters. The first cluster spans cells 1 and 2, so its size is 2. The second cluster spans cell 4 only, so its size is 1. Therefore the largest cluster is the first cluster with a size of 2. The getClusterSizeSortedList function should return “2,1” which has no extra spaces and no newlines in it.

Example 3:

0: [Active](key=Storm;hash=0;name=FireStorm;price=$200;quantity=2) | 1:

[Active](key=Ox;hash=1;name=FireOx;price=$200;quantity=2) | 2: [Active] (key=Cow;hash=2;name=FireCow;price=$200;quantity=2) | 3: [Empty] | 4: [Active](key=Rain;hash=4;name=FireRain;price=$300;quantity=3) | 5:

[Active](key=Dog;hash=5;name=FireDog;price=$300;quantity=3)

has only 1 cluster of size 5, spanning cells 4, 5, 0, 1, and 2. Notice for probing purposes, we can “wrap around” the table, hence the last cell is actually connected to the first cell. You can consider the table as a circular array. Therefore, these are NOT two clusters. (4, 5) and (0, 1, 2) are actually connected as one big cluster. The getClusterSizeSortedList function should return “5” which has no extra spaces and no newlines in it.

void performRehashing();

Perform rehashing. It is just a private function that should be called by yourself when rehashing needs to be performed during add.

In the following example, we have set the printSteps flag to true, so that you can see all the details and learn what to print for the 3 operations: add, remove, and get.

You can also find the exact code used for this example in the first 9 test cases we gave to you. Please read them also.

Suppose we have a linear-probing hash table with m = 3, and a hash function int (*hash)

(string, int) = [](string s, int m) {return (int)s.length() % m; } which basically takes the string length of the input string and does mod m on it. The table will be empty at the beginning. hashTable-&gt;print() will print this table (assume hashTable points to our hash table):

0: [Empty] | 1: [Empty] | 2: [Empty]

We would also call togglePrintSteps once to enable the printing of the steps. Your program should also print those steps exactly when that option is on (on the other hand, don’t print anything yourself during add/remove/get when that option is off).

We will be using the magic suffix as the key, as mentioned.

First, we add new Magic{“Fire”, “Ball”, 100, 10} (key is “Ball” then) to it. Since the hash of the key is 4%3=1, it will be added to the cell 1.

The add function will print 2 lines (for all printing, there is no extra space at the front or the end of each line; and each line will end with exactly one endl):

hash(“Ball”) = 1 FireBall added at cell 1

It always prints the hash value of the key in the first line in this exact format and spacing. Then it will print all the steps involved. Since there is no collision, there is one step (i.e. one comparison) only and that is simply a successful add at cell 1.

Our table becomes:

0: [Empty] | 1: [Active]

(key=Ball;hash=1;name=FireBall;price=$100;quantity=10) | 2: [Empty]

Let’s also print the various statistics with function calls like this:

cout &lt;&lt; “Active cell count = ” &lt;&lt; hashTable-&gt;getActiveCellCount() &lt;&lt; cout &lt;&lt; “Accumulated comparison count = ” &lt;&lt; hashTable-&gt;getAccumulat cout &lt;&lt; “Cluster count = ” &lt;&lt; hashTable-&gt;getClusterCount() &lt;&lt; endl; cout &lt;&lt; “Largest cluster size = ” &lt;&lt; hashTable-&gt;getLargestClusterSiz cout &lt;&lt; “Cluster size list = ” &lt;&lt; hashTable-&gt;getClusterSizeSortedLi

The statistics printed would be:

Active cell count = 1

Accumulated comparison count = 1

Cluster count = 1

Largest cluster size = 1

Cluster size list = 1

Next we add new Magic{“Fire”, “Wind”, 200, 20} (key is “Wind” then) to it. Since the hash of the key is 4%3=1, there is actually one collision. The add function should print these 3 lines:

hash(“Wind”) = 1 FireWind collided at cell 1

FireWind added at cell 2

The table and statistics become:

0: [Empty] | 1: [Active]

(key=Ball;hash=1;name=FireBall;price=$100;quantity=10) | 2: [Active]

(key=Wind;hash=1;name=FireWind;price=$200;quantity=20)

Active cell count = 2

Accumulated comparison count = 3

Cluster count = 1

Largest cluster size = 2

Cluster size list = 2

If we add another magic now, rehashing will happen. Let’s see what that is first, then we continue with the example.

Rehashing

For this assignment, rehashing should be performed when the number of active cells is more than half of the hash table size, before adding the new item.

To perform rehashing, you need to take out all the items, double the size of the hash table (in practice, we should find a nearby prime number instead, but for this assignment we don’t worry about that to make your life easier :)), and insert the items back to the expanded table. The cell statuses of the cells in the expanded table will be either ACTIVE or EMPTY.

The insertion order of the items to the new table is the same as their appearance order in the old/original table Cell array. So start with adding the old table[0] to the new table, then table[1], then table[2], and so on.

Now we continue with the example. Let’s add new Magic{“Fire”, “Storm”, 300, 30} (key is “Storm” then) to it. Since, before adding the new item, we currently have 2 items in the table, and that is more than half of the table size. Rehashing has to be preformed. The add output should be exactly these 10 lines:

hash(“Storm”) = 2 Rehashing is needed! hash(“Ball”) = 4 FireBall added at cell 4 hash(“Wind”) = 4 FireWind collided at cell 4

FireWind added at cell 5 Rehashing is done!

FireStorm collided at cell 5

FireStorm added at cell 0

Notice when rehashing is needed, it prints “Rehashing is needed!” in the second line then perform the rehashing which prints the next 5 lines (which show 3 steps/comparisons, for adding the 2 old items back to the expanded table). Then “Rehashing is done!” should be printed. Finally, print all the steps needed to add the new item. In this example, actually adding the new item needs 2 more steps/comparisons. There are 5 steps/comparisons needed in total – that should be accumulated to comparisonCount as usual. Let’s see the table and statistics:

Given the magic’s name (note that it is the full name, i.e., prefix+suffix like “FireBall”), quantity, and price, add it to our inventory.

If the inventory already has this magic (magic with the same suffix in the corresponding table), then simply increase the current quantity of this magic in the table, by the specified quantity. If the provided price is different from the current price, just update the price to this new price.

If the inventory doesn’t already have this magic, then we need to add it to the corresponding hash table (e.g. fire magic must go to the fire table) using only the suffix as the key (e.g. use “Ball” as the key for “FireBall”).

The function only fails and returns false, when calling add on the corresponding table returns false. It is successful in all other cases, and returns true. E.g. assume no overflow would happen when you increase the quantity of a current magic.

Also assume the given quantity and price are positive.

bool sell(string name, int quantity);

Remove quantity of the magic with name (note that it is the full name, i.e., prefix+suffix like “FireBall”) from our inventory.

If the magic cannot be found from the inventory (i.e. get on the corresponding table returns nullptr), just return false.

If the inventory has this magic, check if there is enough stock to remove. If there is enough current stock, remove quantity from it, increase data member profit by the removed quantity multiplied by the magic’s current price, and return true. If current stock is less than quantity, do nothing and return false.

Additionally, make sure that the magic is removed from the hash table when its quantity reaches 0. (by calling remove of the hash table for it)

Assume the given quantity is positive.

To get the same accumulated comparison count as the expected output, you should do the following:

If there is enough stock to sell, get of the involved hash table (according to the prefix of the magic) should be called exactly once.

If there is not enough stock to sell, get of the involved hash table should be called exactly once.

If there is just enough stock to sell, both the get and remove of the involved hash table should be called exactly once.

void print() const;

It prints the shop profit and the inventory (all 3 tables, one by one). Its implementation is given. It is your task to read and understand it yourself. We are not going to explain what it does for you.

There are 67 given test cases of which the code can be found in the given main.cpp file.

These 67 test cases are first run without any memory leak checking (they are numbered #1 #67 on ZINC). Then, the same 67 test cases will be run again, in the same order, with memory leak checking (those will be numbered #68 – #134 on ZINC). For example, test case #70 on ZINC is actually the given test case 2 (in the given main function) run with memory leak checking.

About memory leak and other potential errors

In the grading report, pay attention to various errors reported. For example, under the “make” section, if you see a red cross, click on the STDERR tab to see the compilation errors. You must fix those before you can see any program output for the test cases below.

Make sure you submit the correct file yourself. You can download your own file back from ZINC to verify. Again, we only grade what you uploaded last to ZINC.

About any ZINC server / webpage / UI problem

Compilation Requirement

It is required that your submissions can be compiled and run successfully in our online autograder ZINC. If we cannot even compile your work, it won’t be graded. Therefore, for parts that you cannot finish, just put in dummy implementation so that your whole program can be compiled for ZINC to grade the other parts that you have done. Empty implementations can be like:

int SomeClass::SomeFunctionICannotFinishRightNow()

{ return 0; }

void SomeClass::SomeFunctionICannotFinishRightNowButIWantOtherPartsG

{

}

FAQ

Frequently Asked Questions

Q: My code doesn’t work / there is an error, here is the code, can you help me fix it?

A: As the assignment is a major course assessment, to be fair, you are supposed to work on it on your own and we should not finish the tasks for you. We might provide some very general hints to you, but we shall not fix the problem or debug for you.

Q: Can I add extra helper functions?

Q: Can I include additional libraries?

A: No. Everything you need is already included – there is no need for you to add any include statement (under our official environment).

Q: Can I use global variable or static variable such as “static int x”?

A: No.

Q: Can I use “auto”?

A: No.

Q: Can I use “goto”?

A: No.

Q: Can I use function X or class Y in this assignment?

In this particular PA, it is probably related to misuse of dynamic memory. Good luck with bug hunting!

Q: Can I use a variabe as the size of a static array?

A: No. Per the official C++ standard, which our course follows, a static array size must be a constant expression. It is an unofficial feature supported by some compiler extensions. On ZINC, we have added a compilation flag “-Werror=vla” to g++ so that violating this standard will trigger a compilation error. If you need a variable-sized array, please use dynamic arrays.

Q: Should we stop at the first EMPTY cell we find during get and remove operations? In other words, finding an EMPTY cell should be one of the stopping criteria (early termination), right?

A: Yes. There was a mistake in the description and sample output which has been fixed at 16 25pm on Apr 28th, as announced on Canvas. Sorry about that. For details, we have bolded the updated/additional description in the description of the add and remove functions, as well as the Hashing example section for you to see the update clearly.

Q: Is there anything to print with cout when the addition fails?

A: There is a given test case for that. Please study the given main.cpp file and the corresponding sample output. In general, the detailed examples on this webpage and the given test cases should be sufficient for you to infer what to print in each situation. You should study them to verify / help with your own understanding of the requirements.

Q: In the case where we encounter an EMPTY cell during the get and remove operations, how many comparisons/steps should we add to the “accumulated comparison count”?

A: You just need to add to it the number of comparisons needed to reach the EMPTY cell. You can find an example of it in the Hashing example section. We just added this clarification to the function description for get and remove to make it clearer at 11 50am on Apr 29th.

Q: For stockUp, how many get and add function calls should be made to arrive at the same “accumulated comparison count” as the expected output?

A: It is basically the minimal number of operations required. You can follow this guideline:

get should always be called exactly once in all scenarios.

Only call add exactly once when the item needs to be added to the table.

Q: For add, can I assume magic won’t be a nullptr?

A: Yes.

Q: For stockUp, can I assume the given magic name is valid? For example, its prefix must be “Fire”, “Ice”, and “Lightning”, right?

A: Yes. In general you can assume all inputs are valid.

Q: For performRehashing, what should we do to the DELETED cells?

A: Since the whole point of rehashing is to “start over” with a bigger table in a sense. You should just ignore the DELETED cells, and only add the ACTIVE cells back to the new table, you won’t have any DELETED cell left after the expansion as a result.

Q: For get and remove, what should we do when we encounter a DELETED cell?

A: See this post.

Q: For add, it seems that it is impossible to return false if we perform rehashing to enlarge the table whenever there is not enough space?

Q: For sell, it said ” (i.e. get on the corresponding table returns false)”, it actually meant nullptr, right?

Q: Why is there no step messages printed in the test cases when sell and stockUp are tested? On the other hand, why there are step messages printed when some of the test cases are tested? When should I print the messages?

A: This post should help.

Anyway, it is not something you need to worry about. We won’t have such extreme cases.
