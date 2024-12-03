# PIP Change Source

## Source List

- Tsinghua: https://pypi.tuna.tsinghua.edu.cn/simple
- Aliyun: https://mirrors.aliyun.com/pypi/simple
- Douban: https://pypi.douban.com/simple
- USTC: https://pypi.mirrors.ustc.edu.cn/simple
- Tencent: https://mirrors.cloud.tencent.com/pypi/simple

## Instant Change Source

```Bash
pip install your_package -i https://pypi.tuna.tsinghua.edu.cn/simple
```

## Config Change Source


Create file `～/.pip/pip.conf`
```Conf
[global]
index-url=https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host=pypi.tuna.tsinghua.edu.cn
```