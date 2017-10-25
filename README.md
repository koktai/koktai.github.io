# 國臺對照活用辭典
https://koktai.github.io/

## Source code project
https://github.com/a-tsioh/koktai-polymer

## How to update this websits
- Clone source code from https://github.com/a-tsioh/koktai-polymer
```
git clone https://github.com/a-tsioh/koktai-polymer
cd koktai-polymer/
```

- Install packages
```
bower install
gulp install -g polymer-cli
```

- Build
```
polymer build
```

- Test in local ( http://localhost:8888 )
```
polymer serve build/default --port 8888
```
- if everythings fine, update to github pages
```
cd ..
git clone git@github.com:koktai/koktai.github.io.git
cd koktai.github.io
git checkout gh-pages
rm -rf css/ data/ font/ img/ js/ src/ vendor/ index.html
/bin/cp -fpr ../koktai-polymer/build/default/* ./


# test before commit/push
# becouse pages hosts in github, use http server for testing without polymer.
python -m SimpleHTTPServer 8888

# DON'T USE THIS
#polymer serve --port 8888


# commit & push if page looks fine
git add . && git commit -m "update gh-pages"

git checkout master
git merge gh-pages
git push --all
```

- Then check website https://koktai.github.io/

## Contributors

- [a-tsioh](https://github.com/a-tsioh)
- [kilfu0701](https://github.com/kilfu0701)

## Lincense
