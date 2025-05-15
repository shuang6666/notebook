# Docker Useful Command

## 常用的快速环境部署

> 优点
> - 易于迁移
> - 环境隔离

- -v文件系统的映射挂载
- -p端口的映射
- -d进行后台运行
- -it中断模式进行运行
- --name设置创建的容器名称
- -w设置默认的工作路径

```Bash
docker run -d -it --name vending-frontend -v $(pwd):$(pwd) -p 10003:10003 -w $(pwd) node:10.24.1 /bin/bash
docker attach vending-frontend
```