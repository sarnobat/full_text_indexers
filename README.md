# full_text_indexers

### Swish++
```
  
  find  -iname "*.htm*" | tee /tmp/html_files.txt
  cat /tmp/html_files.txt | index++ --index-file /tmp/swish++.index --verbosity 4 --pattern 'html:*.htm*' -e 'text:*.txt' -
```
```
  cat du_files.txt  | perl -pe 's{^.*?\s+}{}g' | grep '.htm' | index++ --index-file /tmp/swish++.index --verbosity 4 --pattern 'html:*.htm*' -e 'text:*.txt' --temp-dir /media/sarnobat/ebay/trash/ -
```

```
  cd web
  search++ --max-results 1000 -i /media/sarnobat/ebay/swish++.index mysearchterm
```

```
  cd web
  search++ --dump-index
```

### Recoll
```
cat html_files.txt | RECOLL_TMPDIR=/media/sarnobat/cache_recoll recollindex -if -c /media/sarnobat/cache_recoll/recoll_index/
ls ~/.recoll

recollq -c /media/sarnobat/cache_recoll/recoll_index/  'mysearchterm -myexcludedterm mime:text/html'
```

### Tracker
```
  sudo apt install -y tracker
  tracker3 index
  tracker3 index --add videos/
```
### Others
* strigi
* xapian
* puggle
