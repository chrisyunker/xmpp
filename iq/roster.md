## jabber:iq:roster

### get roster

__request__
```xml
<iq id='1' type='get'>
  <query xmlns='jabber:iq:roster'/>
</iq>
```

__response__
```xml
<iq from='user1@yunker.io' to='user1@yunker.io/res1' id='1' type='result'>
  <query xmlns='jabber:iq:roster'>
    <item subscription='both' name='user2' jid='user2@yunker.io'/>
  </query>i
</iq>
```

### set roster

__request__
```xml
<iq id='1' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item name='user2' jid='user2@yunker.io'>
      <group>general</group>
    </item>
  </query>
</iq>
```

__response__


### subscribe

__user1 subscribes to user2__
```xml
<presence type='subscribe' to='user2@yunker.io'/>
```

__user2 receives request from user1__
```xml
<presence from='user1@yunker.io' to='user2@yunker.io/res1' type='subscribe'/>
```

__user2 accepts request from user1__
```xml
<presence type='subscribed' to='user1@yunker.io'/>
```

__user1 receives ack from user2__
```xml
<presence from='user2@yunker.io' to='user1@yunker.io/res1' type='subscribed'/>
```
