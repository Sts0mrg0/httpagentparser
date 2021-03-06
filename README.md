[![Downloads](http://pepy.tech/badge/httpagentparser)](http://pepy.tech/project/httpagentparser)

[![PYPI](https://img.shields.io/pypi/v/httpagentparser.svg)](https://pypi.python.org/pypi/httpagentparser)

[![Travis](https://img.shields.io/travis/shon/httpagentparser.svg)](https://travis-ci.org/shon/httpagentparser)


Features
========

-   Fast
-   Detects OS and Browser. Does not aim to be a full featured agent parser
-   Will not turn into django-httpagentparser ;)

Usage
=====

~~~~ {.sourceCode .python}
>>> import httpagentparser
>>> s = "Mozilla/5.0 (X11; U; Linux i686; en-US) AppleWebKit/532.9 (KHTML, like Gecko) \
        Chrome/5.0.307.11 Safari/532.9"
>>> print(httpagentparser.simple_detect(s))
('Linux', 'Chrome 5.0.307.11')
>>> print(httpagentparser.detect(s))
{'os': {'name': 'Linux'},
 'browser': {'version': '5.0.307.11', 'name': 'Chrome'}}

>>> s = "Mozilla/5.0 (Linux; U; Android 2.3.5; en-in; HTC_DesireS_S510e Build/GRJ90) \
        AppleWebKit/533.1 (KHTML, like Gecko) Version/4.0 Mobile Safari/533.1"
>>> print(httpagentparser.simple_detect(s))
('Android Linux 2.3.5', 'Safari 4.0')
>>> print(httpagentparser.detect(s))
{'dist': {'version': '2.3.5', 'name': 'Android'},
'os': {'name': 'Linux'},
'browser': {'version': '4.0', 'name': 'Safari'}}
~~~~

History
=======

<http://stackoverflow.com/questions/927552/parsing-http-user-agent-string/1151956#1151956>
