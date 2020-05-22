# Interval_splitting-avl_tree-

Problem Description:- 
Input - A set of real numbers which initially contains the epsilon value followed by certains points.
What is to be done - The input is to be taken point by point and for each point we are supposed to merge that point with an interval if it lies at a distance less than epsilon(an input parameter) from one of the points in that interval else a new interval is supposed to be created which contains only this point.
Output- Set of intervals.

Code:
The input is taken from a file containing doubles. The first double of the file contains the epsilon value and the rest doubles are the input values separated by a space.
The intervals are stored in an ordered map. The key of the map is a double which consists the lower bound of the interval being represented by it while the corresponding value is a vector pair which consists of the lower bound followed by the upper bound.
Each point in the form of double is taken and then by using an iterator we go from each interval to the next in the ascending order of the lower bound of the intervals. Checking for the sufficient conditions that point is included into the existing interval or a new interval is created.

Time Complexity:
The worst case time complexity of the present code is O(n^2). Because, with the use of the inbuilt iterator, the traversal is in the ascending order of the lower bound. When we are supposed to add the largest element always then the time complexity would be O(1)+O(2)+O(3)+......O(N). When N is sufficiently large this time complexity will be O(N^2).

Code:
The input is taken from a file containing doubles.The first double of the file contains the epsilon value and the rest doubles are the input values separated by a space.
The intervals are stored in an avl tree. Each avl tree node in this project contains two double pointers namely key and value along with right and left child pointers similar to those of the general trees. Key is the lower bound of that interval corresponding to that node and value is the upper bound of the same. The key is the criteria which is used to compare the nodes and to balance the tree. 
Each point in the form of double is read from the input file and with each node it encounters it is checked whether the point can be merged with that node else to which subtree(left or right) is the search for the required node to be continued. If there is no node with which it can be merged then a new node is created whose key and value are the same and are equal to the point to be added, else the previous(left childs rightmost child) or post(right childs leftmost child) nodes are checked if necessary.
Finally, the required output is given to a file.

Time Complexity:
The worst case time complexity of this code is O(nlogn).As each insertion is made sure to be of O(logi) where i is the number of intervals that are present at the time of adding a point and O(log1)+O(log2)+O(log3)+......O(logn) = O(nlogn) when n is sufficiently large.
