Tags: #
____
# Реализация
![[Pasted image 20240424201924.png]]
```python
def momentum_method(x_start, learning_rate, epsilon, num_iterations, momentum, delta=0.01):  

x_curr = x_start
df_x = sp.diff(f(x)) 

trace = []
trace.append(x_curr) 

h_curr = 0
h_trace = []
h_trace.append(h_curr)
  

for i in range(1, num_iterations):  

	h_new = momentum * h_curr + learning_rate * df_x.subs(x, x_curr)
	x_new = x_curr - h_new
	trace.append(x_new)

	h_trace.append(h_new)

	if (abs(x_new - x_curr) < epsilon) or (abs(df_x.subs(x, x_new)) < delta):

		return x_new, trace, i  

	x_curr = x_new	
	h_curr = h_new 

return x_new, trace, i

```


____
### Zero-Links

____
### Links