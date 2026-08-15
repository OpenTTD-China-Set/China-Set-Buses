# China Set: Buses -README

1. General Information
2. Building
3. Credits
4. License

## 1. General Information

China Set: Buses is the bus sector of the China set of OpenTTD.
China Set: Buses is licensed under GPL v2.

This set contains buses covering the whole of China (including Hong Kong, Macao and Taiwan Province), 
including urban buses, suburban/regional buses, intercity buses/coaches, long-distance coaches and tourist coaches.

Bus Classification:
- Urban Bus: primarily operates in urban areas with few seats and ample standing room.
- Suburban/Regional Bus: primarily operates in suburban/regional areas with more seats and limited standing room.
- Intercity Bus/Coach: buses or coaches offering passenger services between nearby cities.
- Long-distance Coach: mainly used for long-distance services, with a large number of seats and no standing room provided.
- Tourist Coach: mainly used for high-value services, with luxurious and spacious interior arrangements and no standing room provided.

According to Chinese laws and regulations, buses manufactured in 2013 and later must be equipped with 
an speed limiter. Buses with standing areas are limited to 70 km/h, while buses without standing areas 
are limited to 100 km/h. In practice, some buses may have a maximum speed lower than the legal limit.

According to national standards, Chinese coaches are classified into five grades from low to high based 
on vehicle type and interior configuration: Ordinary Class, Medium Class, High Class I, High Class II, 
and High Class III.

I have filled in data for the cargo_age_period based on the vehicle type, class, and specific configuration.

## 2. Building

The source is available on [GitHub](https://github.com/OpenTTD-China-Set/China-Set-Buses). These tools are required to build the GRF:

- nml
- make
- gcc
- gorender, or renderobject

You would need to render all models first, then you can build the GRF.

> [!NOTE]
> The first build will be slow since all models have to be rendered, which is a slow process.
> You can use `make -j n` to speed up the process by running multiple tasks at once where `n` is the task limit.

Using Linux or WSL:

```bash
#!/bin/bash
# you'll have to install gorender from https://github.com/mattkimber/gorender
# here we use apt for demo

# dependencies
sudo apt install python3
sudo apt install python3-pip
sudo apt install make
pip3 install nml
# we would also need gcc, but that should be already included in most distros

# compiling
make
# alternatively, you could use "make -j n" where n is the total number of parallel tasks you want to run at once.
```

Using Windows (Scoop is advised here, but non-scoop compilations are also possible):

```powershell
# we suggest you to use scoop; you can get scoop @ https://scoop.sh

# dependencies
scoop bucket add main
scoop bucket add openttd https://github.com/WenSimEHRP/OpenTTD-Bucket
scoop install python
scoop install make
scoop install openttd/nml
scoop install openttd/gorender
# we would need the gcc compiler in from mingw
scoop install mingw

# compiling
make
# alternatively, you could use "make -j n" where n is the total number of parallel tasks you want to run at once.
```

## 3. Credits

Contributors (in alphabetical order):

- Ahyangyi
- babel
- EMB190
- GUANGMING
- John Franklin
- taiqiji432292
- WenSim

Thanks to:

- andythenorth
- Belaja Lilija
- dP
- Emperor Jake
- Garlic_Bread42
- KeepinItRail
- peter1138
- planetmaker
- Simo333
- Timberwolf

- CS Bus set team
- Ikarus set team

Special thanks to everyone whom thanks is due;
Patch Pack Developers, especially JGR;
OpenTTD Developers; and Chris Sawyer.

## 4. License

China Set: Buses

Copyright (C) 2023-2026 China Set Team

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License along
with this program; if not, please check
https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html