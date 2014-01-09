## Privacy

xmlns: jabber:iq:privacy

### Get privacy list names

__request__
```xml
<iq id='1' type='get'>
  <query xmlns='jabber:iq:privacy'/>
</iq>
```

__response__
```xml
<iq from='user1@yunker.io' to='user1@yunker.io/res1' id='1' type='result'>
  <query xmlns='jabber:iq:privacy'>
    <list name='list1'/>
  </query>
</iq>
```

### Get specific privacy list

__request__
```xml
<iq id='1' type='get'>
  <query xmlns='jabber:iq:privacy'>
    <list name='list1'/>
  </query>
</iq>
```

__response__
```xml
<iq from='user1@yunker.io' to='user1@yunker.io/res1' id='1' type='result'>
  <query xmlns='jabber:iq:privacy'>
    <list name='list1'>
      <item type='jid' value='user2@yunker.io' action='deny' order='1'/>
    </list>
  </query>
</iq>
```

### Set privacy

__request__
```xml
<iq id='1' type='set'>
  <query xmlns='jabber:iq:roster'>
    <list name="list1">
      <item action='deny' order='1' type='jid' value='user2@yunker.io'/>
    </list>
  </query>
</iq>
```

__response__
```xml
<iq from='user1@yunker.io' to='user1@yunker.io/res1' id='1' type='result'/>
```

