# indexed priority queue implemented with a python list

Three classes
indexed min heap, indexed max heap and indexed median heap
min_ipqa, max_ipqa, median_ipqa


an element of arbitrary index can be removed with pop_using_input_index in O(log(N))

``` python
my_min_ippa = min_ipqa()
my_min_ippa.insert(0, 1)
my_min_ippa.insert(1, 3)
my_min_ippa.insert(2, -3)
my_min_ippa.insert(3, -5)
my_min_ippa.insert(4, 5)
print('arbitrary at index 2 popped with value', my_min_ippa.pop_using_input_index(2))

while my_min_ippa.len > 0:
    print(my_min_ippa.poptop())

```
results will be
```
arbitrary at index 2 popped with value (2, -3)
(3, -5)
(0, 1)
(1, 3)
(4, 5)

```

Note that the tuple is (index, value)
and the heap is popping by ordering the value instead of the index

## Median heap

```python
my_median_ipqa = median_ipqa()
e = [1, 2, 3, 4, 2, 3, 6, 8, 4, 5]
d = 3
for i, val in enumerate(e):
    my_median_ipqa.insert(i, val)
    print(my_median_ipqa)
    print(my_median_ipqa.get_median())
```