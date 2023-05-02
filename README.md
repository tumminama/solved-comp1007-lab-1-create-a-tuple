Download Link: https://assignmentchef.com/product/solved-comp1007-lab-1-create-a-tuple
<br>
Review: A tuple is an <strong><u>immutable</u></strong> sequence type that contains an ordered collection of items. After you create a tuple, you usually cannot change it anymore. Previously, we learned that a tuple can be created by including the sequence of data items inside ( ). In fact, a tuple can be created even without the ( ).

<strong>Example 3.1</strong>: Try the following statements to create a few tuples and check them:

<h1>  tuple1 = 1, 3, 5, 7</h1>

<strong>print</strong>(tuple1)

tuple2 = (1, 3, 5, 7)

<strong>print</strong>(tuple2)

<h2>  #Are tuple1 and tuple2 the same? “==” is a comparison operator     print(tuple1 == tuple2)</h2>




tuple3 = (“Jack”, “John”, “Alice”)

<strong>print</strong>(tuple3)

tuple4 = (1, “Jack”, 2, “John”)

<strong>print</strong>(tuple4)

<strong><u>Negative indexing</u></strong>: Recall that tuple[0] refers to the first item, tuple[8] refers to the 9‐th item, etc. More interestingly, Python also supports <strong>negative indexing</strong>: e.g., tuple[‐1] refers to the last item, tuple[‐2] refers to the 2<sup>nd</sup> last item, etc. This is convenient if you want to access the data in the reverse order.




Fig. 1 An illustration of negative indexing

<strong>Example 3.2</strong>: Try the following statements to access the items in a tuple through indexing

<strong>print</strong>(tuple4[0])

<strong>print</strong>(tuple4[1])

<strong>print</strong>(tuple4[2])

<strong>print</strong>(tuple4[3])

<strong>print</strong>(tuple4[‐1])

<strong>print</strong>(tuple4[‐2])

<strong>print</strong>(tuple4[‐3])

<strong>print</strong>(tuple4[‐4])

<h1>More   about Lists</h1>

Review: A list is a <strong><u>mutable</u></strong> sequence type that can hold any number of ordered data items with any data type. Due to this flexibility, it is one of the most commonly used data structures in Python.

A list can be generated by providing a list of data items enclosed by <strong>square brackets []</strong>, separated by commas. A list can also be generated from an existing non‐list sequence (such as a range or a tuple) by built‐in function <strong>list()</strong>.

After you create a list, you can further revise it by adding new items, removing existing items, or changing the order of items.

<strong>Example 3.3</strong>: Try the following statements to create a few lists in different ways:

<table width="0">

 <tbody>

  <tr>

   <td width="550">list1 = [1, 3, 5, 7] <strong>print</strong>(list1)list2 = [“Jack”, “John”, “Alice”] <strong>print</strong>(list2)list3 = [1, “Jack”, 2, “John”] <strong>print</strong>(list3) <strong>#Generate a list from a range </strong>my_range = range(10, 20, 2) <strong>print</strong>(my_range) list4 = list(my_range) <strong>print</strong>(list4)<strong> </strong><strong>#Generate a list from a tuple tuple1 = (</strong>“John”, “Alice”, “Jack”<strong>)</strong> list5 = list(tuple1) <strong>print</strong>(list5) <strong>#Is list5 equal to tuple1? print(</strong><strong>list5 == tuple1</strong><strong>)</strong></td>

  </tr>

 </tbody>

</table>




Remark: In Example 3.3, although <strong>list5</strong> has the same data items as <strong>tuple1</strong>, they are different because they have different types (list vs. tuple) and they support different operations.

<strong><u>List Operations</u></strong>: List structure supports many useful operations (i.e., data processing!). Below is a list of common list operations:

<table width="0">

 <tbody>

  <tr>

   <td width="187">Operation</td>

   <td width="377">Explanation</td>

  </tr>

  <tr>

   <td width="187">Indexing through []</td>

   <td width="377">To access an item in the list</td>

  </tr>

  <tr>

   <td width="187"><strong><em>len(</em></strong><em>mylist<strong>)</strong></em></td>

   <td width="377">Return the number of items in list <strong><em>mylist</em></strong></td>

  </tr>

  <tr>

   <td width="187"><em>mylist.<strong>append(</strong>object<strong>)</strong> </em></td>

   <td width="377">Add an <strong><em>object</em></strong> at the end of the list <strong><em>mylist</em></strong></td>

  </tr>

  <tr>

   <td width="187"><em>mylist.<strong>insert(</strong>index, object<strong>)</strong> </em></td>

   <td width="377">Add an <strong><em>object</em></strong> at the <strong><em>index</em></strong> location of the list <strong><em>mylist</em></strong>. The index begins with 0.</td>

  </tr>

  <tr>

   <td width="187"><em>mylist.<strong>remove(</strong>object<strong>)</strong> </em></td>

   <td width="377">Remove the <strong><em>object</em></strong> from the list <strong><em>mylist</em></strong>. If multiple items in</td>

  </tr>

  <tr>

   <td width="187"> </td>

   <td width="377">the list have the same value, the first one will be removed.</td>

  </tr>

  <tr>

   <td width="187"><em>mylist.<strong>sort()</strong> </em></td>

   <td width="377">Sort the <strong><em>items</em></strong> in the list <strong><em>mylist</em></strong>.</td>

  </tr>

  <tr>

   <td width="187"><em>mylist.<strong>reverse()</strong> </em></td>

   <td width="377">Rearrange the items of list <strong><em>mylist</em></strong> in reverse order.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Example 3.4</strong>: Try the following statements to get familiar with list operations:

<table width="0">

 <tbody>

  <tr>

   <td width="550">list6 = [“Jack”, “John”, “Alice”] <strong>print</strong>(list6) <strong>print</strong>(list6[0]) <strong>print</strong>(list6[‐1]) <strong>print</strong>(len(list6)) list6.append(“Jack”) <strong>print</strong>(list6)list6.insert(2, “Jack”) <strong>print</strong>(list6) list6.remove(“Jack”) <strong>print</strong>(list6) list6.sort() <strong>print</strong>(list6) list6.reverse() <strong>print</strong>(list6)</td>

  </tr>

 </tbody>

</table>




There is another important operation in Python: <strong>slicing</strong>, that deserves a separate treatment.

<strong><u>Slicing</u></strong> means the access of a subset of items in a sequence of data items, which is very important in data analysis.

<ul>

 <li>You can access a range of items in a list <strong>mylist</strong> through mylist[start:stop], where <strong>start</strong> Is the index of the first item in your slice, and <strong>stop−1</strong> is the index of the last item in your slice.</li>

 <li>If your slice begins with the first element in the list, you can set <strong>start</strong> empty (i.e., mylist[:stop]).</li>

 <li>If your slice includes the items up to the end of the list, you can set <strong>stop</strong> empty (i.e., mylist[start:]).</li>

 <li>Slicing with increments through mylist[start:stop:step], where <strong>step</strong> specifies the increment between the indices.</li>

</ul>




Fig. 2 An illustration of indexing and slicing




Let’s learn from the following example:

<strong>Example 3.5</strong>: Try the following statements to get familiar with <strong>list slicing</strong>:

a = list(range(10))  <strong>print</strong>(a) b = a[2:6] <strong>print</strong>(b) c = a[:5] <strong>print</strong>(c) d = a[5:] <strong>print</strong>(d) e = a[3:10:2] <strong>print</strong>(e)




<h1>Dictionaries</h1>

<strong><u>Key‐Value Pairs</u></strong>: Information is very often more than individual numbers or strings: they have relationships. For example, a person named “Jack” has an age of 35; his wife “Linda” has an age of 32; his daughter “Alice” has an age of 6; his father “David” has an age of 68. In Python, we can create a pair of data items that are related, e.g., “Jack”:35, “Linda”:32, “Alice”:6, and “David”:68. They are called <strong><u>key‐value pairs</u></strong>: the key “Jack” has a value 35; the key “Linda” has a value 32; the key “Alice” has a value 6, and the key “David” has a value 68. Notice that the key and its value are separated by a colon.

<strong>Property of key‐value pair</strong>s: In general, a key is a fixed and representative property of an object, and hence it should be immutable. Furthermore, the <strong><em>key</em></strong> should be unique in a collection of key‐value pairs. E.g., the student ID is unique in the set HKBU students, so student ID can serve as the key for the set of student records. On the other hand, the value associated with a key is mutable and can be anything. The <strong><em>value</em></strong> can even be a list that includes a lot of data items, such as names, courses, marks, etc. E.g., a key value pair can be “17212346” : [“CHAN DAI MAN”, “2000‐01‐01”, “Male”].

<strong><u>Python Dictionary</u></strong>: If we have thousands to millions of key‐value pairs like {“Jack”:35}, could we quickly find out the age of a person (i.e., the value) if you know the name (i.e., the key)? The question is similar to looking up a dictionary to find out the explanation of an English word: the word is the key, and the explanation is the value. In Python, a data structured called <strong><em>dictionary</em></strong> is provided to organize and process key‐value pairs.

A dictionary can be generated by providing a sequence of key‐value pairs, enclosed by curly braces <strong>{ }</strong> and separated by comma.

<strong><u>Position indexing vs Key indexing</u></strong>: Different from tuples or lists, the items in a dictionary cannot be accessed through position indexing because the items are organized according to the keys, rather than the order provided by the users. To access the value of a key, the user can use the key as the index: <strong>my_dict[key]</strong>.

To add a new key‐value pair into a dictionary, just use: <strong>my_dict[new_key] = new_value</strong>. If the <strong>new_key</strong> already exists in the dictionary, the old value will be replaced by <strong>new_value</strong> because a dictionary doesn’t allow two key‐value pairs with the same key.

To remove a key‐value pair from a dictionary, use method <strong>my_dict.pop(key)</strong>. <strong>Example 3.6</strong>: Try the following statements to get familiar with <strong>dictionary</strong>:

<table width="0">

 <tbody>

  <tr>

   <td width="550">family = {“Jack”:35, “Linda”:32, “Alice”:6} print(family) print(len(family)) family[“David”] = 68 print(family) print(len(family)) family[“Alice”] = 7 print(family) family.pop(“David”) print(family)stu = {“17212345”:[“CHAN DAI MAN”, “2000‐01‐01”, “Male”],        “17216789”:[“WONG Maggie”, “2000‐06‐21”, “Female”]} print(stu[“17212345”])#stu[“17212345”] is a list. So what is stu[“17212345”][0]? print(stu[“17212345”][0]) print(stu[“17216789”])#stu[“17216789”] is a list. So what is stu[“17216789”][2]? print(stu[“17216789”][2]) #add the Address information into the dictionary stu[“17212345”].append(“KOWLOON TONG”) print(stu[“17212345”])stu[“17216789”].append(“SAI KONG”) print(stu[“17216789”])</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong><u>Summary:</u> </strong>

In this Lab1B, we have reviewed and learnt the following data structures that can store a sequence of data items:

    tuple, list, dictionary

Tuples are immutable, while lists and dictionaries are mutable.

We also learned how to access, add, and delete data items of lists and dictionaries.