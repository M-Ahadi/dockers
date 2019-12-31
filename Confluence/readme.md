https://tech.cuixiangbin.com/?p=1248

export JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar ${JAVA_OPTS}"

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p conf -m aaa@bbb.com -n my_name -o mydomain.com -s {your_server_id}

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p tc -m aaa@bbb.com -n my_name -o mydomain.com -s {your_server_id}

java -jar /opt/atlassian/confluence/confluence/WEB-INF/lib/atlassian-agent.jar -p questions -m aaa@bbb.com -n my_name -o mydomain.com -s {your_server_id}
