##Python中写在元组里面的语句

'''javascript
loops = (randrange(2, 5) for x in xrange(randrange(3, 7)))
'''
不象通常我们写在list中的形如：
'''
[x for x in another]
'''
元组中没有**x**来指明元组的元素，第一次看到的时候我也不太懂是什么意思，
后来查stackoverflow，其中的回答如下：
'''
[e for e in ([n for n in xrange(random.randrange(1, 5))] for x in xrange(10))]
'''
输出结果：
'''
[[0, 1, 2, 3], [0, 1, 2], [0], [0], [0, 1], [0], [0, 1], [0, 1, 2, 3], [0, 1, 2], [0, 1, 2]]
'''
足见元组前半部分的语句是代表元组的取值范围，后面**for循环**的循环次数就表明元组的元素个数，而且看似语句的返回结果是一个元组（tuple），实际返回的是一个生成器，只能用迭代的方式去访问其中的元素。
