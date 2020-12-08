## build mirador3 with [esbuild](https://github.com/evanw/esbuild)


bump deps 
```
ncu -u
Upgrading /private/tmp/mirador-integration/package.json
[====================] 9/9 100%

 css-loader                ^3.6.0  →   ^5.0.1     
 mirador              ^3.0.0-rc.4  →   ^3.0.0     
 mirador-image-tools       ^0.8.0  →  ^0.10.0     
 react                   ^16.13.1  →  ^17.0.1     
 react-dom               ^16.13.1  →  ^17.0.1     
 style-loader              ^1.2.1  →   ^2.0.0     
 webpack                  ^4.43.0  →  ^5.10.0     
 webpack-cli              ^3.3.12  →   ^4.2.0
 ```

 ```
 npm install
 ```

 install esbuild

 ```
 npm install esbuild
```

build

```
time ./node_modules/.bin/esbuild src/index.js \
    --bundle \
    --define:process.env.NODE_ENV=\"production\" \
    --outfile=esbuild/mirador.js \
    --minify \
    --external:'domain'
```

!!!
```
1.10s user 0.28s system 261% cpu 0.528 total
```


open [esbuild/index.html](http://tilde.club/~atomotic/m3/)
