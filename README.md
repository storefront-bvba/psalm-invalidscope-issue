# Psalm .html template issue reproducer

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
E

ERROR: UndefinedDocblockClass - bad.phtml:7:1 - Docblock-defined class or interface MyNamespace\Block\CustomBlocks does not exist (see https://psalm.dev/200)
/** @var CustomBlocks $block */

?>


------------------------------
1 errors found
------------------------------
```
