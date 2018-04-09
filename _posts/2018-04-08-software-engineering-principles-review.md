Bloc.io - Module 5 - Software Engineering Principles Study Guide

  1. Understand the differences between the data structures and trade-offs (array vs linked list, hash tables, trees, etc.)
  Don't worry about implementation just understand how they're built and what they're good for.

    Linked-Lists

      About Linked List Data Structures:
      https://github.com/Neidley/sep-assignments/blob/checkpoint-3-linked-lists/01-data-structures/03-linked-lists/linked-lists-answers.txt

      Linked list's read, create, and delete methods were all much slower than array's same methods.

      Arrays utilize Spacial Locality. Linked Lists allow utilization of additional memory.

    Hashes

      Open addressing

        - makes sure underlying array is not resized during
          insertion unless the underlying array is indeed full.

      Separate chaining

        - utilizes linked-lists to "chain" off underlying array's
          indexes. An Insertion first checks if index returned from
          hashing function is occupied.
          If so, the last node is found on any potential existing linked-list,
          (of which the @next attribute is NIL) and the new item insertion is complete.

    Trees

      Binary Search Trees

        - Maintains one root node off which all others branch off

        - Each node has at most, 2 adjoined nodes

        - Each node's left and right attributes are written according to
        that nodes' value.

      Min/Max Binary Heap

        - Has all the properties of a Binary Search Tree but also organizes
          row by value with either the maximum value node as the root (max binary heap) or the minimum value node is the root (min binary heap)

  2. Understand what Object Relational Mapping is. Conceptual, nothing code related. You should have learned this with ruby.

    "Object Relational Mapping, or ORM is similar to a translation service, in that it provides a way for Rails developers to manipulate a database using Ruby, rather than writing SQL. Rails employs an ORM library named ActiveRecord to provide this translation service."
    - Bloc.io

    Rails Console

      - Provides command line access to a Rails application and Ruby.

    SQL

      -	SQL is a language for communicating with a relational database.

    Object Relational Mapping

      - Object-Relational Mapping (ORM) is a design pattern that connects the objects of an application to tables in a database. Using ORM, the properties and relationships of objects in an application can be connected to a database without the need to write SQL statements.

    ActiveRecord

      - ActiveRecord is Rails' ORM library.

  3. Understand all the O time complexities and what they mean/signify.

    O(1)
      Read as "constant time" or "Big-O of constant time". No matter the size of n, the algorithm always takes the same amount of time to execute. This is the fastest an algorithm can operate.

    O(logn)
      Read as "logarithmic time" or "Big-O of logarithmic time". As the size of n grows, the time it takes the algorithm to execute and complete grows faster than constant time. Logarithmic time algorithms are slower than constant time algorithms.

    O(n)
      Read as "linear time" or "Big-O of linear time". As the size of n grows, the time it takes the algorithm to execute and complete grows at the same rate. Linear time algorithms are slower than constant time algorithms.

    O(nlogn)
      Read as "loglinear time" or "Big-O of loglinear time". As the size of n grows, the time it takes the algorithm to execute and complete grows faster than constant time. Loglinear time algorithms are slower than linear time algorithms.

    O(n2)
      Read as "quadratic time" or "Big-O of quadratic time". As n grows, the time it takes the algorithm to execute grows faster than loglinear time. This is considered a slow efficiency classification. Quadratic time algorithms are slower than loglinear time algorithms and overall considered relatively slow, but still usable.

    O(2n)
      Read as "exponential time" or "Big-O of exponential time". As n grows, the time it takes the algorithm to execute grows much faster than quadratic time. Algorithms with this complexity are very slow, and in most cases unusable.

  4. Be able to identify all of the sorts you encountered. Once again no need for implementing them, but you should be able to identify them given some code. You should know the time complexities of them as well.

    Insertion Sort
      Moves items from an unsorted collection to a new, sorted collection by inserting items in their proper place one at a time. This algorithm has poor performance compared to other sorting algorithms.

    Selection Sort
      Selects the item which should be sorted "next" and moves it to the front (or back) of the collection. Selection sort has poor performance compared to other sorting algorithms.

    Bubble Sort
      Passes through a collection multiple times. In each pass, it compares adjacent items and swaps them according to the desired sorting order. The algorithm finishes when there are no swaps done for a complete pass. Bubble sort has poor performance when compared to other sorting algorithms.

    Merge Sort
      Breaks the collection into sub-collections and sorts each sub-collection. Sorted sub-collections are merged together (using recursion) to form larger sorted collections until the entire collection is sorted. Merge sort has good performance compared to other sorting algorithms.

    Quick Sort
      Picks a pivot point and compares each item to the pivot point. It moves each item according to the pivot point. When there are no more items to move in the first iteration, these steps are repeated for the "left" and "right" sides of the collection. Quick sort has good performance compared to other sorting algorithms.

  5. Study LEFT, RIGHT, and INNER join.



  6. Be able to write a linear search and binary search and know the associated runtimes.

    Binary Search

      - The best case scenario for binary search is if the collection
        being searched through has only one item, such that the algorithm has 0(1).
        If the collection only has one item,
        then in the binary search high, low, and mid are all equal at which point
        the method returns "not found"/nil or the item at the sole index.

      - The worst case scenario for binary search is if the input
        collection approaches an infinite size. In this case, the collection will have to be cut in half more times but that's not so bad because on first iteration you're still throwing away half of an infinite collection of items. Because of this, binary search in it's worst case has O(log n).

      What is the Big-O of binary search?

        - O(log n). Worst case of binary search is log n

      What is the Big-Ω of binary search?

        - Ω(1). Best case for binary search is constant

      What is the Big-Ө of binary search?

        - Ө(logn). Average case for binary search is log n.

  7. Be able to design a database and write CREATE TABLE statements.

    Example:

      CREATE TABLE boat (
        id integer PRIMARY KEY NOT NULL,
        type text NOT NULL,
        license_plate varchar(7) NOT NULL,
        owner_id integer REFERENCES owner(id)
      );

  8. Be able to utilize JOINS and subqueries in a query.



  9. Understand the purpose of normalization and denormalization

    Benefits of data normalization:

      Data integrity:
        - not only does normalization reduce data duplication, since there is no redundant, neglected data, normalization prevents update anomalies (mistakes) and data inconsistencies.

      Optimized queries:
        - normalized tables group data more logically, and produce rapid, efficient joins.

      Faster index creation and sorting (since the tables have fewer columns)

      Faster update performance (since there are fewer indexes per table)

      Improved concurrency resolution (since table locks will affect less data)

    Data Denormalization
      - If data normalization aims to reduce redundancy, data denormalization is a process performed on a previously-normalized database to increase read performance.

    Methods of denormalization

      Common techniques for denormalization in database design include:
      - Adding redundant groups
      - Adding derived columns
      - Combining tables
      - Repeating groups
      - Creating extract tables
      - Partitioning relations

end
