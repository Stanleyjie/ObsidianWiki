fatal: unable to access 'https://github.com/Stanleyjie/ObsidianCareer.git/': HTTP/2 stream 1 was not closed cleanly before end of the underlying stream
```JSON
git config --global http.version HTTP/1.1
```

fatal: unable to access 'https://github.com/Stanleyjie/ObsidianCareer.git/': Failed to connect to github.com port 443 after 21102 ms: Couldn't connect to server
解决这个问题只需要用两个步骤
```JSON
git config --global http.proxy http://127.0.0.1:[代理端口]
git config --global https.proxy http://127.0.0.1:[代理端口]
```
取消代理
```JSON
git config --global --unset http.proxy
git config --global --unset https.proxy
```

fatal: unable to access 'https://github.com/Stanleyjie/ObsidianCareer.git/': Empty reply from server