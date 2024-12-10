# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  Things like lower order terms may be ignored in asymptotic analysis, but obviously wouldn't be ignored in practice as everything is used. Even just this one example leads to more inputs in practice.

  Optimization of the code's use of hardware always has an impact on the performance of the code. If it is not optimized properly to utilize resources efficiently, the code may run slow in practice. For example, sometimes things like a GPU can be used in hardware acceleration to help optimize a program. Or even the addition of RAM, or using a cache can have a major impact.

  The third reason is that asymptotic analysis is theoretical. You need to actually test it to get real data, as there may be differences based on things such as inputs alone, or unexpected issues that the user may come across. Of course you can calculate things like runtime, but there are going to be things that aren't taken into account. This could be things such as background processes running, which take up resources. Calculations can't ever be 100% accurate as there are tiny details that impact it along the way, which is why testing it is so important.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  Using logarithms we find that the search time for 10000 elements is 1.33 times longer than that for 1000 elements, so it would take 6.65 seconds. I did use ChatGPT to help with this. The reason I used logarithms is because the asymptotic complexity of a binary search tree is O(logn). If it wasn't a binary search tree we could use something like $$O(n^2)$$ or O(n!), depending on the case.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  Poorly managed trees drastically effect runtime, where they may not have the desired amount of children, or one "side" may have significantly more elements than the other. For instance, if a binary tree where not balanced properly, with one side containing many more elements than the other, this could affect runtime. This would only affect larger data sets if the balancing was done, but not properly (where the further down the tree you go, the less organized it becomes). When these trees are unbalanced, it would increase the runtime as the expected organization does not exist. This could make the runtime approach O(n) instead of O(logn). If the tree were completely unbalanced, the runtime would be O(n). This could account for such a bg diffeence, if it was expected that everything would already be sorted.

  The different data types stored in the tree would affect runtime, and could potentially drastically change it with enough elements. For example, if you have a tree of strings, and a tree of integers, the tree of integers would almost certainly run faster. This is because it simply doesn't take as much resources to work with something as simple as an integer versus a string. Yes this would affect a smaller data set as well as a larger one, but it would do more harm to a large data set purely becuase it has to deal with this setback many more times, which increases the runtime.

  Background processes or other applications can consume resources, such as using the CPU. This of course would leave less resources for the program you are trying to run. This can negatively affect the search as it can't use all aspects of a computer to search as quickly as possible. This would affect both small and larger data sets, but the effect would be multiplied as there are more actions to be performed for a larger data set. This could be made even worse with needing to sort many more elements than a small data set, with even less resources. It would then take drastically more time just to sort a single element.

Add your answers to this markdown file.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
