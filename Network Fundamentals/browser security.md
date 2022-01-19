# 浏览器安全

## Respawning cookies
https://en.wikipedia.org/wiki/Zombie_cookie

## Flash cookies
https://en.wikipedia.org/wiki/Local_shared_object

## Entity tags
https://en.wikipedia.org/wiki/HTTP_ETag

ETag 可用于跟踪唯一用户，随着 HTTP cookie 越来越多地被具有隐私意识的用户删除。 2011 年 7 月，Ashkan Soltani 和加州大学伯克利分校的一组研究人员报告说，包括 Hulu 在内的许多网站都在使用 ETag 进行跟踪。Hulu 和 KISSmetrics 都已于 2011 年 7 月 29 日停止“重生”，因为 KISSmetrics 及其 20 多个客户正面临集体诉讼，原因是使用“不可删除的”跟踪 cookie，部分涉及使用 ETag。

由于 ETag 由浏览器缓存并随对同一资源的后续请求返回，因此跟踪服务器可以简单地重复从浏览器接收到的任何 ETag，以确保分配的 ETag 无限期地持续存在（与持久性 cookie 类似）。 额外的缓存头也可以增强 ETag 数据的保存。

可以通过清除浏览器缓存来刷新 ETag（实现方式各不相同）
## Canvas fingerprinting
https://en.wikipedia.org/wiki/Canvas_fingerprinting

由于指纹主要基于浏览器、操作系统和安装的图形硬件，因此它不能唯一识别用户。 在一项有 294 名来自 Amazon 的 Mechanical Turk 参与者的小规模研究中，观察到了 5.7 位的实验熵。 该研究的作者表示，在野外可能会观察到更多的熵，并且指纹中使用的模式也更多。 虽然本身不足以识别个人用户，但该指纹可以与其他熵源结合以提供唯一标识符。 据称，由于该技术有效地对 GPU 进行指纹识别，因此熵与之前浏览器指纹技术（如屏幕分辨率和浏览器 JavaScript 功能）的熵“正交”。 