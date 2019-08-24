graph TD

classDef blue fill:#faf9f9,stroke:#888,stroke-width:2px;

DSK(Desktop)-->GUI
GUI[Whirlpool-gui] -->CLIAPI{cli-api}
DEV(Third-party software)-->CLIAPI

CLIAPI -->|rest|CLI[Whirlpool-cli]
CMD(Command-line)-->|java -jar|CLI

CLI-->CLIENT[Whirlpool-client]
WALLET(Android)-->CLIENT
class DSK,DEV,CMD,WALLET blue
