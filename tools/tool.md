
## 1 将IP转换为Long类型的数字,然后和Ip段作比较

``` scala
def ipToLong(ip: String): Long = {

    val arr: Array[String] = ip.split("\\.")
    var ipNum: Long = 0
    arr.foreach(ip => {
      ipNum = ip.toLong | ipNum << 8L

    })
    ipNum
  }
```
