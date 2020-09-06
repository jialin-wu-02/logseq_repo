---
title: Leetcode
---

## #CAREER

## #Robinhood #Medium 755. Pour Water [[August 3rd, 2020]]
### Simulation like question, not very hard. For loop / recursion + pointers can solve it easily.

## #Hard 42. Trapping Rain Water [[August 4th, 2020]] [[Favorite Questions]]
### Given __n__ non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it is able to trap after raining.

### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FaUiQj0BAdp.png?alt=media&token=2f9beac6-be2b-4a6c-afef-ae73c9a8c6fd)

### ```javascript
Input: [0,1,0,2,1,0,1,3,2,1,2,1]
Output: 6```

### Very interesting question that can leverage the power of [[Dynamic Programming]].

### First, the brute force solution:
#### Notice that we can iterate the height array and calculate the amount of water trapped within each index by looking at the right maximum and the left maximum height and then find the minimum of the two.

### Second, the [[Dynamic Programming]] solution:
#### Since we need to iterate the height array and looking at right and left maximum height, we can do that by going over each indices' right & left maximum height in one pass. Then combine the passes' result together. Thus giving us. O(N) runtime.

## [[Leetcode]] Problem List
### Array
#### {DONE}} - Two Sum - https://leetcode.com/problems/two-sum/ 

#### {DONE}} - Best Time to Buy and Sell Stock - https://leetcode.com/problems/best-time-to-buy-and-sell-stock/ 
##### First try in two pass:
###### ```clojure
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        small_array = []
        prev_small = float("inf")
        
        for i in range(len(prices)):
            if prices[i] < prev_small:
                prev_small  = prices[i]
            small_array.append(prev_small)
        
        result = 0
        for i in range(1, len(prices)):
            if prices[i] - small_array[i - 1] > result:
                result =  prices[i] - small_array[i - 1]
        
        return result```

#### {DONE}} - Contains Duplicate - https://leetcode.com/problems/contains-duplicate/ [[August 27th, 2020]]

#### - Product of Array Except Self - https://leetcode.com/problems/product-of-array-except-self/

#### - Maximum Subarray - https://leetcode.com/problems/maximum-subarray/

#### - Maximum Product Subarray - https://leetcode.com/problems/maximum-product-subarray/

#### - Find Minimum in Rotated Sorted Array - https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/

#### - Search in Rotated Sorted Array - https://leetcode.com/problems/search-in-rotated-sorted-array/

#### - Container With Most Water - https://leetcode.com/problems/container-with-most-water/

#### - 3Sum - https://leetcode.com/problems/3sum/

### Binary
#### - Sum of Two Integers - https://leetcode.com/problems/sum-of-two-integers/

#### - Number of 1 Bits - https://leetcode.com/problems/number-of-1-bits/

#### - Counting Bits - https://leetcode.com/problems/counting-bits/

#### - Missing Number - https://leetcode.com/problems/missing-number/

#### - Reverse Bits - https://leetcode.com/problems/reverse-bits/

### Dynamic Programming
#### - Climbing Stairs - https://leetcode.com/problems/climbing-stairs/

#### - Coin Change - https://leetcode.com/problems/coin-change/

#### - Longest Increasing Subsequence - https://leetcode.com/problems/longest-increasing-subsequence/

#### - Longest Common Subsequence -

#### - Word Break Problem - https://leetcode.com/problems/word-break/

#### - Combination Sum - https://leetcode.com/problems/combination-sum-iv/

#### - House Robber - https://leetcode.com/problems/house-robber/

#### - House Robber II - https://leetcode.com/problems/house-robber-ii/

#### - Decode Ways - https://leetcode.com/problems/decode-ways/

#### - Unique Paths - https://leetcode.com/problems/unique-paths/

#### - Jump Game - https://leetcode.com/problems/jump-game/

### Graph
#### - Clone Graph - https://leetcode.com/problems/clone-graph/

#### - Course Schedule - https://leetcode.com/problems/course-schedule/

#### - Pacific Atlantic Water Flow - https://leetcode.com/problems/pacific-atlantic-water-flow/

#### - Number of Islands - https://leetcode.com/problems/number-of-islands/

#### - Longest Consecutive Sequence - https://leetcode.com/problems/longest-consecutive-sequence/

#### - Alien Dictionary (Leetcode Premium) - https://leetcode.com/problems/alien-dictionary/

#### - Graph Valid Tree (Leetcode Premium) - https://leetcode.com/problems/graph-valid-tree/

#### - Number of Connected Components in an Undirected Graph (Leetcode Premium) - https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/

### Interval
#### - Insert Interval - https://leetcode.com/problems/insert-interval/

#### - Merge Intervals - https://leetcode.com/problems/merge-intervals/

#### - Non-overlapping Intervals - https://leetcode.com/problems/non-overlapping-intervals/

#### - Meeting Rooms (Leetcode Premium) - https://leetcode.com/problems/meeting-rooms/

#### - Meeting Rooms II (Leetcode Premium) - https://leetcode.com/problems/meeting-rooms-ii/

### Linked List
#### - Reverse a Linked List - https://leetcode.com/problems/reverse-linked-list/

#### - Detect Cycle in a Linked List - https://leetcode.com/problems/linked-list-cycle/

#### - Merge Two Sorted Lists - https://leetcode.com/problems/merge-two-sorted-lists/

#### - Merge K Sorted Lists - https://leetcode.com/problems/merge-k-sorted-lists/

#### - Remove Nth Node From End Of List - https://leetcode.com/problems/remove-nth-node-from-end-of-list/

#### - Reorder List - https://leetcode.com/problems/reorder-list/

### Matrix
#### - Set Matrix Zeroes - https://leetcode.com/problems/set-matrix-zeroes/

#### - Spiral Matrix - https://leetcode.com/problems/spiral-matrix/

#### - Rotate Image - https://leetcode.com/problems/rotate-image/

#### - Word Search - https://leetcode.com/problems/word-search/

### String
#### - Longest Substring Without Repeating Characters - https://leetcode.com/problems/longest-substring-without-repeating-characters/

#### - Longest Repeating Character Replacement - https://leetcode.com/problems/longest-repeating-character-replacement/

#### - Minimum Window Substring - https://leetcode.com/problems/minimum-window-substring/

#### - Valid Anagram - https://leetcode.com/problems/valid-anagram/

#### - Group Anagrams - https://leetcode.com/problems/group-anagrams/

#### - Valid Parentheses - https://leetcode.com/problems/valid-parentheses/

#### - Valid Palindrome - https://leetcode.com/problems/valid-palindrome/

#### - Longest Palindromic Substring - https://leetcode.com/problems/longest-palindromic-substring/

#### - Palindromic Substrings - https://leetcode.com/problems/palindromic-substrings/

#### - Encode and Decode Strings (Leetcode Premium) - https://leetcode.com/problems/encode-and-decode-strings/

### Tree
#### - Maximum Depth of Binary Tree - https://leetcode.com/problems/maximum-depth-of-binary-tree/

#### - Same Tree - https://leetcode.com/problems/same-tree/

#### - Invert/Flip Binary Tree - https://leetcode.com/problems/invert-binary-tree/

#### - Binary Tree Maximum Path Sum - https://leetcode.com/problems/binary-tree-maximum-path-sum/

#### - Binary Tree Level Order Traversal - https://leetcode.com/problems/binary-tree-level-order-traversal/

#### - Serialize and Deserialize Binary Tree - https://leetcode.com/problems/serialize-and-deserialize-binary-tree/

#### - Subtree of Another Tree - https://leetcode.com/problems/subtree-of-another-tree/

#### - Construct Binary Tree from Preorder and Inorder Traversal - https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/

#### - Validate Binary Search Tree - https://leetcode.com/problems/validate-binary-search-tree/

#### - Kth Smallest Element in a BST - https://leetcode.com/problems/kth-smallest-element-in-a-bst/

#### - Lowest Common Ancestor of BST - https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/

#### - Implement Trie (Prefix Tree) - https://leetcode.com/problems/implement-trie-prefix-tree/

#### - Add and Search Word - https://leetcode.com/problems/add-and-search-word-data-structure-design/

#### - Word Search II - https://leetcode.com/problems/word-search-ii/

### Heap
#### - Merge K Sorted Lists - https://leetcode.com/problems/merge-k-sorted-lists/

#### - Top K Frequent Elements - https://leetcode.com/problems/top-k-frequent-elements/

#### - Find Median from Data Stream - https://leetcode.com/problems/find-median-from-data-stream/
