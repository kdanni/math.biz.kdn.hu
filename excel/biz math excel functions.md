# Biz Math Excel functions

## PV - FV

### Kamatos kamat - FV
- math  
  - `FV = PV ⋅(1+r)^n`
  - FV = 100⋅(1+0,05)^2 = 110,25	
    - 110,25 Ft
  - FV = 100⋅(1+0,05)^5
    - 127,63 Ft
- excel
  - `=FV(r;n;pmt;pv;Type)`
    - Pmt: The payment made each period; it cannot change over the life of the annuity.
    - Pv: The present value, or the lump-sum amount that a series of future payments is worth right now.
    - Type Optional. The number 0 or 1 and indicates when payments are due.
      - `0 or omitted`: At the end of the period
      - `1`:	At the beginning of the period
  - =FV(0,05;2;;-100;1)
    - 110,25 Ft
  - =FV(0,05;5;;-100;1)
    - 127,63 Ft

### Jelenérték - PV
- math
	- `PV = FV / (1+r)^n`
  - PV = 100 / (1+0,05)^2 = 90,703	
    - 90,70 Ft
  - PV = 100 / (1+0,05)^5
    - 78,35 Ft
- excel
	- `=PV(r;n;pmt;fv;Type)`
    - Pmt: The payment made each period and cannot change over the life of the annuity.
    - Fv: The future value, or a cash balance you want to attain after the last payment is made.
    - Type Optional. The number 0 or 1 and indicates when payments are due.
      - `0 or omitted`: At the end of the period
      - `1`:	At the beginning of the period
  - =PV(0,05;2;;-100;1)
    - 90,70 Ft
  - =PV(0,05;5;;-100;1)
    - 78,35 Ft


### Nettó jelenérték és IRR

- `'=NPV(rate;valu1;value2;...)`
  - `=NPV(0,06;100;100;100;600)`
- `'=IRR(array;[guess])`
  - `=IRR({-742\100\100\100\600})`


- horizontal array (hun local)
  - `={-742\100\100\100\600}`
- vertical array (hun local)
  - `={1;2;3;4;5}`
