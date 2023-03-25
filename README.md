<img width="894" alt="Screenshot 2023-03-24 at 11 48 09 PM" src="https://user-images.githubusercontent.com/43849911/227607759-641a9482-49c2-400f-a37d-c010782833bf.png">

<img width="678" alt="Screenshot 2023-03-24 at 11 48 40 PM" src="https://user-images.githubusercontent.com/43849911/227607853-aba0c11e-9219-4ad5-9407-edd52f26277d.png">

```
brew install hadoop

hadoop version
Hadoop 3.3.4
Source code repository https://github.com/apache/hadoop.git -r a585a73c3e02ac62350c136643a5e7f6095a3dbb
Compiled by stevel on 2022-07-29T12:32Z
Compiled with protoc 3.7.1
From source with checksum fb9dd8918a7b8a5b430d61af858f6ec
This command was run using /usr/local/Cellar/hadoop/3.3.4/libexec/share/hadoop/common/hadoop-common-3.3.4.jar

start-all.sh

stop-all.sh

https://towardsdatascience.com/installing-hadoop-on-a-mac-ec01c67b003c

echo export "AVARIABLE=example" >> ~/.bash_profile


```

https://towardsdatascience.com/installing-hadoop-on-a-mac-ec01c67b003c

<img width="1788" alt="Screenshot 2023-03-25 at 11 41 18 AM" src="https://user-images.githubusercontent.com/43849911/227700148-d41a92d0-f2fc-4619-9096-a3226f3237be.png">

<img width="910" alt="Screenshot 2023-03-25 at 11 41 47 AM" src="https://user-images.githubusercontent.com/43849911/227700169-81a9d310-d88d-4fd9-9b58-dcf332307e7b.png">

<img width="1177" alt="Screenshot 2023-03-25 at 11 42 22 AM" src="https://user-images.githubusercontent.com/43849911/227700205-9c90128d-1bc9-451f-8c19-b7b28c5ef4e4.png">

<img width="1325" alt="Screenshot 2023-03-25 at 11 43 06 AM" src="https://user-images.githubusercontent.com/43849911/227700246-fe589634-7a1a-422f-aca2-dbf6ee3c1300.png">

<img width="1300" alt="Screenshot 2023-03-25 at 11 43 21 AM" src="https://user-images.githubusercontent.com/43849911/227700257-cdcb7f94-a5ca-431d-a0a1-d8a84aeecf6e.png">

<img width="686" alt="Screenshot 2023-03-25 at 11 46 29 AM" src="https://user-images.githubusercontent.com/43849911/227700396-02f07f78-d964-4341-939f-d19a7afa7dc5.png">

```
jps
10177 
563 jenkins.war
24901 DataNode
26038 NodeManager
26109 Jps
24799 NameNode
25935 ResourceManager

hadoop fs -mkdir /input

hadoop fs -put input.txt  /input

hadoop jar target/WordCount-1.0-SNAPSHOT.jar org.sai.WC_Runner /input/input.txt /output

localhost:8088
part 00000

hadoop fs -cat /output/part-00000
```

<img width="1246" alt="Screenshot 2023-03-25 at 11 54 18 AM" src="https://user-images.githubusercontent.com/43849911/227700740-e526ac4c-4f43-4242-b5f7-b6f3c9aad715.png">

<img width="820" alt="Screenshot 2023-03-25 at 11 58 14 AM" src="https://user-images.githubusercontent.com/43849911/227700884-c634f163-ab9e-4adf-843b-ffb583e967c3.png">

<img width="768" alt="Screenshot 2023-03-25 at 12 02 51 PM" src="https://user-images.githubusercontent.com/43849911/227701081-88a94d1f-d5ed-4911-b2ac-e58a99190ea4.png">

```
hdfs dfs -cat /input/input.txt         
2023-03-25 12:11:47,547 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent egestas dui vel pharetra 
volutpat. Morbi suscipit sapien vitae commodo sagittis. Donec gravida efficitur sagittis. 
Nunc feugiat, magna eu ultrices placerat, justo augue iaculis mi, ut facilisis ex ex et 
libero. Phasellus diam est, tincidunt vel lorem ultrices, lacinia faucibus arcu. Mauris in 
laoreet neque. Morbi justo ante, rutrum a pharetra ac, pellentesque non enim. Cras accumsan 
ultricies dui. Quisque at ligula tellus. Donec eget quam in velit interdum vulputate. 
Integer nec ipsum vitae eros vulputate maximus sit amet id magna. Morbi sagittis, dui 
hendrerit congue varius, ante ex tristique ligula, eget fringilla est est sed justo. Nam 
pharetra diam a ante fringilla, in egestas orci dictum. Orci varius natoque penatibus et 
magnis dis parturient montes, nascetur ridiculus mus.

Phasellus sed nulla urna. Aliquam ac tincidunt massa. Nunc consequat accumsan consequat. 
Fusce nec dapibus dolor. Vivamus venenatis dapibus augue a hendrerit. Maecenas orci nisl, 
blandit a metus sed, faucibus ultrices ante. Fusce et rutrum leo.

Pellentesque maximus rutrum augue, vel vestibulum sem accumsan ut. Duis ligula justo, 
feugiat sit amet dapibus eu, sollicitudin quis enim. Donec ac laoreet turpis, sit amet 
porta nunc. Praesent posuere, dui ut fringilla mattis, ex massa dignissim massa, a semper 
magna leo ac nibh. Cras pharetra, augue at suscipit semper, erat sapien luctus libero, 
vitae vestibulum dui metus sit amet urna. Phasellus elementum scelerisque turpis, sit amet 
interdum urna dapibus ut. Morbi libero dui, ullamcorper sed erat ac, maximus commodo 
tortor. Nullam imperdiet mattis lectus sed aliquam. Aliquam erat volutpat. Pellentesque non 
mauris in sem euismod auctor. Duis accumsan facilisis lacus. Cras dictum est ut nisl 
pellentesque varius. Nullam vitae justo eget lorem scelerisque consectetur.

hdfs dfs -checksum /input/input.txt
2023-03-25 12:12:17,947 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
/input/input.txt	MD5-of-0MD5-of-512CRC32C	0000020000000000000000004b6394ce8ece871ab563a260a1f55a67
```

Installation
https://www.youtube.com/watch?v=H999fIuymqc
https://stackoverflow.com/questions/48978480/hadoop-permission-denied-publickey-password-keyboard-interactive-warning/49960886
export HADOOP_SSH_OPTS="-p 22"


<img width="651" alt="Screenshot 2023-03-25 at 12 24 42 PM" src="https://user-images.githubusercontent.com/43849911/227701988-7d45aa78-c2be-4b2b-952e-b543e66e2050.png">

<img width="1335" alt="Screenshot 2023-03-25 at 12 32 05 PM" src="https://user-images.githubusercontent.com/43849911/227702369-203725a2-e67e-4864-9dbc-e18ec4342305.png">

<img width="1788" alt="Screenshot 2023-03-25 at 12 32 41 PM" src="https://user-images.githubusercontent.com/43849911/227702395-6f54b10e-5860-45b7-a514-c5f7ec286a68.png">

<img width="1248" alt="Screenshot 2023-03-25 at 12 35 00 PM" src="https://user-images.githubusercontent.com/43849911/227702500-ddd44319-1cf3-4782-b449-d149b03796e3.png">

<img width="1788" alt="Screenshot 2023-03-25 at 12 35 50 PM" src="https://user-images.githubusercontent.com/43849911/227702535-4b1477f2-3bdc-4c95-8401-9737a80530d6.png">

<img width="1788" alt="Screenshot 2023-03-25 at 12 36 02 PM" src="https://user-images.githubusercontent.com/43849911/227702544-7b18b608-077e-4c0b-b28a-1ac8bddb15b4.png">

<img width="1783" alt="Screenshot 2023-03-25 at 12 36 30 PM" src="https://user-images.githubusercontent.com/43849911/227702564-72b28f27-61ba-41bf-b35b-aaeaf003b7f0.png">

<img width="1248" alt="Screenshot 2023-03-25 at 12 37 18 PM" src="https://user-images.githubusercontent.com/43849911/227702581-20322164-d619-498c-a4e6-69f622322834.png">

