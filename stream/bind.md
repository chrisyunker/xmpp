## Bind

xmlns: urn:ietf:params:xml:ns:xmpp-bind

### Set bind

__request__
```xml
<iq id="iq_1" type="set">
  <bind xmlns="urn:ietf:params:xml:ns:xmpp-bind">
    <resource>mac</resource>
  </bind>
</iq>
```

__response__
```xml
<iq id="iq_1" type="result">
  <bind xmlns="urn:ietf:params:xml:ns:xmpp-bind">
    <jid>chris@yunker.io/mac</jid>
  </bind>
</iq>
```

