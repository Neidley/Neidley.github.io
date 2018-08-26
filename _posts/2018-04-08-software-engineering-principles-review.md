---
layout: post
title: Software Engineering Principles Review
---

### 1. Understand the differences between the data structures and trade-offs (array vs linked list, hash tables, trees, etc.) Don't worry about implementation just understand how they're built and what they're good for.

---

#### _Linked-Lists_

[_About Linked List Data Structures_](https://github.com/Neidley/sep-assignments/tree/master/01-data-structures/03-linked-lists)

Linked list's read, create, and delete methods were all much slower than array's
same methods.

Arrays utilize Spacial Locality. Linked Lists allow utilization of additional
memory.

#### _Hashes_

[_Hashes pt 1_](https://github.com/Neidley/sep-assignments/tree/master/01-data-structures/04-hashes-part-1)

[_Hashes pt 2_](https://github.com/Neidley/sep-assignments/tree/master/01-data-structures/05-hashes-part-2)

##### _Open addressing_

_makes sure underlying array is not resized during
insertion unless the underlying array is indeed full._

##### _Separate chaining_

_utilizes linked-lists to "chain" off underlying array's
indexes. An Insertion first checks if index returned from
hashing function is occupied.
If so, the last node is found on any potential existing linked-list,
(of which the @next attribute is NIL) and the new item insertion is complete._

#### _Trees_

##### _Binary Search Trees_

[_Binary Tree_](https://github.com/Neidley/sep-assignments/tree/master/01-data-structures/06-trees)

* Maintains one root node off which all others branch off. Each node has at most, 2 adjoined nodes. Each node's left and right attributes are written according to that nodes' value.

###### _Min/Max Binary Heap_

_Has all the properties of a Binary Search Tree but also organizes row by value with either the maximum value node as the root (max binary heap) or the minimum value node is the root (min binary heap)_

### 2. Understand what Object Relational Mapping is (Conceptually, nothing code related. You should have learned this with Ruby.)

---

#### _Object Relational Mapping, or ORM_

_provides a way for Rails developers to manipulate a database using Ruby, rather than writing SQL. Rails employs an ORM library named ActiveRecord to provide this translation service._

#### _Rails Console_

_Provides command line access to a Rails application and Ruby._

#### _SQL_

_SQL is a language for communicating with a relational database._

#### _Object Relational Mapping_

_Object-Relational Mapping (ORM) is a design pattern that connects the objects of an application to tables in a database. Using ORM, the properties and relationships of objects in an application can be connected to a database without the need to write SQL statements._

#### _ActiveRecord_

_ActiveRecord is Rails' ORM library._

### 3. Understand all the O time complexities and what they mean/signify.

---

#### _O(1)_

_Read as "constant time" or "Big-O of constant time". No matter the size of
n, the algorithm always takes the same amount of time to execute. This is the
fastest an algorithm can operate._

#### _O(logn)_

_Read as "logarithmic time" or "Big-O of logarithmic time". As the size of n
grows, the time it takes the algorithm to execute and complete grows faster
than constant time. Logarithmic time algorithms are slower than constant time
algorithms._

#### _O(n)_

_Read as "linear time" or "Big-O of linear time". As the size of n grows, the
time it takes the algorithm to execute and complete grows at the same rate.
Linear time algorithms are slower than constant time algorithms._

#### _O(nlogn)_

_Read as "loglinear time" or "Big-O of loglinear time". As the size of n grows,
the time it takes the algorithm to execute and complete grows faster than constant
time. Loglinear time algorithms are slower than linear time algorithms._

#### _O(n2)_

_Read as "quadratic time" or "Big-O of quadratic time". As n grows, the time
it takes the algorithm to execute grows faster than loglinear time. This is
considered a slow efficiency classification. Quadratic time algorithms are
slower than loglinear time algorithms and overall considered relatively slow,
but still usable._

#### _O(2n)_

_Read as "exponential time" or "Big-O of exponential time". As n grows, the
time it takes the algorithm to execute grows much faster than quadratic time.
Algorithms with this complexity are very slow, and in most cases unusable._

### 4. Be able to identify all of the sorts you encountered. Once again no need for implementing them, but you should be able to identify them given some code. You should know the time complexities of them as well.

---

#### [_Insertion Sort_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-sorting/insertion_sort.rb)

_Moves items from an unsorted collection to a new, sorted collection by inserting
items in their proper place one at a time. This algorithm has poor performance
compared to other sorting algorithms.
Big 0(n2)_

#### [_Selection Sort_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-sorting/selection_sort.rb)

_Selects the item which should be sorted "next" and moves it to the front
(or back) of the collection. Selection sort has poor performance compared to
other sorting algorithms.
Big 0(n2)_

#### [_Bubble Sort_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-sorting/bubble_sort.rb)

_Passes through a collection multiple times. In each pass, it compares adjacent
items and swaps them according to the desired sorting order. The algorithm
finishes when there are no swaps done for a complete pass. Bubble sort has
poor performance when compared to other sorting algorithms.
Big 0(n2)_

#### [_Merge Sort_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-sorting/merge_sort.rb)

_Breaks the collection into sub-collections and sorts each sub-collection.
Sorted sub-collections are merged together (using recursion) to form larger
sorted collections until the entire collection is sorted. Merge sort has good
performance compared to other sorting algorithms.
Big O(nlogn)_

#### [_Quick Sort_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-sorting/quick_sort.rb)

_Picks a pivot point and compares each item to the pivot point. It moves each
item according to the pivot point. When there are no more items to move in
the first iteration, these steps are repeated for the "left" and "right" sides
of the collection. Quick sort has good performance compared to other sorting algorithms.
Big O(nlogn)_

### 5. [Study LEFT, RIGHT, and INNER join.](https://github.com/Neidley/relational-database-fundamentals/tree/master/fundamental-sql-commands)

---

```
SELECT department.name, professor.name
FROM department
LEFT OUTER JOIN professor
ON professor.department*id = department.id;
```

### 6. Be able to write a linear search and binary search and know the associated runtimes.

---

#### _Binary Search_

[_Binary Search iterative_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-searching/binary_search_iterative.rb)

[_Binary Search recursive_](https://github.com/Neidley/algorithms-and-complexity/blob/master/algorithms-searching/binary_search_recursive.rb)

_The best case scenario for binary search is if the collection being searched through has only one item, such that the algorithm has 0(1). If the collection only has one item, then in the binary search high, low, and mid are all equal at which point the method returns "not found"/nil or the item at the sole index._

_The worst case scenario for binary search is if the input collection approaches an infinite size. In this case, the collection will have to be cut in half more times but that's not so bad because on first iteration you're still throwing away half of an infinite collection of items. Because of this, binary search in it's worst case has O(log n)._

#### What is the Big-O of binary search?

_O(log n). Worst case of binary search is log n_

#### What is the Big-Ω of binary search?

_Ω(1). Best case for binary search is constant_

#### What is the Big-Ө of binary search?

_Ө(logn). Average case for binary search is log n._

### 7. [Be able to design a database and write CREATE TABLE statements.](https://github.com/Neidley/relational-database-fundamentals/blob/master/fundamental-sql-commands/fundamental-sql-commands-assignment.txt)

---

Example:

```
CREATE TABLE boat (
id integer PRIMARY KEY NOT NULL,
type text NOT NULL,
license\*plate varchar(7) NOT NULL,
owner\*id integer REFERENCES owner(id)
);
```

### [8. Be able to utilize JOINS and subqueries in a query.](https://github.com/Neidley/relational-database-fundamentals/tree/master/JOIN-statements)

---

### 9. Understand the purpose of normalization and denormalization

---

#### Benefits of data normalization:

#### _Data integrity:_

* not only does normalization reduce data duplication, since there is no
  redundant, neglected data, normalization prevents update anomalies (mistakes)
  and data inconsistencies.

#### _Optimized queries:_

_normalized tables group data more logically, and produce rapid, efficient joins._

_Faster index creation and sorting (since the tables have fewer columns)_

_Faster update performance (since there are fewer indexes per table)_

_Improved concurrency resolution (since table locks will affect less data)_

#### _Data Denormalization_

* If data normalization aims to reduce redundancy, data denormalization is
  a process performed on a previously-normalized database to increase read performance.

#### _Methods of denormalization_

Common techniques for denormalization in database design include:

_Adding redundant groups_

_Adding derived columns_

_Combining tables_

_Repeating groups_

_Creating extract tables_

_Partitioning relations_
