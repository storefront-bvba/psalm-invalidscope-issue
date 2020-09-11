# Psalm suppress InvalidScope issue reproducer

https://github.com/vimeo/psalm/issues/4162

## How to reproduce

```
composer install
```

```
vendor/bin/psalm bad.phtml
```

expected result:
```
Scanning files...
Analyzing files...

░
------------------------------
No errors found!
------------------------------
```

actual result:
```
Scanning files...
Analyzing files...

E

ERROR: InvalidScope - bad.phtml:5:5 - Invalid reference to $this in a non-class context (see https://psalm.dev/013)
<?= $this


------------------------------
1 errors found
------------------------------
```
