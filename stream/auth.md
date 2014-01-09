## SASL Authentication

xmlns: urn:ietf:params:xml:ns:xmpp-sasl

### Authenticate plain

__request__
```xml
<auth xmlns="urn:ietf:params:xml:ns:xmpp-sasl" mechanism="PLAIN">ABCD==</auth>
```

__response__
```xml
<success xmlns="urn:ietf:params:xml:ns:xmpp-sasl" />
```

