# c_7707
虚拟币支付回调监听同步代码 TRX TRC20波场钱包PHP开发示例源码
<br/></br>
[下载地址](https://www.uuid2.com/7707.html "下载地址")
<br/></br>
<h3>源码简介：</h3>
<p>PHP版本，包括离线生成钱包地址、离线转账，TRX转账、TRC20转账、钱包归集<p>
<p>源码描述：<p>
<p>波场php版钱包实例，包括离线钱包生成、激活，TRX、TRC20转账，离线签名，账户归集，充值转账监听，使用fastadmin开发，带sql文件，使用workerman、think-queue做转账监听。<p>
<p>注意，这不是完整的支付源码，不是那种第四方的支付系统源码，下面的图片就是这个源码的截图，所以没技术的就不要下了。为了避免跟我一样盲目自行，我把安装后的图放下面，等下不会搞说我骗人。<p>
<p>只是集成到了一个开源的框架Bootstrap而已，后台FastAdmin，其实我也没搞明白，当时看到说是不需要自己搭建节点，在这个代码里面配置网络节点链接就可以，给需要的人吧，下面是原来对这个源码的介绍。<p>
<p>该代码希望你至少知道一些区块链的基础概念，如地址、公钥、私钥、合约等。如不清楚，就不要下了！！！<p>
<p>所有测试代码封装在 application common logic TronLogic.php中在，<p>
<p>转账和交易监听入口在 application push controller Worker.php中。<p>
<p>地址余额监听没有做区块同步，只是需要将监听到每个地址最后一次交易的区块记录下来，下次监听的时候就从最后查询到的区块开始监听，一直循环<p>
<p>接口测试可以在 application api controller Address.php中查看怎么调用的，编码环境在win+php7.4 Linux请注意目录大小写<p>
<p>归集和监听入口使用的是workerman 入口在根目录的server.php中 归集方法里面使用了 think-queue 队列 php think queue:work {队列名} 如果不会的会可以看看官方文档 都是最基础的使用方法哈<p>
<p>框架就是基于thinkphp5的fastadmin，安装就是tp5的安装方法，创建站点，配置伪静态，导入数据库，访问api模块里的address控制器里的方法就可以撸了啊 控制器里面注释也很清楚啊<p>
<p>后台地址：/ PWcRgnIzQK.php / index / login<p>
<p>这个是FastAdmin后台，所以密码忘记FastAdmin后台密码了怎么办？<p>
<p>数据库修改fa_admin表的两个字段<p>
<p>密码(password)：c13f62012fd6a8fdf06b3452a94430e5<p>
<p>密码盐(salt)：rpR6Bv<p>
<p>登录密码是 123456<p>
<h3>截图：</h3>
<img src="https://www.uuid2.com/wp-content/uploads/img/pro/20220218/16451661111856.jpg" alt="虚拟币支付回调监听同步代码 TRX TRC20波场钱包PHP开发示例源码"><img src="https://www.uuid2.com/wp-content/uploads/img/pro/20220218/1645166111467.jpg" alt="虚拟币支付回调监听同步代码 TRX TRC20波场钱包PHP开发示例源码"><img src="https://www.uuid2.com/wp-content/uploads/img/pro/20220218/1645166112352.jpg" alt="虚拟币支付回调监听同步代码 TRX TRC20波场钱包PHP开发示例源码"><img src="https://www.uuid2.com/wp-content/uploads/img/pro/20220218/16451661144725.jpg" alt="虚拟币支付回调监听同步代码 TRX TRC20波场钱包PHP开发示例源码">
