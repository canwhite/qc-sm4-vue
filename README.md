# qc-sm4-vue
在vue中使用国密sm4作对称加密

## use  

```
//引入的时候注意相对位置
import sm4 from "../libs/sm4.js"
...



const msg = 'hello world! 我是 juneandgreen.' // 可以为 utf8 串或字节数组
const key = '0123456789abcdeffedcba9876543210' 
//可以为 16 进制串或字节数组，要求为 128 比特

let encryptData = sm4.encrypt(msg, key) // 加密，默认输出 16 进制字符串，默认使用 pkcs#5 填充
console.log('--encode--',encryptData);

let decodeData = sm4.decrypt(encryptData,key);//解密
console.log('--decode--',decodeData);




/*
输出：
--encode-- 726e28c1c032a3f16760e63b518e6c15e547c160bfdc54fcbffb7c8fadad926d594bc9d6d410e62dbacc5a9485181f50 Home.vue:30
--decode-- hello world! 我是 juneandgreen.

*/



```


