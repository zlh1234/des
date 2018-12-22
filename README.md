#### DES对称加密算法

---

> 为解决中文乱码的问题，采用了base64加密。

> 先将明文使用base64加密，再使用des加密。
##### 使用方法：
###### 1.引入JS文件
```
<script src="des.min.js"></script>
<script>
    //密钥
    var key = "custom key";
    //密文
    var value = "DES对称加密算法";
    //实例化
    var Des = new Des(key,value);
    //加密
    var ciphertext = Des.encrypt(key,value);
    //解密
    var plaintext = Des.decrypt(key,ciphertext);
    console.log("密文 :",ciphertext);
    //95c55f672cfcd96920348ef3e6a2a46ea4747be745871b5760c52452fca93a2b
    console.log("明文:",plaintext);
    //DES对称加密算法
</script>
```
