
Moving from here to there:

```
pax -w local_dir | ssh user@remote_host "cd /path/to/destination && pax -r"
```

or moving from there to here:

```
ssh user@remote_host "cd /path/to/ && pax -w destination" | pax -r
```
