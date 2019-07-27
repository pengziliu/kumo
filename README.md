
>官方地址：https://github.com/kennycason/kumo

# 引入pom
> 核心包以及语言支持包

```
   <dependency>
            <groupId>com.kennycason</groupId>
            <artifactId>kumo-core</artifactId>
            <version>1.17</version>
        </dependency>

        <dependency>
            <groupId>com.kennycason</groupId>
            <artifactId>kumo-tokenizers</artifactId>
            <version>1.17</version>
        </dependency>
 ```
            
            
            
# 注意点
中文词云使用要同时使用中文解析器以及Font，否则会出现中文乱码，官方文档未指出！

```
//使用中文解析器
 frequencyAnalyzer.setWordTokenizer(new ChineseWordTokenizer());
 
 
//此处不设置会出现中文乱码
java.awt.Font font = new java.awt.Font("STSong-Light", 2, 18);
final WordCloud wordCloud = new WordCloud(dimension, CollisionMode.PIXEL_PERFECT);
wordCloud.setKumoFont(new KumoFont(font));
 
 ```
 

