# ReactJS and Redux Questions Answers

Looking forward to appear in React and Redux Interview, here are the key React and Redux Interview Questions with Answers only for you.

### Table of Contents
| Sr.No.        | Question      | 
| ------------- |-------------| 
| 1             |[How does React work? How does Virtual-DOM work in React?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#1-how-does-react-work-how-does-virtual-dom-work-in-react) | 
| 2             |[What is JSX?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#2-what-is-jsx) |
| 3             |[Difference between forward() method & SendRedirect() method?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#3-difference-between-forward-method--sendredirect-method) |
| 4             |[Difference between HashMap and HashTable?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#4-difference-between-hashmap-and-hashtable) |
| 5             |[Difference between HashSet and TreeSet?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#5-difference-between-hashset-and-treeset) |
| 6             |[What is meant by Collections in Java?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#6-what-is-meant-by-collections-in-java) | 
| 7             |[What is meant by Ordered and Sorted in collections?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#7-what-is-meant-by-ordered-and-sorted-in-collections) |
| 8             |[Explain about Set and their types in a collection?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#8-explain-about-set-and-their-types-in-a-collection) |
| 9             |[What is the final keyword in Java?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#9-what-is-the-final-keyword-in-java) |
| 10             |[What is a Thread?](https://github.com/aatul/Java-Interview-Questions-Answers/blob/master/README.md#10-what-is-a-thread) |
---

### 1. How does React work? How does Virtual-DOM work in React?

React creates a virtual DOM. When state changes in a component it firstly runs a “diffing” algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff. The HTML DOM is always tree-structured — which is allowed by the structure of HTML documents. The DOM trees are huge nowadays because of large apps. Since we are more and more pushed towards dynamic web apps (Single Page Applications — SPAs), we need to modify the DOM tree incessantly/constantly and a lot. And this is a real performance and development pain.

The Virtual DOM is an abstraction of the HTML DOM. It is lightweight and detached from the browser-specific implementation details. It is not invented by React but it uses it and provides it for free. ReactElements lives in the virtual DOM. They make the basic nodes here. Once we define the elements, ReactElements can be rendered into the "real" DOM. Whenever a ReactComponent is changing the state, diff algorithm in React runs and identifies what has changed. And then it updates the DOM with the results of diff. The point is - it’s done faster than it would be in the regular DOM.

The major features of React are:
*	It uses VirtualDOM instead of RealDOM considering that RealDOM manipulations are expensive.
*	Supports server-side rendering.
*	Follows Unidirectional data flow or data binding.
*	Uses reusable/composable UI components to develop the view.

---

### 2. What is JSX?

JSX is a syntax extension to JavaScript and comes with the full power of JavaScript.
*	 JSX produces React “elements”.
*	 You can embed any JavaScript expression in JSX by wrapping it in curly braces. 

After compilation, JSX expressions become regular JavaScript objects. This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions. Even Though React does not require JSX, it is the recommended way of describing our UI in React app.

For example, below is the syntax for a basic element in React with JSX and its equivalent without it.
```js
const element=(
  <h1 classname="greeting">
    Hello World!
  </h1>
```
Equivalent of the above using React.createElement
```js
const element= React.createElement(
  'h1',
  {"classname": "greeting"},
  'Hello World!'
);
```
---

### 3. Difference between forward() method & SendRedirect() method?

| forward() method        | sendRedirect() method      | 
| ------------- |-------------| 
|forward() sends the same request to another resource.|sendRedirect() method sends new request always because it uses the URL bar of the browser.|
|forward() method works at server side.|sendRedirect() method works at client side.|
|forward() method works within the server only.|sendRedirect() method works within and outside the server.|

---

### 4. Difference between HashMap and HashTable?

| HashMap        | HashTable      | 
| ------------- |-------------| 
|Methods are not synchronized|Key methods are synchronized|
|Not thread safe|Thread safe|
|Iterator is used to iterate the values|Enumerator is used to iterate the values|
|Allows one null key and multiple null values|Doesn’t allow anything that is null|
|Performance is high than HashTable|Performance is slow|

---

### 5. Difference between HashSet and TreeSet?

| HashSet        | TreeSet      | 
| ------------- |-------------| 
|Inserted elements are in random order|Maintains the elements in the sorted order|
|Can store null objects|Couldn’t store null objects|
|Performance is fast|Performance is slow|

---

### 6. What is meant by Collections in Java?

The Collection in Java is a framework that provides an architecture to store and manipulate the group of objects. Java Collections can achieve all the operations that you perform on data such as searching, sorting, insertion, manipulation, and deletion.Java Collection means a single unit of objects. The Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet). 

Collections are used to perform the following operations:
*	Searching
*	Sorting
*	Manipulation
*	Insertion
*	Deletion 
---

### 7. What is meant by Ordered and Sorted in collections?

**Ordered:**

It means the values that are stored in a collection is based on the values that are added to the collection. So we can iterate the values from the collection in a specific order.

**Sorted:**

Sorting mechanism can be applied internally or externally so that the group of objects sorted in a particular collection is based on properties of the objects.

---

### 8. Explain about Set and their types in a collection?

**Set**

Set cares about uniqueness. It doesn’t allow duplicates. Here the “equals ( )” method is used to determine whether two objects are identical or not.

**Hash Set:**
*	Unordered and unsorted.
*	Uses the hash code of the object to insert the values.
*	Use this when the requirement is “no duplicates and don’t care about the order”.

Example:
```java
public class Fruit {
  public static void main (String[] args){
    HashSet<String> names = new HashSet <=String>();
    names.add(“banana”);
    names.add(“cherry”);
    names.add(“apple”);
    names.add(“kiwi”);
    names.add(“banana”);
    System.out.println(names);
  }
}
```
Output:

[banana, cherry, kiwi, apple]

Doesn’t follow any insertion order. Duplicates are not allowed.

**Linked Hash set:**
*	An ordered version of the hash set is known as Linked Hash Set.
*	Maintains a doubly-Linked list of all the elements.
*	Use this when the iteration order is required.

Example:
```java
public class Fruit {
  public static void main (String[] args){
    LinkedHashSet<String> names = new LinkedHashSet <String>();
    names.add(“banana”);
    names.add(“cherry”);
    names.add(“apple”);
    names.add(“kiwi”);
    names.add(“banana”);
    System.out.println(names);
  }
}
```
Output:

[banana, cherry, apple, kiwi]

Maintains the insertion order in which they have been added to the Set. Duplicates are not allowed.

**Tree Set:**
*	It is one of the two sorted collections.
*	Uses “Read-Black” tree structure and guarantees that the elements will be in an ascending order.
*	We can construct a tree set with the constructor by using comparable (or) comparator.

Example:
```java
public class Fruits{
  public static void main (String[] args) {
    Treeset<String> names= new TreeSet<String>();
    names.add(“cherry”);
    names.add(“banana”);
    names.add(“apple”);
    names.add(“kiwi”);
    names.add(“cherry”);
    System.out.println(names);
  }
}
```
Output:

[apple, banana, cherry, kiwi]

TreeSet sorts the elements in an ascending order. And duplicates are not allowed.


---

### 9. What is the final keyword in Java?

**Final variable:**

Once a variable is declared as final, then the value of the variable could not be changed. It is like a constant.

Example:
```java
final int = 12;
```
**Final method:**

A final keyword in a method that couldn’t be overridden. If a method is marked as a final, then it can’t be overridden by the subclass.

**Final class:**

If a class is declared as final, then the class couldn’t be subclassed. No class can extend the final class.


---

### 10. What is a Thread?

In Java, the flow of an execution is called Thread. Every java program has at least one thread called main thread, the Main thread is created by JVM. The user can define their own threads by extending Thread class (or) by implementing Runnable interface. Threads are executed concurrently.

Example:
```java
public static void main(String[] args){//main thread starts here

}
```
---

Wish you all the best.
