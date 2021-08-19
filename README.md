# xk6-file
[k6](https://go.k6.io/k6) extension for writing files, implemented using the
[xk6](https://github.com/k6io/xk6) system.

## Build
```shell
xk6 build --with github.com/avitalique/xk6-file@latest
```

## Example
```javascript
import file from 'k6/x/file';

const filepath = 'sample-output.txt';

export default function () {
    file.writeString(filepath, 'New file. First line.\n');
    file.appendString(filepath, `Second line. VU: ${__VU}  -  ITER: ${__ITER}`);
}
```

## Run sample script
```shell
./k6 run sample-script.js
```
