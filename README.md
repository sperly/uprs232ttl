# uprs232ttl
TTL Serial Adapter for C64/C128 UserPort.

The adapter is based on a non-inverting cmos buffer chip, CD4050. Following signals are used from the C64/C128:
```
FLAG <- RX (via a jumper)
PB0  <- RX
PB1  -> RTS
PB6  <- CTS
PA2  -> TX
```

There are also jumpers to switch signal path to enable null-modem communication. The default position is marked on pcb and it set for null-modem communication.
```
J4:

 RX/TX
| o o |         Null-Modem
| o o |
  o o

 RX/TX
  o o           Controller-Peripheral
| o o |
| o o |


J5:

CTS/RTS
| o o |         Null-Modem
| o o |
  o o

CTS/RTS
  o o           Controller-Peripheral
| o o |
| o o |

```

The serial output is pin compatible with common serial-usb adapters:
```
1 - GND
2 - CTS
3 - VCC
4 - TX
5 - RX
6 - DTR

```

Jumper 1 is used for enabeling RX interupt on the C64/C128. And jumper 2 is enabeling power thru the serial adapter.
```
J1:

RX Int
| o |         RX interupt enabled
| o |

RX Int
  o           RX interupt disabled
  o 


J2:

 Pwr
| o |         Power feed from C64/C128 enabled
| o |

 Pwr
  o           Power feed from C64/C128 disabled
  o 

```


Top side of pcb:
[[/Doc/uprs232ttl-Top.png|Top view of pcb]]

Bottom side of pcb, also containing info on jumper settings:
[[/Doc/uprs232ttl-bottom.png|Bottom view of pcb]]
