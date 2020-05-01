# My 4 Favorite Ruby methods

### `.sort`

Sorts data given a comparison block. Non destructive! 

```ruby
["andrew", "pat", "garrett"].sort{ |x,y|  x.length <=> y.length } # ["pat", "andrew", "garrett"]
```

### `.inject`

Given an iterable object and a initial value, it will perform the action of a block on each element
and return the aggregate value. Non destructive! 

```ruby
[1,2,3,4].inject(0){ |sum, x| sum + x } # 10
```

### `.bsearch`

On an array, it applies a binary search given a condition in a block
```ruby
[1,2,3,4,5,7,8,9].bsearch{ |x| x > 7 } # 8
```

###  `.flatten`

On an array, it will take any nested arrays and make it into a 1-d array

```ruby
[[1,2, [3,[4,5,6],7]],8,9,10].flatten # [1,2,3,4,5,6,7,8,9,10]
```