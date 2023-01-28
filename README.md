
<div class="panel panel-default" id="project-description">
  <div class="panel-body">
    <p><img src="https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/248/willy-wonka.png"><br>
<br></p>



<h2>Background Context</h2><p>This project is meant to be done by groups of two students. Each group of two should <a href="/rltoken/gIcHRL9I7i1lw2CTAll37A" title="pair program" target="_blank">pair program</a> for at least the mandatory part.</p>

<h2>Resources</h2>

<p><strong>Read or watch</strong>:</p>

<ul>
<li><a href="/rltoken/-j5MKLBlzZAC2RfJ5DTBIg" title="Sorting algorithm" target="_blank">Sorting algorithm</a> </li>
<li><a href="/rltoken/WRvrE2BaNVQFssHiUATTrw" title="Big O notation" target="_blank">Big O notation</a> </li>
<li><a href="/rltoken/ol0P7NbYVb5R31iOv4Q40A" title="Sorting algorithms animations" target="_blank">Sorting algorithms animations</a> </li>
<li><a href="/rltoken/_I0aEvhfJ66Xyob6dd9Utw" title="15 sorting algorithms in 6 minutes" target="_blank">15 sorting algorithms in 6 minutes</a> (<em><b>WARNING</b>: The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms</em>)</li>
<li><a href="/rltoken/Ea93HeEYuNkOL7sGb6zzGg" title="CS50 Algorithms explanation in detail by David Malan" target="_blank">CS50 Algorithms explanation in detail by David Malan</a></li>
<li><a href="/rltoken/21X_eaj5RGcLIL9mZv2sqw" title="All about sorting algorithms" target="_blank">All about sorting algorithms</a></li>
</ul>

<h2>Learning Objectives</h2>

<p>At the end of this project, you are expected to be able to <a href="/rltoken/b-QhraVUoSGmQ1C4QfNoFw" title="explain to anyone" target="_blank">explain to anyone</a>, <strong>without the help of Google</strong>:</p>

<h3>General</h3>

<ul>
<li>At least four different sorting algorithms</li>
<li>What is the Big O notation, and how to evaluate the time complexity of an algorithm</li>
<li>How to select the best sorting algorithm for a given input</li>
<li>What is a stable sorting algorithm</li>
</ul>



<h2>More Info</h2>

<h3>Data Structure and Functions</h3>

<ul>
<li>For this project you are given the following <code>print_array</code>, and <code>print_list</code> functions:</li>
</ul>

<pre><code>#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array &amp;&amp; i &lt; size)
    {
        if (i &gt; 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
</code></pre>

<pre><code>#include &lt;stdio.h&gt;
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i &gt; 0)
            printf(", ");
        printf("%d", list-&gt;n);
        ++i;
        list = list-&gt;next;
    }
    printf("\n");
}
</code></pre>

<ul>
<li>Our files <code>print_array.c</code> and <code>print_list.c</code> (containing the <code>print_array</code> and <code>print_list</code> functions) will be compiled with your functions during the correction.</li>
<li>Please declare the prototype of the functions <code>print_array</code> and <code>print_list</code> in your <code>sort.h</code> header file</li>
<li>Please use the following data structure for doubly linked list:</li>
</ul>

<pre><code>/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
</code></pre>

<p>Please, note this format is used for Quiz and Task questions.</p>

<ul>
<li><code>O(1)</code></li>
<li><code>O(n)</code></li>
<li><code>O(n!)</code></li>
<li>n square -&gt; <code>O(n^2)</code></li>
<li>log(n) -&gt; <code>O(log(n))</code></li>
<li>n * log(n) -&gt; <code>O(nlog(n))</code></li>
<li>n + k -&gt; <code>O(n+k)</code></li>
<li>…</li>
</ul>

<p>Please use the “short” notation (don’t use constants). Example: <code>O(nk)</code> or <code>O(wn)</code> should be written <code>O(n)</code>.
If an answer is required within a file, all your answers files must have a newline at the end.</p>
</div>

<h2>Tasks</h2>

<h3 class="panel-title">
	<a href="./0-bubble_sort.c">0-bubble_sort</a>
 </h3>
Write a function that sorts an array of integers in ascending order using the  Bubble Sort algorithm

-   Prototype:  `void bubble_sort(int *array, size_t size);`
-   You’re expected to print the  `array`  after each time you swap two elements (See example below)

Write in the file  `0-O`, the big O notations of the time complexity of the Bubble sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./1-insertion_sort_list.c">
		1. Insertion sort
	</a>
 </h3>
 
 Write a function that sorts a doubly linked list of integers in ascending order using the Insertion Sort algorithm

-   Prototype:  `void insertion_sort_list(listint_t **list);`
-   You are not allowed to modify the integer  `n`  of a node. You have to swap the nodes themselves.
-   You’re expected to print the  `list`  after each time you swap two elements (See example below)

Write in the file  `1-O`, the big O notations of the time complexity of the Insertion sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./2-selection_sort.c">
		2. Selection sort
	</a>
 </h3>
Write a function that sorts an array of integers in ascending order using the Selection Sort algorithm

-   Prototype:  `void selection_sort(int *array, size_t size);`
-   You’re expected to print the  `array`  after each time you swap two elements (See example below)

Write in the file  `2-O`, the big O notations of the time complexity of the Selection sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./3-quick_sort.c">
		3. Quick sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the  Quick Sort algorithm

-   Prototype:  `void quick_sort(int *array, size_t size);`
-   You must implement the  `Lomuto`  partition scheme.
-   The pivot should always be the last element of the partition being sorted.
-   You’re expected to print the  `array`  after each time you swap two elements (See example below)

Write in the file  `3-O`, the big O notations of the time complexity of the Quick sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case

<h3 class="panel-title">
	<a href="./100-shell_sort.c">
		4. Shell sort - Knuth Sequence
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Shell Sort algorithm, using the  `Knuth sequence`

-   Prototype:  `void shell_sort(int *array, size_t size);`
-   You must use the following sequence of intervals (a.k.a the Knuth sequence):
    -   `n+1 = n * 3 + 1`
    -   `1, 4, 13, 40, 121, ...`
-   You’re expected to print the  `array`  each time you decrease the interval (See example below).

**No big O notations of the time complexity of the Shell sort (Knuth sequence) algorithm needed - as the complexity is dependent on the size of array and gap**
 
<h3 class="panel-title">
	<a href="./101-cocktail_sort_list.c">
		5. Cocktail shaker sort
	</a>
 </h3>

Write a function that sorts a doubly linked list of integers in ascending order using the  Cocktail shaker sort  algorithm

-   Prototype:  `void cocktail_sort_list(listint_t **list);`
-   You are not allowed to modify the integer  `n`  of a node. You have to swap the nodes themselves.
-   You’re expected to print the  `list`  after each time you swap two elements (See example below)

Write in the file  `101-O`, the big O notations of the time complexity of the Cocktail shaker sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./102-counting_sort.c">
		6. Counting sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Counting Sort algorithm

-   Prototype:  `void counting_sort(int *array, size_t size);`
-   You can assume that  `array`  will contain only numbers  `>= 0`
-   You are allowed to use  `malloc`  and  `free`  for this task
-   You’re expected to print your counting array once it is set up (See example below)
    -   This array is of size  `k + 1`  where  `k`  is the largest number in  `array`

Write in the file  `102-O`, the big O notations of the time complexity of the Counting sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./103-merge_sort.c">
		7. Merge sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Merge Sort   algorithm

-   Prototype:  `void merge_sort(int *array, size_t size);`
-   You must implement the  `top-down`  merge sort algorithm
    -   When you divide an array into two sub-arrays, the size of the left array should always be <= the size of the right array. i.e.  `{1, 2, 3, 4, 5}`  ->  `{1, 2}, {3, 4, 5}`
    -   Sort the left array before the right array
-   You are allowed to use  `printf`
-   You are allowed to use  `malloc`  and  `free`  only once (only one  **call**)
-   Output: see example

Write in the file  `103-O`, the big O notations of the time complexity of the Merge sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case

<h3 class="panel-title">
	<a href="./104-heap_sort.c">
		8. Heap sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Heap Sort algorithm

-   Prototype:  `void heap_sort(int *array, size_t size);`
-   You must implement the  `sift-down`  heap sort algorithm
-   You’re expected to print the  `array`  after each time you swap two elements (See example below)

Write in the file  `104-O`, the big O notations of the time complexity of the Heap sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case
 
<h3 class="panel-title">
	<a href="./105-radix_sort.c">
		9. Radix sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Radix Sort algorithm

-   Prototype:  `void radix_sort(int *array, size_t size);`
-   You must implement the  `LSD`  radix sort algorithm
-   You can assume that  `array`  will contain only numbers  `>= 0`
-   You are allowed to use  `malloc`  and  `free`  for this task
-   You’re expected to print the  `array`  each time you increase your  `significant digit`

<h3 class="panel-title">
	<a href="./106-bitonic_sort.c">
		10. Bitonic sort
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Bitonic sort algorithm

-   Prototype:  `void bitonic_sort(int *array, size_t size);`
-   You can assume that  `size`  will be equal to  `2^k`, where  `k >= 0`  (when  `array`  is not  `NULL`  …)
-   You are allowed to use  `printf`
-   You’re expected to print the  `array`  each time you swap two elements (See example below)
-   Output: see example

Write in the file  `106-O`, the big O notations of the time complexity of the Bitonic sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case

<h3 class="panel-title">
	<a href="./1000-sort_deck.c">
		11. Quick Sort - Hoare Partition scheme
	</a>
 </h3>

Write a function that sorts an array of integers in ascending order using the Quick Sort  algorithm

-   Prototype:  `void quick_sort_hoare(int *array, size_t size);`
-   You must implement the  `Hoare`  partition scheme.
-   The pivot should always be the last element of the partition being sorted.
-   You’re expected to print the  `array`  after each time you swap two elements (See example below)

Write in the file  `107-O`, the big O notations of the time complexity of the Quick sort algorithm, with 1 notation per line:

-   in the best case
-   in the average case
-   in the worst case

<h3 class="panel-title">
	<a href="./107-quick_sort_hoare.c">
		12. Dealer
	</a>
 </h3>

Write a function that sorts a deck of cards.

-   Prototype:  `void sort_deck(deck_node_t **deck);`
-   You are allowed to use the C standard library function  `qsort`
-   Please use the following data structures:

<pre><code>typedef enum kind_e
{
    SPADE = 0,
    HEART,
    CLUB,
    DIAMOND
} kind_t;

/**
 * struct card_s - Playing card
 *
 * @value: Value of the card
 * From "Ace" to "King"
 * @kind: Kind of the card
 */
typedef struct card_s
{
    const char *value;
    const kind_t kind;
} card_t;

/**
 * struct deck_node_s - Deck of card
 *
 * @card: Pointer to the card of the node
 * @prev: Pointer to the previous node of the list
 * @next: Pointer to the next node of the list
 */
typedef struct deck_node_s
{
    const card_t *card;
    struct deck_node_s *prev;
    struct deck_node_s *next;
} deck_node_t;
</code></pre>

-   You have to push you  `deck.h`  header file, containing the previous data structures definition
-   Each node of the doubly linked list contains a card that you cannot modify. You have to swap the nodes.
-   You can assume there is exactly  `52`  elements in the doubly linked list.
-   You are free to use the sorting algorithm of your choice
-   The deck must be ordered:
    -   From  `Ace`  to  `King`
    -   From Spades to Diamonds
    -   See example below
 <pre><code>alex@/tmp/sort$ cat 1000-main.c
#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;
#include "deck.h"

void print_deck(const deck_node_t *deck)
{
    size_t i;
    char kinds[4] = {'S', 'H', 'C', 'D'};

    i = 0;
    while (deck)
    {
        if (i)
            printf(", ");
        printf("{%s, %c}", deck-&gt;card-&gt;value, kinds[deck-&gt;card-&gt;kind]);
        if (i == 12)
            printf("\n");
        i = (i + 1) % 13;
        deck = deck-&gt;next;
    }
}

deck_node_t *init_deck(const card_t cards[52])
{
    deck_node_t *deck;
    deck_node_t *node;
    size_t i;

    i = 52;
    deck = NULL;
    while (i--)
    {
        node = malloc(sizeof(*node));
        if (!node)
            return (NULL);
        node-&gt;card = &amp;cards[i];
        node-&gt;next = deck;
        node-&gt;prev = NULL;
        if (deck)
            deck-&gt;prev = node;
        deck = node;
    }
    return (deck);
}

int main(void)
{
    card_t cards[52] = {
        {"Jack", CLUB}, {"4", HEART}, {"3", HEART}, {"3", DIAMOND}, {"Queen", HEART}, {"5", HEART}, {"5", SPADE}, {"10", HEART}, {"6", HEART}, {"5", DIAMOND}, {"6", SPADE}, {"9", HEART}, {"7", DIAMOND}, {"Jack", SPADE}, {"Ace", DIAMOND}, {"9", CLUB}, {"Jack", DIAMOND}, {"7", SPADE}, {"King", DIAMOND}, {"10", CLUB}, {"King", SPADE}, {"8", CLUB}, {"9", SPADE}, {"6", CLUB}, {"Ace", CLUB}, {"3", SPADE}, {"8", SPADE}, {"9", DIAMOND}, {"2", HEART}, {"4", DIAMOND}, {"6", DIAMOND}, {"3", CLUB}, {"Queen", CLUB}, {"10", SPADE}, {"8", DIAMOND}, {"8", HEART}, {"Ace", SPADE}, {"Jack", HEART}, {"2", CLUB}, {"4", SPADE}, {"2", SPADE}, {"2", DIAMOND}, {"King", CLUB}, {"Queen", SPADE}, {"Queen", DIAMOND}, {"7", CLUB}, {"7", HEART}, {"5", CLUB}, {"10", DIAMOND}, {"4", CLUB}, {"King", HEART}, {"Ace", HEART},
    };
    deck_node_t *deck;

    deck = init_deck(cards);
    print_deck(deck);
    printf("\n");
    sort_deck(&amp;deck);
    printf("\n");
    print_deck(deck);
    return (0);
}
alex@/tmp/sort$ gcc -Wall -Wextra -Werror -pedantic  -std=gnu89 1000-main.c 1000-sort_deck.c -o deck
alex@/tmp/sort$ ./deck
{Jack, C}, {4, H}, {3, H}, {3, D}, {Queen, H}, {5, H}, {5, S}, {10, H}, {6, H}, {5, D}, {6, S}, {9, H}, {7, D}
{Jack, S}, {Ace, D}, {9, C}, {Jack, D}, {7, S}, {King, D}, {10, C}, {King, S}, {8, C}, {9, S}, {6, C}, {Ace, C}, {3, S}
{8, S}, {9, D}, {2, H}, {4, D}, {6, D}, {3, C}, {Queen, C}, {10, S}, {8, D}, {8, H}, {Ace, S}, {Jack, H}, {2, C}
{4, S}, {2, S}, {2, D}, {King, C}, {Queen, S}, {Queen, D}, {7, C}, {7, H}, {5, C}, {10, D}, {4, C}, {King, H}, {Ace, H}


{Ace, S}, {2, S}, {3, S}, {4, S}, {5, S}, {6, S}, {7, S}, {8, S}, {9, S}, {10, S}, {Jack, S}, {Queen, S}, {King, S}
{Ace, H}, {2, H}, {3, H}, {4, H}, {5, H}, {6, H}, {7, H}, {8, H}, {9, H}, {10, H}, {Jack, H}, {Queen, H}, {King, H}
{Ace, C}, {2, C}, {3, C}, {4, C}, {5, C}, {6, C}, {7, C}, {8, C}, {9, C}, {10, C}, {Jack, C}, {Queen, C}, {King, C}
{Ace, D}, {2, D}, {3, D}, {4, D}, {5, D}, {6, D}, {7, D}, {8, D}, {9, D}, {10, D}, {Jack, D}, {Queen, D}, {King, D}
alex@/tmp/sort$
</code></pre>
