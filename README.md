Differences between Hashtable and Dictionary
--------------------------------------------

Dictionary:
-----------
•It throws an exception of 'KeyNotFoundException'  if we try to find a key which does not exist.
•It is faster than a Hashtable because there is no boxing and unboxing.
•Only public static members are thread safe.
•Dictionary is a generic type which means we can use it with any data type.
•Dictionary maintains the order of entries by which entries 
•Dictionary relies on chaining whereas Hashtable relies on rehashing
•Dictionary was introduced in C#2.0.
•Dictionary uses KeyValuePair<K,T> generic objects to represent its key-value pairs.
•

Hashtable:
----------
•It returns null if we try to find a key which does not exist.
•It is slower than dictionary because it requires boxing and unboxing.
•All the members in a Hashtable are thread safe,
•Hashtable is not a generic type,
•When using large collection of key value pairs hashtable would be considered more efficient than dictionary.
•When we retrieve the record in collection the hashtable does not maintain the order of entries while dictionary 
 maintains the order of entries by which entries 
•Hashtable relies on rehashing
•Hashtable was introduced in C# 1.0.
•Hashtable is an untyped associative container that uses DictionaryEntry class to return results of enumeration 
 through its key-value pairs.
•


KeyValuePair:
-------------
KeyValuePair is a struct that contains a single key and a single value. KeyValuePair is useful when you want to store two related
pieces of information as a single unit. KeyValuePair < T,T > is for iterating through Dictionary < T,T >.

DictionaryEntry:
----------------
DictionaryEntry is a struct that contains a single key and a single value. DictionaryEntry is for iterating through HashTables.
We use DictionaryEntry in a foreach-loop.

Thread Safety between Dictionary and Hastable:
----------------------------------------------
Hashtable is thread safe for use by multiple reader threads and a single writing thread. It is thread safe for multi-thread 
use when only one of the threads perform write (update) operations, which allows for lock-free reads provided that the 
writers are serialized to the Hashtable.

A Dictionary can support multiple readers concurrently, as long as the collection is not modified. Even so, enumerating through 
a collection is intrinsically not a thread-safe procedure. In the rare case where an enumeration contends with write accesses, 
the collection must be locked during the entire enumeration. To allow the collection to be accessed by multiple threads for 
reading and writing, you must implement your own synchronization.

