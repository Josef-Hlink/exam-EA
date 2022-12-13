# Evolutionary Algorithms - Practice Exam 2022

## Multiple choice - 20 questions with 60 points

- ***Each problem has a variable number of correct statements***
- ***There is always at least one correct statement for each question***
- ***All correct statements are marked: 3 points***
- ***Correct statement(s) is/are partially marked without a wrong answer: 1 point***
- ***A wrong statement is marked: 0 points***

---

### Question 1

> Which statement(s) are characteristics of the evolutionary algorithms?

<!-- A -->
A. Evolutionary algorithms require no fitness gradient information of any kind to proceed.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
Evolutionary algorithms do not require any fitness gradient information, as they are based on the principle of natural selection.
This means that they do not take into consideration the fitness gradient of the a given current solution, which would be defined as the relative change in fitness compared to previous solutions.
They rather the fitness of the current solution compared to the fitness values of the solutions in the population.
</p> </details> <br>

<!-- B -->
B. Evolutionary algorithms are easy to process in parallel and can escape from local minima where deterministic optimization methods may fail.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
Evolutionary algorithms are easy to process in parallel, because many solutions can be evaluated individually at once.
They can also escape from local minima, because of their stochastic nature.
</p> </details> <br>

<!-- C -->
C. Evolutionary algorithms are local random search algorithms.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
Evolutionary algorithms are not local random search algorithms.
One could say that they are like random search algorithms, but they differ in that they actually use the fitness values of the solutions in the population to select the best solutions.
</p> </details> <br>

<!-- D -->
D. Evolutionary algorithms require presumptions with respect to the problem space.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
Evolutionary algorithms do not require any presumptions with respect to the problem space.
They are not based on any specific problem, but rather on the simple principle of natural selection.
It is important to note however, that some variations evolutionary algorithms do benefit from problem-specific knowledge, such as for the initialization of σ values in <i>Evolution Strategies</i>.
</p> </details> <br>


### Question 2

> Regarding exploration and exploitation in EAs, which statement(s) is/are correct?

<!-- A -->
A. Exploration relates to local search and exploitation relates to global search.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
<i>Exploration</i> is defined as the process of searching for new solutions, and <i>exploitation</i> is defined as the process of using the current best solution to find a better solution.
Local search describes the process of searching for a better solution in the neighborhood of the current parent solution, while global search describes the process of selecting the best solutions from the entire population.
</p> </details> <br>

<!-- B -->
B. Crossover operators have the ability to jump out of a local optimum.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
Crossover operators do not have the ability to jump out of a local optimum.
They are used to combine the best solutions from the population, and therefore they do not have the ability to search for a better solution outside of a local optimum if the population is already stuck.
</p> </details> <br>

<!-- C -->
C. Mutation operators can search for an optimum near the parent.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
This is quite literally what mutation does.
It mutates the parent solution, and therefore it can search for a better solution near the parent.
</p> </details> <br>

<!-- D -->
D. Going too far into exploration will get you stuck in local optima.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
If the current best solution is very close to the global optimum, it is not beneficial to search for a better solution too far out of the neighborhood of this current one.
This is because the probability of finding a better solution is very low, and therefore it is better to search for a better solution in the neighborhood of the current best solution.
</p> </details> <br>


### Question 3

> Two state-of-the-art discrete problems are OneMax ( $f_\mathrm{OM}(\mathbf{x}) = \sum_{i=1}^n x_i$ ) and BinaryValue ( $f_\mathrm{BV}(\mathbf{x}) = \sum_{i=1}^n x_i \cdot 2^{n-i}$ ). Which statement(s) is/are correct regarding solving these two problems by EAs?

<!-- A -->
A. Compared to $f_\mathrm{BV}$, $f_\mathrm{OM}$ is easier to optimize, because there is a strong fitness-distance correlation in $f_\mathrm{OM}$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
Fitness-distance correlation is defined as the correlation between the fitness and the number of mutations required to reach the optimum.
In <i>OM</i>, the fitness is equal to the number of ones in the solution, and the number of mutations required to reach the optimum is equal to the number of zeros in the solution.
Therefore, there is a very strong fitness-distance correlation in <i>OM</i>.
This is not the case in BV, where the fitness is equal to the sum of the binary values of the solution, and the number of mutations required to reach the optimum is equal to the number of zeros in the solution.
Therefore, there is no strong fitness-distance correlation in <i>BV</i>.
</p> </details> <br>

<!-- B -->
B. Compared to $f_\mathrm{BV}$, $f_\mathrm{OM}$ is easier to optimize, because $f_\mathrm{OM}(\mathbf{x})$ is a monotonically strictly increasing function.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
We can not say that the function is monotonically strictly increasing, because the function is not strictly increasing for all values of <i>x</i>.
That is, the order of <i>x</i> is not defined, so we can not state that for any a, b, where a < b, f(a) < f(b).
</p> </details> <br>

<!-- C -->
C. Compared to $f_\mathrm{OM}$, $f_\mathrm{BV}$ is easier to optimize, because each variable in a decision vector has a different weight in the BinaryValue function.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
While it is true that each variable in a decision vector has a different weight in the BinaryValue function, this does not make the problem easier to optimize.
</p> </details> <br>

<!-- D -->
D. $f_\mathrm{OM}$ and $f_\mathrm{BV}$ have the same difficulty to optimize, as only the Hamming distance to the optimum determines the quality of search.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
The Hamming distance is defined as the number of bits that differ between two solutions.
While it is true that the Hamming distance is equal to the number of mutations required to reach the optimum in both problems (i.e. the number of zeros in the current solution), this is not the only factor that determines the quality of search.
</p> </details> <br>


### Question 4

> Suppose the computational complexity of an optimization algorithm is $\Theta(n^2 \log n)$, where $n$ represents the number of elements in a decision vector. Which interpretation(s) is/are correct?
> Suppose $c$ and $C$ are two constants, and $0 < c < C \ll \infty$ in the following statements.

<!-- A -->
A. There exists a constant $C>0$ such that for all $n$ the expected runtime is at most $Cn^2 \log n$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
The Theta-complexity on an algorithm is defined as the bounds on the worst-case runtime of an algorithm.
Therefore, the expected runtime of an algorithm is always at most the Theta-complexity of the algorithm with upper bound Cn^2 log n.
</p> </details> <br>

<!-- B -->
B. There exists a constant $C>0$ such that for all $n$ the expected runtime is at least $Cn^2 \log n$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
C denotes the upper bound, not the lower bound.
</p> </details> <br>

<!-- C -->
C. There exists a constant $c>0$ such that for all $n$ the expected runtime is at most $cn^2 \log n$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
c denotes the lower bound, not the upper bound.
</p> </details> <br>

<!-- D -->
D. There exists a constant $c>0$ such that for all $n$ the expected runtime is at least $cn^2 \log n$.  

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
c indeed denotes the lower bound, and the expected runtime is always at least the Theta-complexity of the algorithm with lower bound cn^2 log n.
</p> </details> <br>


### Question 5

> We denote $T(n) = 2n \times n + 3C$ and $T'(n) = n + 1000$ as the running time of the algorithms $A$ and $B$, respectively, where $n$ is the dimension of the given problem and $C$ is constant. Which statement(s) is/are correct?

<!-- A -->
A. The algorithm $A$ is linear time $O(n)$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
It is quadratic time (O(n^2)).
</p> </details> <br>

<!-- B -->
B. The algorithm $A$ is quadratic time $O(n^2)$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
<i>n</i> is multiplied by itself, so the complexity is quadratic.
</p> </details> <br>

<!-- C -->
C. The algorithm $B$ is linear time $O(n)$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
<i>n</i> is multiplied by 1, so the complexity is linear.
</p> </details> <br>

<!-- D -->
D. $A$ is faster than $B$ for large $n$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
While it is true that <i>A</i> is faster than <i>B</i> for small <i>n</i> (assuming <i>C</i> is small too), this is not the case for large <i>n</i>, because <i>A</i> is quadratic, while <i>B</i>'s performance scales linearly.
</p> </details> <br>


### Question 6

> Given a bitstring (ie., individual) $a = (01011100)$ and a mutation operator $m_p: \{0,1\}^8 \rightarrow \{0,1\}^8$ that inverts single bits independently of each other with probability $p \in [0,1]$. Which statement(s) is/are correct?

<!-- A -->
A. The total probability that 3 out of 8 bits are changed by mutation is $15p^3(1-p)^5$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
The answer is almost correct, but the number of combinations is wrong.
The probability for flipping x out of y bits with probability p is y choose x p^x (1-p)^(y-x).
8 choose 3 is 56, not 15, so the probability is 56p^3(1-p)^5.
</p> </details> <br>

<!-- B -->
B. $P(a \rightarrow 10101011)$ is $p^7$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
7 bits are flipped in this case, so the probability of flipping all those exact 7 bits is p^7.
</p> </details> <br>

<!-- C -->
C. $P(a \rightarrow a)$ is $1$.

<details> <summary> <i> see answer </i> </summary>
<b>False</b> <br> <p>
The probability of flipping no bits is (1-p)^8, not 1.
It is possible, but the probability p would have to be set to 0.
</p> </details> <br>

<!-- D -->
D. The total probability that $i (0 \leq i \leq 8, i \in \N)$ out of 8 bits are changed by mutation is $8Ci \times p^i (1-p)^{8-i}$.

<details> <summary> <i> see answer </i> </summary>
<b>True</b> <br> <p>
This is the correct formula for the probability of flipping i out of 8 bits with probability p.
</p> </details> <br>
