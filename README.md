# CPP.LI Shorten URLs
A simple bash script to shorten URLs with [CPP.LI](https://cpp.li) 


## Installation
### macOS
```shell
wget -O cppli cpp.li/rwbq5 && chmod +x cppli && mv cppli /usr/local/bin/
```
### Linux
```shell
wget -O cppli cpp.li/rwbq5 && chmod +x cppli && mv cppli /usr//bin/
```

## Usage

Shorten a long URL :

```bash
$> cppli https://www.baidu.com
https://cpp.li/xdt4e
```

Shorten a long URL and provide a custom keyword and a custom title :

```bash
$> cppli https://www.google.com -k google
https://cpp.li/google
```

Shorten a URL and receive JSON output, for instance to display with `jq` :
```bash
$> cppli https://www.baidu.com -f json | jq
{
  "status": "success",
  "code": "",
  "message": "https://www.baidu.com added to database",
  "errorCode": "",
  "statusCode": 200,
  "url": {
    "keyword": "kn1an",
    "url": "https://www.baidu.com",
    "title": "百度一下，你就知道",
    "date": "2022-04-26 01:25:03",
    "ip": "103.197.71.19"
  },
  "title": "百度一下，你就知道",
  "shorturl": "https://cpp.li/kn1an"
}
```

Display help message :
```bash
$> cppli --help
```
![a4e051fea1266b1309586](https://telegraph.eowo.us/file/a4e051fea1266b1309586.png)

## License

Do whatever the hell you want with it



