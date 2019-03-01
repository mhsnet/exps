# 开始(hello) [《MHS 学习笔记》] -> [《Node 指南》] (mhs2019.2.28)

- [hello代码]
- [hello运行]

## <span id="code">hello代码</span> [开始(hello)]
> hello.js
```
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

## <span id="run">hello运行</span> [开始(hello)]
```
$ node hello.js
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/note/ "《MHS 学习笔记》"
[《Node 指南》]: https://mhsnet.github.io/note/node/guide/index.html "《Node 指南》"
[开始(hello)]: https://mhsnet.github.io/note/node/guide/start/hello.html "开始(hello)"

[hello代码]: https://mhsnet.github.io/note/node/guide/start/hello.html#code "hello代码"
[hello运行]: https://mhsnet.github.io/note/node/guide/start/hello.html#run "hello运行"