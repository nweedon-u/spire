# Server plugin: upstreamca-memory

The `upstreamca-memory` plugin is responsible for processing CSR requests for intermediate signing
certs (or from Agents if the user does not want the Server to retain signing material). This plugin
will manage/own the Trust Bundles for the Server, and act as the interface for upstream CAs.

The plugin maintains all state in memory, and is lost upon restart.

The plugin accepts the following configuration options:

| Configuration  | Description                           |
| -------------- | ------------------------------------- |
| trust_domain   | The trust domain                      |
| ttl            | The TTL for issued certificates       |
| cert_file_path | Path to the "upstream" CA certificate |
| key_file_path  | Path to the "upstream" CA key file    |