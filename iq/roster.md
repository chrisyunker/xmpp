## Roster

xmlns: jabber:iq:roster

### Get roster

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
  </query>
</iq>
```

### Set roster

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


### Subscribe

__user1 subscribes to user2__

__user1 sends request__
```xml
<presence type='subscribe' to='user2@yunker.io'/>
```

__user2 receives request__
```xml
<presence from='user1@yunker.io' to='user2@yunker.io/res1' type='subscribe'/>
```

__user1 receives roster push__
```
<iq to='user1@yunker.io/mac' from='user1@yunker.io' id='push1' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item ask='subscribe' subscription='none' jid='user2@yunker.io'>
      <group/>
    </item>
  </query>
</iq>
```


__user1 updates roster__
```
<iq id='2' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item jid='user2@yunker.io' nick='user2'>
      <group>General</group>
    </item>
  </query>
</iq>
```

__user1 receives result__
```
<iq to='user1@yunker.io/xiff' from='user1@yunker.io' id='2' type='result'/>
```

__user1 receives roster push__
```
<iq to='user1@yunker.io/mac' from='user1@yunker.io' id='push1' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item ask='subscribe' subscription='none' jid='user2@yunker.io' nick='user2'>
      <group>General</group>
    </item>
  </query>
</iq>
```


__user2 accepts request from user1__
```xml
<presence type='subscribed' to='user1@yunker.io'/>
```

__user2 receives roster push__
```
<iq to='user2@yunker.io/mac' from='user2@yunker.io' id='push2' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item subscription='both' jid='user1@yunker.io'>
      <group/>
    </item>
  </query>
</iq>
```

__user1 receives ack from user2__
```xml
<presence from='user2@yunker.io' to='user1@yunker.io/res1' type='subscribed'/>
```

__user1 receives roster push__
```
<iq to='user1@yunker.io/mac' from='user1@yunker.io' id='push3' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item subscription='both' jid='user2@yunker.io' nick='user2'>
      <group>General</group>
    </item>
  </query>
</iq>
```


__user2 updates roster__
```
<iq id='3' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item jid='user1@yunker.io' nick='user1'>
      <group>General</group>
    </item>
  </query>
</iq>
```

__user2 receives result__
```
<iq to='user2@yunker.io/xiff' from='user2@yunker.io' id='3' type='result'/>
```

__user2 receives roster push__
```
<iq to='user2@yunker.io/mac' from='user2@yunker.io' id='push4' type='set'>
  <query xmlns='jabber:iq:roster'>
    <item subscription='both' jid='user1@yunker.io' nick='user1'>
      <group>General</group>
    </item>
  </query>
</iq>
```

