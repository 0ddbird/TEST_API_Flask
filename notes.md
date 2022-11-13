# App context

`import <file>` vs `from <file> import <object>`

## Doesn't work
```shell
PS E:\Code\Python\pyapi> python
>>> import app
>>> app.app_context().push()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: module 'app' has no attribute 'app_context'
```

## Works

```shell
PS E:\Code\Python\pyapi> python
>>> from app import app
>>> app.app_context().push()
>>> from app import db
>>> db.create_all()
```
