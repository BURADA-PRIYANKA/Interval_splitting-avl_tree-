# Interval_splitting_inbuilt_map

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
