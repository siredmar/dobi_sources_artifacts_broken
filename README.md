# dobi_sources_artifacts_broken
This is a minimalist example to show two things:
- that the current dobi (0.14.0) breaks the sources/artifact system
- that sources won't work with real glob patterns

To try it out we use two different versions of dobi: 0.13.0 and 0.14.0
```
sudo curl -L https://github.com/dnephin/dobi/releases/download/v0.13.0/dobi-linux -o /usr/local/bin/dobi.13
sudo curl -L https://github.com/dnephin/dobi/releases/download/v0.14.0/dobi-linux -o /usr/local/bin/dobi.14
sudo chmod +x /usr/local/bin/dobi.13 /usr/local/bin/dobi.14
git clone https://github.com/siredmar/dobi_sources_artifacts_broken
cd dobi_sources_artifacts_broken
dobi.13 install
dobi.14 install
```

Have a look at dobi.yaml where the different cases are described.

I tried to narrow the error down to PR #184. I assume that those changes are breaking the sources/artifact system in dobi.
