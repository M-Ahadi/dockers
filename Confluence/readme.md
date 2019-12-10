https://tech.cuixiangbin.com/?p=1248

export JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar ${JAVA_OPTS}"

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p conf -m aaa@bbb.com -n my_name -o mydomain.com -s BN4A-034I-D4H8-9OCZ

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p tc -m aaa@bbb.com -n my_name -o mydomain.com -s BN4A-034I-D4H8-9OCZ

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p questions -m aaa@bbb.com -n my_name -o mydomain.com -s BN4A-034I-D4H8-9OCZ
