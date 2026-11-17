# ex02

criar vários arquivos com permissões diferentes:

```bash
chmod 755 test1   # rwxr-xr-x
chmod 600 test3   # rw-------
chmod 644 test4   # rw-r--r--
chmod 400 test5   # r--------
chmod 444 test6   # r--r--r--
```

empacotar tudo:
```bash
tar -cf exo2.tar test1 test3 test4 test5 test6
```

ve as permissões:
```bash
ls -l test*
```

