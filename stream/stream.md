## http://etherx.jabber.org/streams

### get authentication features

__request__
```xml
<?xml version="1.0"?>
<stream:stream to="yunker.io" xmlns="jabber:client" xmlns:stream="http://etherx.jabber.org/streams" version="1.0">
```

__response__
```xml
<?xml version='1.0'?>
<stream:stream xmlns="jabber:client" from="yunker.io" xml:lang="en" version="1.0" id="1" xmlns:stream="http://etherx.jabber.org/streams" />
<stream:features>
  <mechanisms xmlns="urn:ietf:params:xml:ns:xmpp-sasl">
    <mechanism>PLAIN</mechanism>
  </mechanisms>
  <c xmlns="http://jabber.org/protocol/caps" hash="sha-1" ver="thrxRBQjQmEoetQysFuvzmGWk9o=" node="http://www.process-one.net/en/ejabberd/" />
  <register xmlns="http://jabber.org/features/iq-register" />
</stream:features>
```

### get session features

__request__
```xml
<?xml version="1.0"?>
<stream:stream to="yunker.io" xmlns="jabber:client" xmlns:stream="http://etherx.jabber.org/streams" version="1.0">
```

__response__
```xml
<?xml version='1.0'?>
<stream:stream xmlns="jabber:client" from="yunker.io" xml:lang="en" version="1.0" id="2" xmlns:stream="http://etherx.jabber.org/streams" />
<stream:features>
  <bind xmlns="urn:ietf:params:xml:ns:xmpp-bind" />
  <session xmlns="urn:ietf:params:xml:ns:xmpp-session" />
  <c xmlns="http://jabber.org/protocol/caps" hash="sha-1" ver="thrxRBQjQmEoetQysFuvzmGWk9o=" node="http://www.process-one.net/en/ejabberd/" />
  <register xmlns="http://jabber.org/features/iq-register" />
</stream:features>
```

