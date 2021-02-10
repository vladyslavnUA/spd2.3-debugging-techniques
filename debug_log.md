# Debug Log

**Explain how you used the the techniques covered (Trace Forward, Trace Backward, Divide & Conquer) to uncover the bugs in each exercise. Be specific!**

In your explanations, you may want to answer:

- What is the expected vs. actual output?
- If there is a stack trace, what useful information does it contain?
- Which technique did you use, on which line numbers?
- What assumptions did you have about each line of code, and which ones were proven to be wrong?

_Example: I noticed that the program should show pizza orders once a new order is made, and that it wasn't showing any. So, I used the trace forward technique starting on line 13. I discovered the bug on line 27 was caused by a typo of 'pzza' instead of 'pizza'._

_Then I noticed another bug ..._

## Exercise 1
```
[[The expected output of this exercise is the pizza order placed but the actual output throws an error. The stack trace throws the error "TypeError: 'topping' is an invalid keyword argument for PizzaTopping" which means the variable is probably misspelled or not access correctly. Line 79 throws the error because topping is not a model variable. Changing topping to topping_type fixed this error.

My next error came on line 84 which said "werkzeug.routing.BuildError: Could not build url for endpoint '/'. Did you mean 'fulfill_order' instead?" To fix it, I changed the redirect from `redirect(url_for('/'))` to `redirect('/')` 

The other bug I found was pizza information wasn't being saved when passed into the form as the print statement on line 76 was returning None instead of the pizza size. The assumption I had about this code is that the form information was not being pulled correctly and it proved right.]]
```
## Exercise 2

```
[[The expected output is the temperate at the city submitted but the actual output is an API error. At first try, an Internal Server Error is thrown with a backend message of "'city': result_json['name'], KeyError: 'name'". This is thrown because something is wrong with the API call.

In addition, the parameters were being incorrectly retrieved from the form, where the form name "users_city" should be "city" and "requested_units" should be "units"]]
```

## Exercise 3

```
[[The expected output is the list sorted but the actual output is a list indexing error. The first error I get when running the file is "arr[k] = right_side[i] IndexError: list index out of range". This tells me that a list is being sorted through incorrectly.

To fix this, I changed arr[k] = right_side[i] to arr[k] = right_side[j]. Another error saying "TypeError: list indices must be integers or slices, not float" came afterwards. I fixed this by wrapping the mid variable as an integer.]]
```