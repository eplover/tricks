| 表达式 | 匹配 |
| :---: | :---: |
| /^\s*$/ | 空行 |
| /<\s*(\S+)(\s[^>]*)?>[\s\S]*<\s*\/\1\s*>/ | HTML 标记 |
| /[\u4e00-\u9fa5]/ | 汉字 |

* 正则表达式

  `*`：零次或多次匹配   
  `+`：一次或多次匹配   
  `?`：零次或一次匹配   

* 匹配身份证号

  身份证号为15位或者18位。15位时全为数字，18位前17位位数字，最后一位是校验位，可能为数字或字符X

  ```javascript
  var reg = /(^\d{15}$)|(^\d{18}$)|(^\d{17}[\dxX]$)/
  ```

* 匹配手机号码

  ```javascript
  var reg = /((\d{11})|^((\d{7,8})|(\d{4}|\d{3})-(\d{7,8})|(\d{4}|\d{3})-(\d{7,8})-(\d{4}|\d{3}|\d{2}|\d{1})|(\d{7,8})-(\d{4}|\d{3}|\d{2}|\d{1}))$)/
  ```