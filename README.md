# MySQL
MySQL よくわかってないのでコードなおしてくれる人募集中

# Usage
```Java
MySQL mySql = new MySQL("USERNAME", "PASSWORD");
mySql.setAddress("Host:Port");
mySql.setDatabase("Database"); // 予め作成しておく必要があります。(create database NAME);
mySql.setTable("Table"); // なかった場合は作成します
mySql.setTimezone("JST/UTC");
mySql.setUseSSL(true|false);

Editor editor = null;
try {
	editor = mySql.connect();
} catch (SQLException e) {
	e.printStackTrace();
	return;
}

editor.set("key", "value");

String key = editor.get("key");

System.out.println("key value is " + key);
```

# Maven
- Repository
```XML
  <repositories>
    <repository>
      <id>net.simplyrin</id>
      <name>api</name>
      <url>https://api.simplyrin.net/maven/</url>
    </repository>
  </repositories>
```

- Dependency
```XML
  <dependencies>
    <dependency>
      <groupId>net.simplyrin.mysql</groupId>
      <artifactId>MySQL</artifactId>
      <version>1.0</version>
    </dependency>
  </dependencies>
```
