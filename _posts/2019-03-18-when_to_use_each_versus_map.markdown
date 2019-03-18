---
layout: post
title:      "When To Use .Each Versus .Map"
date:       2019-03-18 14:09:31 +0000
permalink:  when_to_use_each_versus_map
---

I am going to tackle the absolutely age old and pressing question of when to the use .each method versus using .map. When I first started learning Ruby, wayyy back in June of this year (though, it has felt like a lifetime ago), I was using .each on everything. Oh, you want to iterate over an array? A hash? Perfect, .each is the catch-all.

```
https://gph.is/1TIQThh
```

I am about to use a lot of GIFs. I am sorry in advance. It came as no surprise that I knew not what I did. While .each is a valuable method, it should be used in specific situations. It is not necessarily a catch-all but should be used when you want to iterate over each element in a collection and perform a particular action on it without returning a new array.

> .Each calls a block once for every element in self, the array we call it on, and passes that element as a parameter. It will return the same array it was called on.


In the example below, we have an array of integers [1, 2, 3, 4] which we call .each on, we then open up our block with some curly braces with |n| which represents the integer we are iterating over, and finally we take that n representing each individual integer in the collection and multiply it by 2.

> ** [1, 2, 3, 4].each { |n| puts n * 2 }
>  => Outputs: 2
>  4
>  6
>  8**

This method can be used on any collection of objects. A collection of integers, strings, puppies, you name it. It's excellent for looping through an array and printing out all of its values. For example, maybe we have array, we can always run a .each on it and have it print out to the screen. Or similarly, we could find the highest number in an array with each, the lowest, etc. I repeat, .Each is not helpful if we want to return a new array because its default is to return the original collection that it was called on. This poses a problem because sometimes we do want to create a new array. Maybe we want to iterate over a collection of checking accounts and give everyone a $50.00 gift. We want a new array to be created so they can hold on to their money. We don't want to say we'll give it to them and then that gift to not be reflected by their balance at the end of the day. If only there were a method that would return a new array once we iterate over it… oh wait! There is!

```
https://gph.is/15bRbWf
```

The .map method will appeal to the block once for each element in self, the array we call it on, and then it will create a whole new array comprised of the values returned by the block. It can also be used on a collection of any objects.
Another method that gets used quite often is .collect. It can be used interchangeably with .map. As it turns out, .map is an alias for .collect but .map is used more frequently. Only reiterating the fact that programmers are indeed the laziest of all humans. Let's take a look at an example. Here, we have an array of [1, 2, 3, 4] and we call the .map method on it. We then open a set of curly braces where we iterate over each integer in the array, represented by |n|, then take the integer and multiply it by 2. The iteration is reflected in a new array that is returned at the end of the block that is every number in the original array multiplied by 2 => [2, 4, 6, 8].

> **[1, 2, 3, 4].map { |n| n * 2}
> => [2, 4, 6, 8]**

Excellent! In the span of just a few minutes, we learned about three methods we can call on to iterate through a collection of objects with different end results. We learned about .each, .map, and .collect (which can be used interchangeably with .map). Now we can diversify our code and be more specific with what we are asking of the data we are working with.

```
https://gph.is/28SYgGf
```
