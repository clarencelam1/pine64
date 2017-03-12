Following step 23 from pine64_setup.md:

```
$ wget https://nodejs.org/dist/v6.10.0/node-v6.10.0-linux-x64.tar.xz
$ tar -xvf node-v6.10.0-linux-x64.tar.xz
$ cd node-v6.10.0-linux-arm64
$ sudo cp -R * /usr/local/
$ sudo rm CHANGELOG.md LICENSE README.md
```

Then you should get:

`$ node -v`

v6.10.0

`$ npm -v`

3.10.3
