# Rev A BOM

58 BOM lines, **96 assembled parts**, every one of them placed on the board. The orderable files, `jlc-bom.csv` and `jlc-cpl.csv`, ship in the fabrication package attached to the release.

33 of the 96 sit on basic parts and 63 on extended ones, so 48 lines carry JLCPCB's one-time extended-part loading fee.

3 lines are not the part the design first asked for, because the original went end-of-life or out of stock:

- **C53** — Replacement for EOL C140935; 1.2pF 50V C0G 0402.
- **L10** — Replacement for discontinued C86083; 10uH 0603.
- **R9,R17,R18** — Alternate for C25744 (stock 0); 10k 0402 1%.

14 footprints are board features rather than parts — FID1-FID3, H1-H3, TP1-TP8 — and are not ordered.

| Qty | Designators | Value | Footprint | MPN | LCSC | Manufacturer |
|---:|---|---|---|---|---|---|
| 1 | C1 | 10uF/10V | `Capacitor_SMD:C_0805_2012Metric` | CL21A106KAYNNNE | C15850 | Samsung Electro-Mechanics |
| 3 | C2,C4,C23 | 10nF | `Capacitor_SMD:C_0402_1005Metric` | CL05B103KB5NNNC | C15195 | Samsung Electro-Mechanics |
| 4 | C6-C8,C28 | 10uF | `Capacitor_SMD:C_0805_2012Metric` | CL21A106KAYNNNE | C15850 | Samsung Electro-Mechanics |
| 4 | C10,C11,C34,C36 | 4.7uF | `Capacitor_SMD:C_0603_1608Metric` | CL10A475KO8NNNC | C19666 | Samsung Electro-Mechanics |
| 12 | C12-C15,C25,C26,C29-C33,C35 | 100nF | `Capacitor_SMD:C_0402_1005Metric` | CL05B104KO5NNNC | C1525 | Samsung Electro-Mechanics |
| 3 | C16,C17,C27 | 1uF | `Capacitor_SMD:C_0603_1608Metric` | CL10B105KA8NNNC | C29936 | Samsung Electro-Mechanics |
| 1 | C18 | 47nF | `Capacitor_SMD:C_0402_1005Metric` | CC0402KRX7R9BB473 | C272875 | YAGEO |
| 4 | C19-C22 | 12pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402JRNPO9BN120 | C106201 | YAGEO |
| 1 | C24 | 470nF | `Capacitor_SMD:C_0402_1005Metric` | CL05A474KP5NNNC | C47339 | Samsung Electro-Mechanics |
| 3 | C39,C40,C44 | 47pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402JRNPO9BN470 | C60137 | YAGEO |
| 2 | C41,C50 | 0.2pF | `Capacitor_SMD:C_0402_1005Metric` | CQ0402BRNPO9BNR20 | C1855077 | YAGEO |
| 1 | C42 | 3.0pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN3R0 | C327228 | YAGEO |
| 2 | C43,C45 | 5.6pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN5R6 | C505468 | YAGEO |
| 1 | C46 | 3.3pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN3R3 | C327287 | YAGEO |
| 1 | C47 | 4.0pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN4R0 | C541337 | YAGEO |
| 1 | C48 | 3.9pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN3R9 | C505474 | YAGEO |
| 1 | C49 | 1.8pF | `Capacitor_SMD:C_0402_1005Metric` | CC0402BRNPO9BN1R8 | C327209 | YAGEO |
| 1 | C51 | 0.8pF | `Capacitor_SMD:C_0402_1005Metric` | GJM1555C1HR80BB01D | C76915 | muRata |
| 1 | C52 | 0.5pF | `Capacitor_SMD:C_0402_1005Metric` | GJM1555C1HR50BB01D | C76911 | muRata |
| 1 | C53 | 1.2pF | `Capacitor_SMD:C_0402_1005Metric` | GJM1555C1H1R2WB01D | C76899 | muRata |
| 1 | D2 | SRV05-4 | `Package_TO_SOT_SMD:SOT-23-6` | SRV05-4.TCT | C13612 | SEMTECH |
| 1 | F1 | 0.5A | `Fuse:Fuse_1812_4532Metric` | SMD1812P050TF/30 | C12559 | RUILON |
| 1 | J1 | SOLAR | `Connector_JST:JST_PH_B2B-PH-K_1x02_P2.00mm_Vertical` | B2B-PH-K-S(LF)(SN) | C131337 | JST |
| 1 | J2 | LiFePO4 | `Connector_JST:JST_PH_B2B-PH-K_1x02_P2.00mm_Vertical` | B2B-PH-K-S(LF)(SN) | C131337 | JST |
| 1 | J3 | 2x3 1.27 | `Connector_PinHeader_1.27mm:PinHeader_2x03_P1.27mm_Vertical_SMD` | PZ127-2-03-S | C3975186 | HCTL |
| 1 | J4 | SOIL | `Connector_JST:JST_PH_B3B-PH-K_1x03_P2.00mm_Vertical` | B3B-PH-K-S(LF)(SN) | C131339 | JST |
| 1 | J5 | U.FL | `Connector_Coaxial:U.FL_Hirose_U.FL-R-SMT-1_Vertical` | U.FL-R-SMT-1(80) | C88374 | HRS |
| 1 | J6 | MM8130-2600 | `lora-node:COAXIAL-SWF` | MM8130-2600RB8 | C91633 | muRata |
| 1 | JP1 | MEAS | `Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical` | PZ254V-11-02P | C492401 | XFCN |
| 1 | L1 | 22uH | `Inductor_SMD:L_1210_3225Metric` | CBC3225T220KR | C223225 | Taiyo Yuden |
| 1 | L3 | 2.2uH | `Inductor_SMD:L_1210_3225Metric` | DFE322512F-2R2M=P2 | C3222669 | muRata |
| 1 | L10 | 10uH | `Inductor_SMD:L_0603_1608Metric` | MLZ1608N100LT000 | C194437 | TDK |
| 1 | L11 | 15nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN15NG00D | C98055 | muRata |
| 1 | L12 | 15uH | `Inductor_SMD:L_0603_1608Metric` | MGFL1608F150MT-LF | C486329 | microgate |
| 1 | L13 | 47nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN47NG00D | C22334 | muRata |
| 2 | L14,L15 | 2.7nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN2N7C00D | C98058 | muRata |
| 1 | L16 | 8.2nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN8N2G00D | C84404 | muRata |
| 1 | L17 | 10nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN10NG00D | C90642 | muRata |
| 1 | L18 | 22nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN22NG00D | C86129 | muRata |
| 1 | L19 | 4.7nH | `Inductor_SMD:L_0402_1005Metric` | LQW15AN4N7B00D | C98064 | muRata |
| 3 | Q1-Q3 | AO3401A | `Package_TO_SOT_SMD:SOT-23` | AO3401A | C15127 | AOS |
| 4 | R3,R4,R8,R10 | 6.8M | `Resistor_SMD:R_0402_1005Metric` | RC0402FR-076M8L | C477777 | YAGEO |
| 1 | R7 | 1M | `Resistor_SMD:R_0402_1005Metric` | 0402WGF1004TCE | C26083 | UNI-ROYAL |
| 3 | R9,R17,R18 | 10k | `Resistor_SMD:R_0402_1005Metric` | RC0402FR-0710KL | C60490 | YAGEO |
| 1 | R11 | 3.0M | `Resistor_SMD:R_0402_1005Metric` | 0402WGF3004TCE | C56582 | UNI-ROYAL |
| 2 | R13,R16 | 100k | `Resistor_SMD:R_0402_1005Metric` | 0402WGF1003TCE | C25741 | UNI-ROYAL |
| 1 | R14 | 4.7M | `Resistor_SMD:R_0402_1005Metric` | 0402WGF4704TCE | C474132 | UNI-ROYAL |
| 2 | R15,R19 | 1k | `Resistor_SMD:R_0402_1005Metric` | 0402WGF1001TCE | C11702 | UNI-ROYAL |
| 1 | R20 | 0R | `Resistor_SMD:R_0402_1005Metric` | 0402WGF0000TCE | C17168 | UNI-ROYAL |
| 1 | TH1 | EXT_NTC | `Connector_JST:JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical` | B2B-XH-A(LF)(SN) | C158012 | JST |
| 1 | U1 | BQ25570 | `Package_DFN_QFN:QFN-20-1EP_3.5x3.5mm_P0.5mm_EP2x2mm` | BQ25570RGRR | C506250 | TI |
| 1 | U2 | TPS61099 | `Package_SON:WSON-6-1EP_2x2mm_P0.65mm_EP1x1.6mm` | TPS61099DRVR | C2842395 | TI |
| 1 | U3 | nRF52840 | `Package_DFN_QFN:Nordic_AQFN-73-1EP_7x7mm_P0.5mm` | NRF52840-QIAA-R | C190794 | NORDIC |
| 1 | U4 | SX1262 | `Package_DFN_QFN:QFN-24-1EP_4x4mm_P0.5mm_EP2.6x2.6mm` | SX1262IMLTRT | C191341 | SEMTECH |
| 1 | U5 | BME280 | `Package_LGA:Bosch_LGA-8_2.5x2.5mm_P0.65mm_ClockwisePinNumbering` | BME280 | C92489 | Bosch |
| 1 | X1 | 32MHz | `Crystal:Crystal_SMD_2016-4Pin_2.0x1.6mm` | TX201632M4BBCE2T | C5339095 | Yajingxin |
| 1 | X2 | 32.768kHz | `Crystal:Crystal_SMD_3215-2Pin_3.2x1.5mm` | Q13FC13500003 | C99010 | EPSON |
| 1 | X3 | 32MHz | `Crystal:Crystal_SMD_2016-4Pin_2.0x1.6mm` | ECS-320-10-37B-CKY-TR | C2450496 | ECS |
