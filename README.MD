1���������¹���IP�б�chnroute.txt

```
curl 'http://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest' | grep ipv4 | grep CN | awk -F\| '{ printf("%s/%d\n", $4, 32-log($5)/log(2)) }' > chnroute.txt
```

2���ϲ�chnroute.txt������chnroute_merged.txt

3��������/12�����ϸĳ�/11�����ϲ�������11_143.txt

4�����ɲ���������cn-no-route.txt

5����������IP���ϲ�������cn-no-route2.txt


ocserv��Ҫ�޸�src/vpn.h��֧�ֳ���96��(ocservĬ��ֵ)��������200��(Cisco AnyConnect���ֵ)��·�ɱ�:

```
#define MAX_CONFIG_ENTRIES 96 
```

96��Ϊ200����