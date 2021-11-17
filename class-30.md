# **Hash Tables**

What is a Hashtable?

Terminology:

1.  Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2.  Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3.  Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
.

## **Structure**


### **Hashing**

Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. 

Hash codes should never have randomness to them. The same key should always produce the same hash code.

### **Collisions**

A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. 

The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

What would happen if two different keys resolved to be the same index of the array? This is called a collision. The hash map needs to be able to handle two keys resolving to the same index.

### **Bucket Sizes**

Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.

## **Creating a Hash**


A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

1.  Add or multiply all the ASCII values together.
2.  Multiply it by a prime number such as 599.
3.  Use modulo to get the remainder of the result, when divided by the total size of the array.
4.  Insert into the array at that index.


***

**To know more please [visit this page](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)**

***