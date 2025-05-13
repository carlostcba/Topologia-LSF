
```mermaid
flowchart LR
    %% Estilos
    classDef core fill:#4285F4,stroke:#2A56C6,color:white;
    classDef distribucion fill:#34A853,stroke:#2E7D32,color:white;
    classDef acceso fill:#FBBC05,stroke:#E8A203,color:black;
    classDef especial fill:#EA4335,stroke:#C62828,color:white;

    %% Núcleo
    RF[fa:fa-shield-alt Router Fortigate]:::core --> C01[fa:fa-network-wired 01 - SW SEC PA - DATACENTER (FO)]:::core

    %% SECUNDARIA
    C01 --> S03[fa:fa-project-diagram 03 - SW SEC PA - DATACENTER]:::distribucion
    S03 --> F03[fa:fa-random 03 - 00 Flex DATACENTER]:::distribucion --> FLEX1[fa:fa-plug 15 - SW FLEX GARITA MALAVER]:::acceso
    S03 --> S031[SW GEN L2 SECRE / DIR SEC BASICO]:::acceso
    S03 --> S032[SW GEN L2 TICS (Corina)]:::acceso
    S03 --> S033[SW GEN L2 ENTREPISO BIBLIOTECA]:::acceso
    S03 --> S034[SW GEN L2 PRECEPTORIA 310]:::acceso
    S03 --> S035[SW GEN L2 LAB FISICA]:::acceso
    S03 --> S036[SW GEN L2 COMUNICACIONES]:::acceso
    S03 --> S037[SW GEN L2 UNIFORMES]:::acceso

    C01 --> S04[fa:fa-project-diagram 04 - SW SEC02 - STELA NEW]:::distribucion
    S04 --> E10[10 - SW ED. FISICA 24B]:::acceso --> M13[SW MUSICA 8B]:::acceso
    S04 --> P11[11 - SEC PA SALA PROF]:::acceso --> SPROF[SW GEN L2 SALA PROF]:::acceso
    S04 --> FLEX2[fa:fa-plug 15 - SW FLEX GARITA MALAVER]:::acceso

    C01 --> S05[fa:fa-project-diagram 05 - SW PRECEPTORIA 210 10GB]:::distribucion --> P14[SW SEC PA - PRECEPTORIA 252]:::acceso

    %% TECNICA
    C01 --> S06[fa:fa-tools 06 - SW TECNICA - LAB DOMOTICA]:::distribucion
    S06 --> T17[17 - SW SEC SS TANGO - FABLAB]:::acceso --> TANGO[SW GEN L2 TANGO]:::acceso
    S06 --> ELEC1[SW GEN L2 ELEC 1]:::acceso
    S06 --> ELEC2[SW GEN L2 ELEC 2]:::acceso
    S06 --> ELEC3[SW GEN L2 ELECTRICIDAD]:::acceso
    S06 --> LIDE[SW GEN L2 LIDE]:::acceso

    %% PRIMARIA
    C01 --> S07[fa:fa-school 07 - SW - PRIMARIA AUXILIARES]:::distribucion
    S07 --> P08[SW PRIMARIA PA - ESCALERA]:::acceso
    S07 --> K07[SW FLEX KIOSKO PRIMARIA]:::acceso --> RMIK[fa:fa-wifi ROUTER MIKROTIK MODO SW]:::especial
    S07 --> D02[SW PRI PB DEPTO IT]:::acceso
    S07 --> G16[PRI PB AULA 21 (GIM CHICO)]:::acceso
    S07 --> EOE[SW GEN L2 EOE PRIMARIA]:::acceso
    S07 --> SPRI[SW GEN L2 SECRETARIA PRIMARIA]:::acceso

    %% JARDIN
    C01 --> S09[fa:fa-seedling 09 - JARDIN - DIRECCION_V2]:::distribucion
    S09 --> L12[12 - SW LAB ENERGIAS 24P]:::acceso
    L12 --> LC1[SW GEN L2 LAB 1 COMP]:::acceso
    L12 --> LC2[SW GEN L2 LAB 2 COMP]:::acceso
    L12 --> LE3[SW GEN L2 LAB 3 ENERGIAS]:::acceso
    L12 --> CNC[SW GEN L2 LAB 2 CNC]:::acceso
    L12 --> KSEC[SW GEN L2 KIOSCO SEC SEC]:::acceso
```
