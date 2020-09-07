1. npm 5.2 之后新增的命令，作用在于方便命令行调用内置模块
2. 原理：到 node_modules/.bin 和系统环境变量\$PATH 下检查命令是否存在，所以 npx 可以直接使用系统命令，Bash 内置命令不可以用 npx 因为不在环境变量里面比如 cd
3. 避免全局安装模块，比如 npx create-react-app my-app 是把 cra 下载到临时目录避免全局安装，只要 npx 后面的模块无法在本地发现就会下载一个同名模块
4. --no-install 参数：强制使用本地模块，如果没发现本地模块则报错
5. --ignore-existing 参数：忽略本地模块而强制使用远程模块
6. 使用不同版本的 node，比 nvm 方便
