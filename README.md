# promissive
call your cb-based func in promissive manner


# usage

``` javascript
request.promise(options).then((res) => {
    //your logic here
});
```

is equiv-to:

``` javascript
return new Promise((resolve, reject) => {
    request(options, (err, res) => {
        return resolve(res);
    });
});
```