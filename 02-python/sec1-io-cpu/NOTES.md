Profile code with builtin tool

Notice now using cache speeds up by reducing network I/O,
leaving disk I/O dominates runtime.

```
// without cache
python -m cProfile -s cumulative load.py 01044099999,02293099999 2021-2021 > profile.txt

// with cache
python -m cProfile -s cumulative load_cache.py 01044099999,02293099999 2021-2021 > profile_cache.txt
```