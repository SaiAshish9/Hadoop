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

sudo start-all.sh

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
12032 ResourceManager
10177 
16114 DataNode
563 jenkins.war
16006 NameNode
22647 Jps
22574 NodeManager

hadoop fs -mkdir /input

hadoop fs -put input.txt  /input

hadoop jar target/WordCount-1.0-SNAPSHOT.jar org.sai.WC_Runner /input/input.txt /output


localhost:8088
part 00000

hadoop fs -cat /output/part-000000
```

<img width="1246" alt="Screenshot 2023-03-25 at 11 54 18 AM" src="https://user-images.githubusercontent.com/43849911/227700740-e526ac4c-4f43-4242-b5f7-b6f3c9aad715.png">

<img width="820" alt="Screenshot 2023-03-25 at 11 58 14 AM" src="https://user-images.githubusercontent.com/43849911/227700884-c634f163-ab9e-4adf-843b-ffb583e967c3.png">

<img width="768" alt="Screenshot 2023-03-25 at 12 02 51 PM" src="https://user-images.githubusercontent.com/43849911/227701081-88a94d1f-d5ed-4911-b2ac-e58a99190ea4.png">



