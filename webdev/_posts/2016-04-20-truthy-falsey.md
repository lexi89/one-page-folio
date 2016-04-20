---
title: Truthy / Falsey For (Ruby) Noobs
---
Ok, this one's real easy but interesting so lets start at the beginning.

When you want to check one thing against another, you write a method that replies - `true` or `false`.

At the most basic level, it looks like this:

```ruby
def more_than_ten? number
  if number > 10
    return true
  else
    return false
  end
end

more_than_ten? 12 # => true
```

When you use boolean symbols, like `>, <, =>, =<, !, ||, &&,` you are telling ruby you want a `true` or `false` value.

No matter what you use these boolean "operators" on, ruby will try to convert it into `true` or `false`. If you ask ruby if an empty string `""` is true, it will tell you it is.

This seems strange because an empty string has nothing in it. And in fact, in other languages, the interpreter will tell you it's `false`.

But when in ruby, we have to accept that it's `true`.

When one converts a non-boolean piece of data like an array, string, hash, number etc... into a `true` or `false` value, we say it's "truthy" or "falsey".
It's `true` (but not *really* true).

There are interesting ways to use this.

```ruby
def truthy_or_falsey value
  if value
    puts "#{value.inspect} is truthy"
  else
    puts "#{value.inspect} is falsey"
  end
end

[true, false, Object, 0, 1, nil, true, false, "", [1, 2, 3], {}].each do |value|
  truthy_or_falsey(value)
end

# =>
# true is truthy
# false is falsey
# Object is truthy
# 0 is truthy
# 1 is truthy
# nil is falsey
# true is truthy
# false is falsey
# "" is truthy
# [1, 2, 3] is truthy
# {} is truthy
```
In Ruby, only `nil` and `false` are falsey, everything else is truthy: `[], {}, "", 0, 1, true, Object, [1,2,3]`.

This can lead to very cute bits of code like this:

```ruby
def logged_in?
  !!current_user
end
```
Here, `!current_user` forces the variable `current_user` into a boolean. A bang is the "not" operator, so it will return the opposite of it's actual value, so we add another bang `!` to change it *back* to it's actual `true` or `false` value. If we added another `!` it would change it *back* to `false` again.

Clever.
