
下载
>
1. 下载源码版本[ltp-3.3.2.tar.gz](https://github.com/HIT-SCIR/ltp/archive/v3.3.2.tar.gz)
2. 下载模型文件[ltp-data-v3.3.1.zip](https://pan.baidu.com/share/link?shareid=1988562907&uk=2738088569)

编译

```
tar zxvf ltp-3.3.2.tar.gz 
cd ltp-3.3.2
./configure 
```

模型文件

```
ltp-data-v3.3.1.zip
```
启动ltp_server

```
bin/ltp_server  --port=12345
```

http调用

```
curl http://127.0.0.1:12345/ltp -d "s=青云志第二季第10集延迟更新了&x=n&t=all"
```

xml结果

```
<?xml version="1.0" encoding="utf-8" ?>
<xml4nlp>
    <note sent="y" word="y" pos="y" ne="y" parser="y" wsd="n" srl="y" />
    <doc>
        <para id="0">
            <sent id="0" cont="青云志第二季第10集延迟更新了">
                <word id="0" cont="青云志" pos="n" ne="O" parent="5" relate="SBV" />
                <word id="1" cont="第二" pos="m" ne="O" parent="2" relate="ATT" />
                <word id="2" cont="季" pos="q" ne="O" parent="4" relate="ATT" />
                <word id="3" cont="第10" pos="m" ne="O" parent="4" relate="ATT" />
                <word id="4" cont="集" pos="q" ne="O" parent="5" relate="ADV" />
                <word id="5" cont="延迟" pos="v" ne="O" parent="-1" relate="HED">
                    <arg id="0" type="A0" beg="0" end="0" />
                </word>
                <word id="6" cont="更新" pos="v" ne="O" parent="5" relate="COO" />
                <word id="7" cont="了" pos="u" ne="O" parent="6" relate="RAD" />
            </sent>
        </para>
    </doc>
</xml4nlp>
```
