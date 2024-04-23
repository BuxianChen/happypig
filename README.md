# happypig

A demo for

- `argparser`: subparser
- package with multiple cli entrypoints.
- packaging by [build backend](https://packaging.python.org/en/latest/glossary/#term-Build-Backend) `setuptools` and `setup.py` with [src layout](https://packaging.python.org/en/latest/discussions/src-layout-vs-flat-layout/)
- [build frontend](https://packaging.python.org/en/latest/glossary/#term-Build-Frontend) using `build`

**packaging**

```bash
python -m pip install -U build twine
python -m build
twine upload dist/*  # enter PyPI token
```

**install**

install from PyPI

```
pip install happypig
```

or you can just use pip [VCS support](https://pip.pypa.io/en/stable/topics/vcs-support/) to install the latest version

```bash
pip install git+https://github.com/BuxianChen/happypig.git
```

**Usage**

```python
from happypig import saying
print(saying("a happy pig", "hang"))  # 'a happy pig saying: hang'
```

```bash
happypig list
python -m pip install tabulate
happypig list --pretty

happypig run

happypig run -n happypig -c hang

happypig-random
```


```
# happypig list
🐀 happy rat (子鼠) saying: jiji
🐂 happy ox (丑牛) saying: mooo
🐅 happy tiger (寅虎) saying: 
🐇 happy rabbit (卯兔) saying: 
🐉 happy dragon (辰龙) saying: 
🐍 happy snake (巳蛇) saying: sisi
🐎 happy horse (午马) saying: 
🐏 happy sheep (未羊) saying: mieee
🐒 happy monkey (申猴) saying: 
🐓 happy rooster (酉鸡) saying: 
🐕 happy dog (戌狗) saying: wang
🐖 happy pig (亥猪) saying: heng

# happypig list --pretty
+----------------------+-----------+
| animal               | content   |
+======================+===========+
| 🐀 happy rat (子鼠)     | jiji      |
+----------------------+-----------+
| 🐂 happy ox (丑牛)      | mooo      |
+----------------------+-----------+
| 🐅 happy tiger (寅虎)   |           |
+----------------------+-----------+
| 🐇 happy rabbit (卯兔)  |           |
+----------------------+-----------+
| 🐉 happy dragon (辰龙)  |           |
+----------------------+-----------+
| 🐍 happy snake (巳蛇)   | sisi      |
+----------------------+-----------+
| 🐎 happy horse (午马)   |           |
+----------------------+-----------+
| 🐏 happy sheep (未羊)   | mieee     |
+----------------------+-----------+
| 🐒 happy monkey (申猴)  |           |
+----------------------+-----------+
| 🐓 happy rooster (酉鸡) |           |
+----------------------+-----------+
| 🐕 happy dog (戌狗)     | wang      |
+----------------------+-----------+
| 🐖 happy pig (亥猪)     | heng      |
+----------------------+-----------+

# happypig run
🐖 happy pig (亥猪) saying: heng

# happypig run -n happypig -c hang
happypig saying: hang

# happypig-random
🐀 happy rat (子鼠) saying: jiji
```