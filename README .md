# Домашнее задание к 10 семинару.

Задача 44: В ячейке ниже представлен код генерирующий DataFrame, которая состоит всего из 1 столбца.
Ваша задача перевести его в one hot вид. Сможете ли вы это сделать без get_dummies?

import random
lst = ['robot'] * 10
lst += ['human'] * 10
random.shuffle(lst)
data = pd.DataFrame({'whoAmI':lst})
data

# Решение

```
data['robot'] = data['whoAmI'].map(lambda x: 1 if x == 'robot' else 0 )
data['human'] = data['whoAmI'].map(lambda x: 1 if x == 'human' else 0 )
data
```
