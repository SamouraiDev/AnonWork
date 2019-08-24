sequenceDiagram
    Note over Client,Server: << WEBSOCKET >>

    Note left of Client: Connecting...
    Client->>+Server: subscribe pool
    Server -->>-Client: SubscribePoolResponse

    Note left of Client: Waiting for a mix...
    Note over Client,Server: ... A new mix starts!
    Server-->>Client: ConfirmInputMixStatusNotification

    Note left of Client: Trying to join a mix...
    Client->>+Server: ConfirmInputRequest
    Note over Client,Server: ... Freeriders wait here for a free mix
    
    Server -->>-Client: ConfirmInputResponse
    Note left of Client: Joined a mix!
    Note over Client,Server: ... Waiting for enough peers

    Note over Client,Server: ... Anonymity set reached!

    Server -->>+Client: RegisterOutputMixStatusNotification
    Note left of Client: Registering output...

    Note over Client / alt. identity,Server: << REST >> from alternate identity
    Client / alt. identity->>-Server: RegisterOutputRequest
    Note left of Client: Registered output

    Note over Client,Server: ... All outputs registered!

    Server -->>+Client: SigningMixStatusNotification
    Note left of Client: Signing...
    Client->>-Server: SigningRequest
    Note left of Client: Signed

    Note over Client,Server: ... All signed!
    Server -->>+Client: SuccessMixStatusNotification
