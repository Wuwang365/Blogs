# python \_\_call\_\_用法

python中的\_\_call\_\_用于使对象具有可执行性，举例如下

```python
class Example:
	def __call__(self):
        print("this is a class call")
        
    def func(self):
        print("this is a func call")

example = Example() # create an instance
example() # execute call function
example.func() # execute func
```

在深度学习框架中存在着大量类似的应用，如pytorch的Module对\_\_call\_\_进行了实现，从而实现了继承于Module的类具备可执行性，即默认调用forward方法并返回

```python
class Module:
    def __call__(self, *input, **kwargs):
        ###
        result = self.forward(*input, **kwargs)
        return result
        
```

