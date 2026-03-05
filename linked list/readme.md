\# Add Two Numbers (Linked List)



Given two linked lists where digits are stored in \*\*reverse order\*\* (head = ones place), add the two numbers and return the sum as a linked list.



\## Approach (Very Simple)

We simulate normal addition with carry, building the result via a dummy head + tail:



1\. Read digits safely  

&nbsp;  `x = (l1 != null ? l1.val : 0)`  

&nbsp;  `y = (l2 != null ? l2.val : 0)`

2\. `sum = x + y + carry`

3\. New digit = `sum % 10`

4\. Update `carry = sum / 10`

5\. Move `l1`, `l2` if not null

6\. Loop until both lists and carry are done:

&nbsp;  `while (l1 != null || l2 != null || carry != 0)`



\## Complexity

\- \*\*Time:\*\* `O(max(m, n))`

\- \*\*Space:\*\* `O(1)` auxiliary



\## Example

Input: `l1 = \[2,4,3]`, `l2 = \[5,6,4]`  

Output: `\[7,0,8]` (807)

