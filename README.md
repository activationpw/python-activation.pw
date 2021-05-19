# python-python-activation.pw


### Описание на русском ниже

Wrapper for automatic reception of SMS-messages by activation.pw

### Installation
You can install from source with:
```
$ git clone https://github.com/activationpw/python-activation.pw.git
$ cd python-python-activation.pw
$ python setup.py install
```
...or install from source but without pip:
```
$ pip install git+https://github.com/activationpw/python-activation.pw.git
```
### Example
```python
from activationpw import Sms, SmsService, GetNumber

wrapper = Sms('API KEY')

activation = GetNumber(
	service=SmsService().Youla,
).request(wrapper)

input('Press enter if your sms was sent')

activation.was_sent().request(wrapper)
code = activation.wait_code(wrapper=wrapper)
print(code)
```
More examples located in /example/ dir

----
Библиотека на python для работы с api сервиса автоматического приёма смс – activation.pw


### Установка
Установка напрямую из репозитория, с ручной сборкой
```
$ git clone https://github.com/tezmen/python-python-activation.pw
$ cd python-python-activation.pw
$ python setup.py install
```
...либо установка через pip но из репозитория, минуя сервера pypi
```
$ pip install git+https://github.com/tezmen/python-python-activation.pw
```
### Простой пример
```python
from activationpw import Sms, SmsService, GetNumber

wrapper = Sms('API KEY')

activation = GetNumber(
	service=SmsService().Youla,
).request(wrapper)

input('Press enter if you sms was sent')

activation.was_sent().request(wrapper)
code = activation.wait_code(wrapper=wrapper)
print(code)
```
Это пример использует встроенный обработчик. Вы можете вручную устанавливать статусы и управлять процессом, а так же много чего ещё.
Больше примеров находится в папке /example/
