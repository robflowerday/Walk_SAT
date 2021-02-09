# Walk_SAT

This is an algorithm for determining the satisfiability of a sentence written in conjunctive normal form.

This algorithm starts by building a model which assigns all propositions in the sentence to be True or False at random.
It then checks whether this model satisfies the sentence. If the sentence is satisfies the algorithm finishes and returns the model that satisfies the sentence.
If it does not satisfy the sentence, the algorithm takes an unsatisfied clause and 'flips the truth value of the symbol' that is, if the proposition is True in the model, it turns it to False, and vice versa.
It then checks the model again and returns the model if it satisfies the sentence, or continues otherwise.

These steps are repeated until either a model is returned or the number of flips that takes place exceeds the maximum flip count given. In which case the algorithm gives up and returns False, wothout a solution.

This algorithm can never proove that an algorithm is unsatisfiable, only that it is satisfiable, or that it is probably not.
This is because it holds no memory of states that have been checked, so given an infinite number as the maximum number of flips, though it may seem the algorithm would be complete, instead if the sentence is unsatisfiable, the algorithm would never terminate - and so is not complete.

This algorithm is better than the similar DPLL algorithm, which is more systematic, is complete and does not utilise randomness in some instance (with regards to speed) and worse in others.
An approach that uses both algorithms is best for a complex problem.
