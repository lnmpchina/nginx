在nginx的项目中如果没有放置favicon.ico日志中会有大量错误
解决方法:
1.修改nginx配置,在server配置区块中添加如下配置:
<pre><code lang=config>
location = /favicon.ico {
  log_not_found off;
  access_log off;
}
</code></pre>
2.在项目目录中添加favicon.ico 文件.
