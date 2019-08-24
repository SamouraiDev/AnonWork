graph TD

classDef ext fill:#faf9f9,stroke:#888,stroke-width:2px;

GUI[Whirlpool-GUI] -->|rest CLI api|CLI[Whirlpool-CLI]
CLI -->CLIENT[Whirlpool-client]

CLIENT -->|websocket + rest|PROTOCOL{Whirlpool-protocol}

SERVER[Whirlpool-server] -->|websocket + rest|PROTOCOL

class DOJO ext
