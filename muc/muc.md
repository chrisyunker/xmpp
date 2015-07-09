## MUC

xmlns: http://jabber.org/protocol/muc

### Join

__request__
```xml
<presence to='my_room@conference.yunker.io/'>
  <priority>0</priority>
  <x xmlns='http://jabber.org/protocol/muc'/>
</presence>
```

__response__
```xml
<presence xmlns='jabber:client' to='chris1@yunker.io/xiff' from='my_room@conference.yunker.io/yunker1'>
  <priority>0</priority>
  <x xmlns='http://jabber.org/protocol/muc#user'>
    <item jid='chris1@yunker.io/xiff' affiliation='none' role='participant'/>
    <status code='100'/>
    <status code='201'/>
  </x>
</presence>
```


### Send Presence

__request__
```xml
<presence to='my_room@conference.yunker.io/'>
  <show>chat</show>
  <status>status message</status>
  <priority>0</priority>
</presence>
```

__response__
```xml
<presence xmlns='jabber:client' to='chris1@yunker.io/xiff' from='my_room@conference.yunker.io/yunker1'>
  <show>chat</show>
  <status>status message</status>
  <priority>0</priority>
  <x xmlns='http://jabber.org/protocol/muc#user'>
    <item jid='chris1@yunker.io/xiff' affiliation='none' role='participant'/>
    <status code='100'/>
  </x>
</presence>
```


### Invite

__request__
```xml
<message id='1' to='room1@conference.yunker.io'>
  <x xmlns='http://jabber.org/protocol/muc#user'>
    <invite to='yunker2@yunker.io'>
      <reason>some reason</reason>
    </invite>
  </x>
</message>
```

__response__
```xml
<message to='yunker2@yunker.io' from='room1@conference.yunker.io' type='normal' inviter='yunker1@yunker.io/xiff'>
  <x xmlns='http://jabber.org/protocol/muc#user'>
    <invite from='yunker1@yunker.io/xiff'>
      <reason>some reason</reason>
    </invite>
  </x>
  <x xmlns='jabber:x:conference' jid='room1@conference.yunker.io'>some reason</x>
  <body>
    yunker1@yunker.io/xiff invites you to the room room1@conference.yunker.io
    (some reason)
  </body>
</message>
```

