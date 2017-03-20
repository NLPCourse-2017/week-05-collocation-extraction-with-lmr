# NLP Lab. Course - Week 05: Collocation Extraction with Local MapReduce

Extracting Collocations from ngram using Local MapReduce

## word count
```console
$ cat citeseerx_descriptions_sents.txt.50000|python wc_map.py|sort|python count_reduce.py
```

## word count with local-mapreduce
```console
$ cat citeseerx_descriptions_sents.txt.50000|./lmr 1M 16 'python wc_map.py' 'python count_reduce.py' wordcount_result
```


## ngram count
```console
$ cat citeseerx_descriptions_sents.txt.50000|python wc_map.py|sort|python count_reduce.py
```

## ngram count with local-mapreduce
```console
$ cat citeseerx_descriptions_sents.txt.50000|./lmr 1M 16 'python nc_map.py' 'python count_reduce.py' ngramcount_result
```


## collocation extraction
```console
$ cat citeseerx_descriptions_sents.txt.50000|python extract_collocation.py
```


## collocation extraction with local-mapreduce
```console
$ cat citeseerx_descriptions_sents.txt.50000|./lmr 1M 16 'python coll_map.py' 'python coll_reduce.py' collocation_result
```
