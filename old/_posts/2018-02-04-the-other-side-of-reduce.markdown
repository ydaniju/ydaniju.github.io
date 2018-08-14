---
layout: post
title:  "The Other Side of Reduce"
description: "Reduce is used for operating on arrays but there's more to it"
date:   2018-02-04 11:33:23 +0100
categories: jekyll update
permalink: the_other_side_of_reduce
source: meta_play
---

You might have been using reduce for a while now. THe usual way is to see 
examples like:

```ruby
# sum

[1, 2, 3].reduce(:+)  # 6

# Another sum

[1, 2, 3].reduce(0) { |accumulator, element| accumulator + element }  # 6

# Multiplication

[1, 2, 3].reduce(:*)  # 6

# Another Multiplication

[1, 2, 3].reduce(1) { |accumulator, element| accumulator * element }  # 6
```

For beginners in Ruby, this might create an impression that reduce usually reduces 
an array to a single items (like in sum or multiplication).

However, when you see yourself doing somthing like this, perhaps you should try 
using reduce.

```ruby

# using each or map
def greater_than_three(arr)
  big_numbers = []

  arr.each do |a|
    big_numbers << a if a > 3
  end

  big_numbers
end


# using reduce

def greater_than_three(arr)
  arr.reduce([]) do |big_numbers, num|
    big_numbers << num if num > 3
  
    big_numbers
  end
end

```

Yes, I know, We can simply achieve this using select

```ruby
  def greater_than_three(arr)
    arr.select { |num| num > 3 }
  end

```

Bless Ruby, we always have this methods to the rescue. Anyways, it's not bad that 
we know that rather than have a variable to hold 
