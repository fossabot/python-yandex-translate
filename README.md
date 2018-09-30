python-yandex-translate [![Build Status](https://travis-ci.org/dveselov/python-yandex-translate.svg?branch=master)](https://travis-ci.org/dveselov/python-yandex-translate)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdveselov%2Fpython-yandex-translate.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdveselov%2Fpython-yandex-translate?ref=badge_shield)
=======================

Python module for Yandex.Translate API.

This module is fully-compatible with Python 2.7+ and 3.3+ versions.


Installation
======================
Use `pip`:

```bash
pip install yandex.translate
```

Usage
=======================


```python
from yandex_translate import YandexTranslate
translate = YandexTranslate('Your API key here.')
print('Languages:', translate.langs)
print('Translate directions:', translate.directions)
print('Detect language:', translate.detect('Привет, мир!'))
print('Translate:', translate.translate('Привет, мир!', 'ru-en'))  # or just 'en'
```

This will output:

```
Languages: {'en', 'el', 'ca', 'it', ..}
Translate directions: ['az-ru', 'be-bg', 'be-cs', ..]
Detect language: 'ru'
Translate: {'text': ['Hello, world!'], 'code': 200, 'lang': 'ru-en'}
```
Also, it's possible to use proxies when doing requests to Yandex.Translate API - just pass `proxies` dictionary [with data in same format](http://docs.python-requests.org/en/master/user/advanced/#proxies) that `requests` use.

License
=======================
WTFPL (Public Domain)


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdveselov%2Fpython-yandex-translate.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdveselov%2Fpython-yandex-translate?ref=badge_large)