On Immutability

One of the problems we ask during our hiring process involves building an immutable tree.
While we are not particular about using a certain style of programming over any other and
have seen some really clever and ingenious solutions, we have also noticed that use
immutability in the problem statement often leaves people confused. We decided to come up
with this blog post to help get over the initial inertia in understand immutability and
some of its consequences.

# Let’s talk about version control

We have come up with a brilliant idea that will solve all the problems in software
(https://www.youtube.com/watch?v=TBwW2vTKVy4) and in the process end up making us
billions. But first we need to write some code for that. Like all great projects, even
this must start with creating a directory,
```bash
mkdir billions
cd billions
build-tool start make-me-billions-template
```
We start our favourite development environment and in a few hours we have a whole bunch of
feature and we are upwards of a few thousand lines of code closer to our billions.

Now that the project is picking steam, we need more people to help make our billions
faster. Hiring a bunch of people is a great idea, getting as many resources to work
together as quickly as possible. But, we soon realise we need a better way to manage our
code. Every time someone makes a change to code they need to check with everyone else
whether is safe to make their  changes, and even then, there are often overwrites. And
situations where there is an interdependence on features, they seem to never get
completed. We clearly need a better way to manage our code.

Let us make a copy of our code each time we make a significant change to it, so now we
never have a situation where many people are working on the same code base, because every
one has their own copy to work with. But clearly this is not sustainable, we need
something still better. And this is where version control comes to our rescue.

# Isn’t that the silliest introduction to version control

If we think about it, in the previous exercise, we decoupled the state of our code from
the time in our development cycle. We began with case where we had to deal with all the
mess of the code being changed by many people simultaneously and often end up with half
garbled code, we had overwriting of code, we have to check with others before making changes
to our code, interdependence would block the whole development at times. We could not
accurately say what the code was a given time.

Once we started making copies of the code for every change to it, we could exactly
determine what our code base looked like at any time in the development cycle, and
multiple people could work on code at the same time, and the interdependence between
features becomes much easier to handle. And this is exactly what our favourite version
control systems help us manage. They are efficient systems to help us maintain immutable
snapshots of our code-base.

# And now, Immutability

Our version control system helped us decouple the state of our code base to the time in
the development cycle by providing us immutable snapshots of our code at every change of
our code base. Immutability give us the same advantages with our data structures.

Immutable data structures once created cannot be changed. When we want make any changes,
we need to create a new value of the structure that along with the changes. Of course,
creating every time we make a change to a large data structure would be slow and memory
consuming, and there are smarter ways to share data between different values of a data
structure, but that discussion would be out of the scope of this article (see Other
Reading).

# An immutable list

Now that we have seen what immutable data structures are and some of the advantages they
provide, lets implement our own version of an immutable list in javascript.
```javascript
var ImmutableList = function (list) {
   if(list.constructor === Array) {
      var list = list;
   } else {
      throw new Error("Invalid Argument, should be a list");
   }
   var list = list;
   return {
      getList: function () {
         return list;
      }
   }
};
```
Our `ImmutableList` is now just a simple wrapper whose constructor takes a list as an
argument and has a simple function to get the list. Lets create functions that append
and remove elements to our `ImmutableList`.

```javascript
var ImmutableList = function (list) {
   if(list.constructor === Array) {
      var list = list;
   } else {
      throw new Error("Invalid Argument, should be a list");
   }
   return {
      getList: function () {
         return list;
      },

   }
};

var append =  function(list, elem) {
   return new ImmutableList(list.concat(elem));
},

var remove =  function(list, elem) {
   return new ImmutableList(list.filter(function (x) { return x != elem});
},
```
Notice how when we add elements to our `ImmutableList`, we create a new `ImmutableList`
object and don’t modify the existing value. It is also important to not that
`list.concat()` does not mutate the original list.

# Other Reading

Now that we have scratch the surface of immutability, there are many other good resources
that explain these topics in greater depth.
   1. https://www.youtube.com/watch?v=I7IdS-PbEgI
   2. https://en.wikipedia.org/wiki/Persistent_data_structure
   3. http://www.cs.cmu.edu/~sleator/papers/another-persistence.pdf

# Getting immutability

Hopefully, this article has at least got you interested in playing with immutable data
structures, here are some of the ways you can get some:
   1. Be disciplined. Immutability is all about not modifying a value once it is created.
      Figure out how you can best mimic immutability in your favourite language.
   2. Use a language that has built in support for immutable data structure. There are a
      lot of programming language like clojure, haskell, scala, etc., have a built in
      support for immutable data structures. Some languages like Haskell force you to only
      use immutable data structures.
   3. Use a library that provides immutable data structures. There are libraries in many
      languages that provide good support for immutability like
      https://facebook.github.io/immutable-js/ for javascript,
      https://github.com/tobgu/pyrsistent for python and
      https://github.com/hamstergem/hamster for ruby.
   4. Implement your own immutable data structures. 
