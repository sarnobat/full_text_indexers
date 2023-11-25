# full_text_indexers

### Swish

### Swish++
```
  cd /3TB/new/
  find /3TB/new/ -iname "*.htm*" | tee ~/sarnobat.git/index/html_files.txt
  cat ~/sarnobat.git/index/html_files.txt | index++ --index-file /3TB/new/swish++.index --verbosity 4 --pattern 'html:*.htm*' -e 'text:*.txt' -
  cat /media/sarnobat/*/du_files.txt  | perl -pe 's{^.*?\s+}{}g' | grep '.htm' | index++ --index-file /media/sarnobat/ebay/swish++.index --verbosity 4 --pattern 'html:*.htm*' -e 'text:*.txt' --temp-dir /media/sarnobat/ebay/trash -
```

```
  cd /media/sarnobat/3TB/new/2020/web
  search++ --max-results 1000 -i /media/sarnobat/ebay/swish++.index mysearchterm
```

```
  cd /media/sarnobat/3TB/new/2020/web
  search++ --dump-index
```

### Recoll
```
cat /media/sarnobat/unmirrored/2021/sarnobat.git/index/html_files.txt | RECOLL_TMPDIR=/media/sarnobat/cache_recoll recollindex -if -c /media/sarnobat/cache_recoll/recoll_index/
ls ~/.recoll

recollq -c /media/sarnobat/cache_recoll/recoll_index/  'mysearchterm -myexcludedterm mime:text/html'
```

### Tracker
```
  sudo apt install -y tracker
  tracker3 index
  tracker3 index --add /media/sarnobat/3TB/2021/disks/thistle/videos
```
### Others
* strigi
* xapian
* puggle
