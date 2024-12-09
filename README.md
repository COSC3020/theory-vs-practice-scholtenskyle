# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  Things like lower order terms may be ignored in asymptotic analysis, but obviously wouldn't be ignored in practice as everything is used. Even just this one example leads to more inputs in practice.

  Optimization of the code's use of hardware always has an impact on the performance of the code. If it is not optimized properly to utilize resources efficiently, the code may run slow in practice. For example, sometimes things like a GPU can be used in hardware acceleration to help optimize a program.

  The third reason is that asymptotic analysis is theoretical. You need to actually test it to get real data, as there may be differences based on things such as inputs alone, or unexpected issues that the user may come across.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  Using logarithms we find that the search time for 10000 elements is 1.33 times longer than that for 1000 elements, so it would take 6.65 seconds. I did use ChatGPT to help with this.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  Poorly managed trees drastically effect runtime, where they may not have the desired amount of children, or one "side" may have significantly more elements than the other. For instance, if a binary tree where not balanced properly, with one side containing many more elements than the other, this could affect runtime. This would only affect larger data sets if the balancing was done, but not properly (where the further down the tree you go, the less organized it becomes). When these trees are unbalanced, it would increase the runtime as the expected organization does not exist. This could make the runtime approach O(n) instead of O(logn).

  Different languages have different best uses for them too, which would affect performance, such as using C++ vs Java, where C++ could potentially perform better because of the better freedoms with memory allocation. You could potetially only allocate memory properly for a few iterations of code, where it starts becoming a mess after that. This would increase runtime, as the code may have to keep checking for available pointers to store memory if not done properly, or may have a more "roundabout" way of storing data which would take more time. Especially if this dataset was so large that it couldn't fit within something like the cache, it would have to use slower memory which of course would slow the program down.

  Background processes or other applications can consume resources, such as using the CPU. This of course would leave less resources for the program you are trying to run. This can negatively affect the search as it can't use all aspects of a computer to search as quickly as possible.

Add your answers to this markdown file.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
