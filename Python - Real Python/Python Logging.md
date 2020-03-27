# Python Logging

https://realpython.com/python-logging/

---

5 default logging levels in order

> - DEBUG
> - INFO
> - WARNING
> - ERROR
> - CRITICAL

---

4 common parameters for logging's `basicConfig()`

> - `level`
> - `filename`
> - `filemode` (default `'a'` for append)
> - `format`

---

set logging level to debug

> ```python
> import logging
> logging.basicConfig(level=logging.DEBUG)
> logging.debug("this will now get logged")

---

logging default log level

> logging.WARNING

---

Config logging to log in the format `DATETIME LEVEL MESSAGE`

> ```python
> import logging
> logging.basicConfig(format='%(asctime)s %(level)s %(message)s')
> ```

---

log stack trace in exception

> Use `logging.error("custom msg", exc_info=True)` or use `logging.exception("custom msg")`
> 
> ```python
> import logging
> try: 
>     99 / 0 
> except Exception as e:
>     logging.error("Exception occured:", exc_info=True)
> ```

---

# TODO: Custom logger