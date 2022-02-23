## ESPHome - electric smoke house and smokebox


# Description:

This is a tutorial on automating a smokehouse with a smoke generator.

Features:

- PID thermal regulation

- measurement of smoke, smokehouse and internal meat temperature

- auto fan/fire speed control

- auto vibrator (improve wood chip burning)

- WIFI/cloud control (via Home Assistant server)

- wattmeter

- LCD display

- manual control buttons

- fuel: wood chips

# Required knowledge:

- Home Assistant: [YTB](https://www.youtube.com/watch?v=u_aKcf_F1MM) 

- ESPHome:        [YTB](https://www.youtube.com/watch?v=mj-24SZLQKk) 

- Soldering:      [YTB](https://www.youtube.com/watch?v=6rmErwU5E-k) 

# Used components:

ESP12F 4CH 1pcs: [ALI](https://www.aliexpress.com/item/1005001651180110.html?spm=a2g0o.productlist.0.0.3753351fOHL2kh&algo_pvid=da105da4-7014-4b55-bb39-96ff547ae06c&algo_exp_id=da105da4-7014-4b55-bb39-96ff547ae06c-13&pdp_ext_f=%7B%22sku_id%22%3A%2212000017011631427%22%7D&pdp_pi=-1%3B167.83%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

MCP23017 1pcs: [ALI](https://www.aliexpress.com/item/1005003141912496.html?spm=a2g0o.productlist.0.0.1ed148dasW0v52&algo_pvid=2d82d3bc-dff2-4938-b175-366b837c4bcd&algo_exp_id=2d82d3bc-dff2-4938-b175-366b837c4bcd-30&pdp_ext_f=%7B%22sku_id%22%3A%2212000024317936226%22%7D&pdp_pi=-1%3B79.81%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

SSR DIN 25A 1pcs: [ALI](faaf-47be-8fb2-69755da82c57-0&pdp_ext_f=%7B%22sku_id%22%3A%2212000027001195887%22%7D&pdp_pi=-1%3B297.08%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

PWM driver 2pcs: [ALI](https://www.aliexpress.com/item/1005001902539055.html?spm=a2g0o.productlist.0.0.55aa25c2GnqXDh&algo_pvid=16b38bb6-1d2d-4fd0-b4b6-a7989aac81fe&algo_exp_id=16b38bb6-1d2d-4fd0-b4b6-a7989aac81fe-45&pdp_ext_f=%7B%22sku_id%22%3A%2212000018072058627%22%7D&pdp_pi=-1%3B24.39%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

Buttons 9pcs: [ALI](https://www.aliexpress.com/item/32850618919.html?spm=a2g0o.productlist.0.0.5d872a47Yax7qv&algo_pvid=6443c32b-9e2f-425b-8ad9-328703a715bd&algo_exp_id=6443c32b-9e2f-425b-8ad9-328703a715bd-42&pdp_ext_f=%7B%22sku_id%22%3A%2265177915549%22%7D&pdp_pi=-1%3B37.69%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

LCD 20x4 5V 1pcs: [ALI](https://www.aliexpress.com/item/4001135515638.html?spm=a2g0o.productlist.0.0.70094d0fWGY9Jz&algo_pvid=392c7a21-9633-491f-82bb-b0336551b1ff&algo_exp_id=392c7a21-9633-491f-82bb-b0336551b1ff-2&pdp_ext_f=%7B%22sku_id%22%3A%2210000014747778203%22%7D&pdp_pi=-1%3B89.57%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

AC-DC 12V 3.3A MD-40-12 DIN 1pcs: [ALI](https://www.aliexpress.com/item/1005002024975538.html?spm=a2g0o.productlist.0.0.5b66639bc7g2C6&algo_pvid=29039fdf-9abb-480c-a1ec-fdcd6659b322&aem_p4p_detail=2022022304181914498879841991630001808887&algo_exp_id=29039fdf-9abb-480c-a1ec-fdcd6659b322-0&pdp_ext_f=%7B%22sku_id%22%3A%2212000018453302440%22%7D&pdp_pi=-1%3B380.44%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

Switch AC 250V 16A 2pcs: [ALI](https://www.aliexpress.com/item/32806585772.html?spm=a2g0o.productlist.0.0.4c533cadEbQ4TY&algo_pvid=42fad9ed-7d3e-41f7-be61-bb7bcfac7a62&algo_exp_id=42fad9ed-7d3e-41f7-be61-bb7bcfac7a62-35&pdp_ext_f=%7B%22sku_id%22%3A%2264444197255%22%7D&pdp_pi=-1%3B27.27%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

Dallas temp. Sensor 4pcs: [ALI](https://www.aliexpress.com/item/32839776524.html) 

FAN 5025 12V 6200rpm 1pcs: [ALI](https://www.aliexpress.com/item/33049767300.html?spm=a2g0o.order_list.0.0.21ef1802FV0N98) 

Vibrator DC 1.5-6V 22400RPM 1pcs: [ALI](https://www.aliexpress.com/item/1005003309418737.html?spm=a2g0o.order_list.0.0.21ef1802FV0N98) 

Wattmeter PZEM-004T 100A 1pcs: [ALI](https://www.aliexpress.com/item/33043137964.html?spm=a2g0o.productlist.0.0.39996e27jijA6Q&algo_pvid=1952f64e-d59d-4ee7-b973-b8eb7d3aefad&algo_exp_id=1952f64e-d59d-4ee7-b973-b8eb7d3aefad-39&pdp_ext_f=%7B%22sku_id%22%3A%2267438540147%22%7D&pdp_pi=-1%3B318.14%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

Heater 2600W 230V 1pcs: [ALI](https://www.aliexpress.com/item/1005003584466174.html?spm=a2g0o.detail.1000014.9.6a92713dVDrXSB&gps-id=pcDetailBottomMoreOtherSeller&scm=1007.13338.177756.0&scm_id=1007.13338.177756.0&scm-url=1007.13338.177756.0&pvid=0e2cb83b-8521-45df-9570-7829ea86d0f4&_t=gps-id:pcDetailBottomMoreOtherSeller,scm-url:1007.13338.177756.0,pvid:0e2cb83b-8521-45df-9570-7829ea86d0f4,tpp_buckets:668%232846%238108%231977&pdp_ext_f=%257B%2522sku_id%2522%253A%252212000027300025510%2522%252C%2522sceneId%2522%253A%252230050%2522%257D&pdp_pi=-1%253B603.47%253B-1%253B-1%2540salePrice%253BCZK%253Brecommend-recommend) 

LED diode set 1pcs: [ALI](https://www.aliexpress.com/item/1005003323707856.html?dp=61e453ee0fa2025c4ba43400&cn=ah&aff_fcid=bd9ed3937ddf4288850b01c823d9a1d7-1645625483275-03644-_d6jWDbY&aff_fsk=_d6jWDbY&aff_platform=link-c-tool&sk=_d6jWDbY&aff_trace_key=bd9ed3937ddf4288850b01c823d9a1d7-1645625483275-03644-_d6jWDbY&terminal_id=f09dc59f89d1480fb0cfa10490f657c7&afSmartRedirect=n) 

Resistors set 1pcs: [ALI](https://www.aliexpress.com/item/1005002631550177.html?spm=a2g0o.productlist.0.0.1ed36405DfJzoB&algo_pvid=91b60b6b-d8f3-4351-9d1b-b23bf0ba2b69&aem_p4p_detail=202202230706528513372260889730002489868&algo_exp_id=91b60b6b-d8f3-4351-9d1b-b23bf0ba2b69-0&pdp_ext_f=%7B%22sku_id%22%3A%2212000021480015802%22%7D&pdp_pi=-1%3B64.29%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

LED light outdoor 20W 230V 1pcs: [ALI](https://www.aliexpress.com/item/4001183488400.html?spm=a2g0o.productlist.0.0.630446b6KVFPmV&algo_pvid=2f0e5a2a-f81a-4789-89be-66a6cdb0ea9a&algo_exp_id=2f0e5a2a-f81a-4789-89be-66a6cdb0ea9a-50&pdp_ext_f=%7B%22sku_id%22%3A%2212000027495977514%22%7D&pdp_pi=-1%3B264.27%3B-1%3B-1%40salePrice%3BCZK%3Bsearch-mainSearch) 

Oven light 25W 230V 1pcs: [ALI](https://www.aliexpress.com/item/1005001265388691.html?spm=a2g0o.productlist.0.0.66ad92e8N4pHp6&algo_pvid=4f47a72a-3b68-4385-8d38-53bfc0c93ff2&algo_exp_id=4f47a72a-3b68-4385-8d38-53bfc0c93ff2-2&pdp_ext_f=%7B%22sku_id%22%3A%2212000015518228734%22%7D&pdp_pi=-1%3B17.74%3B-1%3B1751%40salePrice%3BCZK%3Bsearch-mainSearch) 

Oven E14 holder/socket 1pcs: [ALI](https://www.aliexpress.com/item/1005002315411008.html?spm=a2g0o.productlist.0.0.13b1360dM2UuIt&algo_pvid=8430a2c1-8756-48be-ad43-43a0ccd8533b&algo_exp_id=8430a2c1-8756-48be-ad43-43a0ccd8533b-10&pdp_ext_f=%7B%22sku_id%22%3A%2212000020046504898%22%7D&pdp_pi=-1%3B37.47%3B-1%3B3370%40salePrice%3BCZK%3Bsearch-mainSearch) 


# Schema:

![Schematic](https://github.com/peca2345/ESPHome-udirna/blob/main/test.png?raw=true)

# Gallery

https://photos.app.goo.gl/iQ432f7vACJFKvrUA

# 3D print model:


# ESPHome code
```
esphome:
  name: iudirna
  platform: esp8266
  board: esp12e
  on_boot:
    then:
      - switch.turn_off: fan_auto
      - switch.turn_off: vibrator_auto
      - delay: 5s
      - climate.control:
          id: pid_climate
          mode: 'OFF'
          
logger:
  level: NONE # musi byt vypnuty aby se uvolnil uart pro wattmeter
  hardware_uart: UART1
  
api:
ota:
  password: "a025f35ef14fd7ed30fba26567e45e60"
  
wifi:
  networks:
  - ssid: !secret wifi_ssid
    password: !secret wifi_password 
  manual_ip:
    static_ip: 192.168.1.181
    gateway: 192.168.1.1
    subnet: 255.255.255.0  
    dns1: 192.168.1.1
    dns2: 1.1.1.1
    
###############################################################
###### PINOUT #################################################

# GPIO0   nepouzivat (slouzi pro boot)
# GPIO2   nepouzivat (slouzi pro boot)  
# GPIO9   nepouzivat (pamet)
# GPIO10  nepouzivat (pamet)
# GPIO15  nepouzivat (slouzi pro boot)


# ADC     FREE - analogovy vstup
# GPIO4   i2c sda (mcp23017, lcd)
# GPIO5   i2c scl (mcp23017, lcd)

# GPIO12  dallas                         
# GPIO13  PWM controller fan_output (nejde pres expander)           
# GPIO14  PWM controller vibrator_output (nejde pres expander)    
# GPIO16  SSR rele id: heater (nejde pres expander)                 

#multiplexer MCP23017:
## pin A0-A3 cesta pod deskou pres odpor a zvlast dupont vystup vpravo nahore
#mcp23xxx  pin0   A0  OUT  LED iudirna_led0_termostat             
#mcp23xxx  pin1   A1  OUT  LED iudirna_led2_venkovni_svetlo         
#mcp23xxx  pin2   A2  OUT  LED iudirna_led1_vnitrni_svetlo          
#mcp23xxx  pin3   A3  OUT  LED iudirna_led3_wifi_status          
#mcp23xxx  pin4   A4  OUT  FREE
#mcp23xxx  pin5   A5  IN   BTN iudirna_button5_termostat                                     
#mcp23xxx  pin6   A6  OUT  RELE iudirna_svetlo_in                 
#mcp23xxx  pin7   A7  OUT  RELE iudirna_svetlo_out                

#mcp23xxx  pin8   B0  IN   iudirna_button9_svetlo_venkovni
#mcp23xxx  pin9   B1  IN   iudirna_button8_svetlo_vnitrni    
#mcp23xxx  pin10  B2  IN   iudirna_button10_set_temp_up
#mcp23xxx  pin11  B3  IN   iudirna_button11_set_temp_down
#mcp23xxx  pin12  B4  IN   iudirna_button12_set_fan_up             
#mcp23xxx  pin13  B5  IN   iudirna_button13_set_fan_down           
#mcp23xxx  pin14  B6  IN   iudirna_button14_fan_auto            
#mcp23xxx  pin15  B7  IN   iudirna_button15_vibrator_auto       

###############################################################
###### FUNKCE #################################################

# PREDNI STRANA:
# tlacitko1   +               kratke: +1°C termostat   /   dlouhe: +1 rychlost FANu
# tlacitko2   -               kratke: -1°C termostat   /   dlouhe: -1 rychlost FANu
# tlacitko3   spirala         manualni ovladani spiraly (nejde ovladat pres WIFI)
# tlacitko4   AUTO FAN        kratke: zapne automatickou regulaci FANu
# tlacitko5   AUTO VIBRATOR   kratke: zapne automatickou regulaci vibratoru  
# tlacitko6   svetlo IN       kratke: zapne svetlo uvnitr
# tlacitko7   svetlo OUT      kratke: zapne svetlo venku

# ZADNI STRANA:
# tlacitko1   VIB. MAN        kratke: manualni zap/vyp vibratoru na 5s
# tlacitko2   TIME            kratke: reset doby uzeni

###########################################################

########################################################### 
    
uart: # pro wattmeter pzem004t (musi byt vypnuty logger aby se uvolnil uart)
  rx_pin: GPIO3
  tx_pin: GPIO1
  baud_rate: 9600
  
i2c: # pro dallas, lcd, mcp23017
  sda: GPIO4
  scl: GPIO5
  scan: false # pokud neznas adresy i2c zarizeni tak povol scan (true) a z logu vycti ID 
  
mcp23017:
  - id: 'mcp23017_hub'
    address: 0x20 # zjisteno z logu s povolenym scanem i2c

dallas: 
  - pin: GPIO12
    update_interval: 5s
    
###########################################################

########################################################### LCD DISPLEJ

display: #////////////////////////////////////////////////////////////////////  DISPLAY
  - platform: lcd_pcf8574 #display
    dimensions: 20x4
    address: 0x27
    lambda: |-
      it.printf(0, 0, "Udirna: %.0f", id(iudirna_teplota1).state);
      it.printf(12, 0, "T=%.0f", id(pid_climate).target_temperature_low);
      it.printf(17, 0, "%s", id(pid_mode).state ? "ON" : "OFF");
      it.printf(0, 1, "Maso 1: %.0f", id(iudirna_teplota2).state);
      it.printf(11, 1, " F=%.0f", id(fan_speed).state);
      it.printf(17, 1, "%s", id(fan_auto).state ? "AUT" : "MAN");
      it.printf(0, 2, "Maso 2: %.0f", id(iudirna_teplota3).state);
      it.printf(11, 2, " V=%.0f", id(vibrator_speed).state);
      it.printf(17, 2, "%s", id(vibrator_auto).state ? "AUT" : "MAN"); 
      it.printf(0, 3, "Dymbox: %.0f", id(iudirna_teplota4).state);
      it.printf(11, 3, " H=%.0f", id(iudirna_up_time).state); 

###########################################################

########################################################### TERMOSTAT PID

climate: #////////////////////////////////////////////////////////////////////  CLIMATE

  # PID TERMOSTAT
  - platform: pid # climate
    id: pid_climate
    name: "iUdirna PID Climate Controller"
    sensor: iudirna_teplota1
    default_target_temperature: 65°C
    visual:
      min_temperature: 0
      max_temperature: 99
      temperature_step: 1
    heat_output: heater
    control_parameters:
      kp: 0.22224  
      ki: 0.00067  
      kd: 18.41252 
      # pro funkcni autotune nastav kp,ki,kd: 0 
      # po dokonceni autotune prepis hodnotama z logu
      
###########################################################
sensor: #////////////////////////////////////////////////////////////////////// SENSOR
########################################################### WATTMETER

  # WATTMETER PZEM004T   
  - platform: pzemac
    update_interval: 10s
    current:
      name: "iudirna_pzem_proud"
    voltage:
      name: "iudirna_pzem_napeti"
    energy:
      name: "iudirna_pzem_spotreba"
    power:
      name: "iudirna_pzem_prikon"
      id: pzem_energy
    frequency:
      name: "iudirna_pzem_frekvence"
    power_factor:
      name: "iudirna_pzem_ucinik"

###########################################################

########################################################### PID AUTOTUNE

  # PID HEAT SENSOR (PRO GRAFANU)
  - platform: pid #sensor 
    name: "iUdirna PID Climate HEAT"
    type: HEAT
# PID SENZORY NIZE POVOLIT JEN PRI AUTOTUNE #
#  - platform: pid #sensor
#    name: "iUdirna PID Climate Result"
#    type: RESULT
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate PROPORTIONAL"
#    type: PROPORTIONAL 
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate INTEGRAL"
#    type: INTEGRAL
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate DERIVATIVE"
#    type: DERIVATIVE
#    climate_id: pid_climate
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate COOL"
#    type: COOL
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate KP"
#    type: KP
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate KI"
#    type: KI
#    climate_id: pid_climate
#  - platform: pid #sensor
#    name: "iUdirna PID Climate KD"
#    type: KD
#    climate_id: pid_climate
# PID SENZORY VYSE POVOLIT JEN PRI AUTOTUNE #

###########################################################

########################################################### TEPLOMERY

  # UDIRNA
  - platform: dallas #sensor 
    name: "iudirna_dallas_teplota1"
    address: 0xC106219415E16428 
    id: iudirna_teplota1
    unit_of_measurement: "°C"  
    ## adresa zjistena z logu s povolenym scanem i2c
    
  # MASO1
  - platform: dallas #sensor
    name: "iudirna_dallas_teplota2"
    address: 0xBE06219419160728 
    id: iudirna_teplota2
    unit_of_measurement: "°C" 
    ## adresa zjistena z logu s povolenym scanem i2c
    
  # MASO2
  - platform: dallas #sensor
    name: "iudirna_dallas_teplota3"
    address: 0xB101215744DA0B28 
    id: iudirna_teplota3
    unit_of_measurement: "°C"  
    ## adresa zjistena z logu s povolenym scanem i2c
    
  # DYMBOX
  - platform: dallas #sensor
    name: "iudirna_dallas_teplota4"
    address: 0xB9012157542A0228 
    id: iudirna_teplota4
    unit_of_measurement: "°C"  
    ## adresa zjistena z logu s povolenym scanem i2c
    
    # on_value_range:
    #   above: 14 # pri prekroceni dane teploty se spusti automatizace pro vibrator
    #   then:
    #     - switch.turn_on: vibrator_wait_temp # povoli dalsi podminku pro auto vibrator
    
###########################################################

########################################################### UPTIME SENSOR

  # UPTIME - doba uzeni
  - platform: uptime #sensor
    id: iudirna_up_time
    name: "iudirna_up_time2"
    update_interval: 60s
    filters:
      - lambda: return x / 3600;
    unit_of_measurement: "h"
    
###########################################################

########################################################### FAN + VIB + PID SENSOR

  # PID MODE LAMBDA PRO ZOBRAZENI NA LCD (ziska stav termostatu - heat/off)
  - platform: template #sensor
    id: "pid_mode"
    name: iudirna_pid_mode
    update_interval: 1s
    accuracy_decimals: 0
    lambda: |-
      return id(pid_climate).mode;
      
  # FAN SPEED LAMBDA PRO ZOBRAZENI NA LCD (ziska stupen rychlosti)
  - platform: template #sensor
    id: "fan_speed"
    name: iudirna_fan_speed
    update_interval: 1s
    accuracy_decimals: 0
    lambda: |-
      return id(fan_pwm).speed;
      
  # FAN SPEED LAMBDA PRO ZOBRAZENI NA LCD (ziska stupen rychlosti)
  - platform: template #sensor
    id: "vibrator_speed"
    name: "iudirna_vibrator_speed"
    update_interval: 1s
    accuracy_decimals: 0
    lambda: |-
      return id(vibrator_pwm).speed;
      
###########################################################

########################################################### WIFI SIGNAL  

  # WIFI SIGNAL SENSOR
  - platform: wifi_signal #sensor
    name: "iudirna_signal_wifi2"
    update_interval: 10s     
    
interval: #//////////////////////////////////////////////////////////////////// INTERVAL

  # WIFI SIGNAL - KONTROLA SPOJENI A OVLADANI LED KONTROLKY
  - interval: 1s
    then:
      if:
        condition:
          wifi.connected:
        then:
          - switch.turn_on: iudirna_led3_wifi_status
        else:
          - switch.turn_off: iudirna_led3_wifi_status
          
###########################################################

########################################################### TERMOSTAT - LED

  # LED KONTOLKA TERMOSTATU
  - interval: 100ms
    then:
      if:
        condition: 
          - sensor.in_range:
              id: pid_mode
              above: 1
              below: 5
        then:
          - switch.turn_on: iudirna_led0_termostat
        else:
          - switch.turn_off: iudirna_led0_termostat
          
########################################################### 

########################################################### FAN AUTO 

  # FAN AUTO - zmen teploty a rychlosti dle libosti
  - interval: 10min
    id: interval_fan_auto
    then:
      if:
        condition:
          and:
            - switch.is_on: fan_auto
            - sensor.in_range:
                 id: iudirna_teplota4
                 above: -20 # vyse
                 below: 30  # nize
        then:
          - fan.turn_on:
              id: fan_pwm
              speed: !lambda return (id(fan_pwm).speed = 7.0); # rychlost
        else:               
          if:
            condition:
              and:
                - switch.is_on: fan_auto
                - sensor.in_range:
                     id: iudirna_teplota4
                     above: 30 # vyse
                     below: 50 # nize
            then:
              - fan.turn_on:
                  id: fan_pwm
                  speed: !lambda return (id(fan_pwm).speed = 5.0); # rychlost           
            else:
              if:
                condition:
                  and:
                    - switch.is_on: fan_auto
                    - sensor.in_range:
                        id: iudirna_teplota4
                        above: 55 # vyse
                        below: 80 # nize
                then:
                  - fan.turn_on:
                      id: fan_pwm
                      speed: !lambda return (id(fan_pwm).speed = 3.0); # rychlost   
                      
###########################################################

########################################################### VIBRATOR AUTO

  # VIBRATOR AUTO                    
  - interval: 10min
    id: interval_vibrator_auto
    then:
      if:
        condition:
          and:
            - switch.is_on: vibrator_auto # podminka ktera se spusti manualne tlacitkem
            - sensor.in_range:
                id: iudirna_teplota4
                above: 0  # vyse
                below: 30 # nize
        then:
          - fan.turn_on:
              id: vibrator_pwm
              speed: !lambda return (id(vibrator_pwm).speed = 10.0);  # spusti vibrator na max
          - delay: 3s # ceka 3s
          - fan.turn_on:
              id: vibrator_pwm
              speed: !lambda return (id(vibrator_pwm).speed = 1.0); # snizi rychlost (1=OFF)
          - fan.turn_off: # vypne vibrator
              id: vibrator_pwm
        else:
          if:
            condition:
              and:
                - switch.is_on: vibrator_wait_temp # podminka ktera se povoli az po dosazeni teploty od startu
                - sensor.in_range:
                    id: iudirna_teplota4
                    above: 0  # vyse
                    below: 30 # nize
            then:
              - fan.turn_on:
                  id: vibrator_pwm
                  speed: !lambda return (id(vibrator_pwm).speed = 10.0); # spusti vibrator na max
              - delay: 3s # ceka 3s
              - fan.turn_on:
                  id: vibrator_pwm
                  speed: !lambda return (id(vibrator_pwm).speed = 1.0); # snizi rychlost (1=OFF)
              - fan.turn_off: # vypne vibrator
                  id: vibrator_pwm 
                  
binary_sensor: #//////////////////////////////////////////////////////////////// BINARY_SENSOR                  
                  
###########################################################

########################################################### TLACITKA

  # TLACITKO TERMOSTAT 
  - platform: gpio #binary_sensor
    id: "iudirna_button5_termostat"
    pin:
      mcp23xxx: mcp23017_hub
      number: 5
      mode:
        input: true
        pullup: true
      inverted: true
    filters:
        - delayed_on: 20ms
    on_press:
      - switch.toggle: pid_switch
              
  # TLACITKO SVETLO VNITRNI 
  - platform: gpio #binary_sensor
    id: "iudirna_button8_svetlo_vnitrni"
    pin:
      mcp23xxx: mcp23017_hub
      number: 9
      mode:
        input: true
        pullup: true
      inverted: true
    filters:
        - delayed_on: 20ms
    on_press:
    - switch.toggle: iudirna_svetlo_in
    
  # TLACITKO SVETLO VENKOVNI    
  - platform: gpio #binary_sensor 
    id: "iudirna_button9_svetlo_venkovni"
    pin:
      mcp23xxx: mcp23017_hub
      number: 8 
      mode:
        input: true
        pullup: true
      inverted: true
    filters:
        - delayed_on: 20ms
    on_press:
    - switch.toggle: iudirna_svetlo_out
    
  # TLACITKO TERMOSTAT CILOVA TEPLOTA +1°C   
  - platform: gpio #binary_sensor
    id: "iudirna_button10_set_temp_up"
    pin:
      mcp23xxx: mcp23017_hub
      number: 10
      mode:
        input: true
        pullup: true
      inverted: true
    on_click:
    - min_length: 20ms
      max_length: 500ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature + 1.0);
    - min_length: 500ms
      max_length: 2000ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature + 5.0);    
    - min_length: 2000ms
      max_length: 6000ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature = 65.0);   
            
  # TLACITKO TERMOSTAT CILOVA TEPLOTA -1°C
  - platform: gpio #binary_sensor
    id: "iudirna_button11_set_temp_down"
    pin:
      mcp23xxx: mcp23017_hub
      number: 11
      mode:
        input: true
        pullup: true
      inverted: true
    on_click:
    - min_length: 20ms
      max_length: 500ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature - 1.0);
    - min_length: 500ms
      max_length: 2000ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature - 5.0);
    - min_length: 2000ms
      max_length: 6000ms
      then:
        - climate.control:
            id: pid_climate
#            mode: 'HEAT'
            target_temperature: !lambda return (id(pid_climate).target_temperature = 0.0);
            
  # TLACITKO FAN SPEED +1
  - platform: gpio #binary_sensor
    id: iudirna_button12_set_fan_up
    pin:
      mcp23xxx: mcp23017_hub
      number: 12
      mode:
        input: true
        pullup: true
      inverted: true
    on_click:
    - min_length: 20ms
      max_length: 500ms
      then:
        - fan.turn_on:
            id: fan_pwm
            speed: !lambda return (id(fan_pwm).speed + 1.0);
    - min_length: 500ms
      max_length: 3s
      then:
        - fan.turn_on:
            id: fan_pwm
            speed: !lambda return (id(fan_pwm).speed = 10.0);
            
  # TLACITKO FAN SPEED -1
  - platform: gpio #binary_sensor
    id: iudirna_button13_set_fan_down
    pin:
      mcp23xxx: mcp23017_hub
      number: 13
      mode:
        input: true
        pullup: true
      inverted: true
    on_click:
    - min_length: 20ms
      max_length: 500ms
      then:
      - if:
          condition:
            or:
              - lambda: 'return id(fan_pwm).speed == 1.0;'
              - lambda: 'return id(fan_pwm).speed == 2.0;'
          then:
            - fan.turn_on:
                id: fan_pwm
                speed: !lambda return (id(fan_pwm).speed - 1.0);
            - fan.turn_off:
                id: fan_pwm
          else:
            - fan.turn_on:
                id: fan_pwm
                speed: !lambda return (id(fan_pwm).speed - 1.0);  
    - min_length: 500ms
      max_length: 3s
      then:
        - fan.turn_on:
            id: fan_pwm
            speed: !lambda return (id(fan_pwm).speed = 1.0);
        - fan.turn_off:
            id: fan_pwm
            
  # TLACITKO FAN AUTO 
  - platform: gpio #binary_sensor
    id: iudirna_button14_fan_auto
    pin:
      mcp23xxx: mcp23017_hub
      number: 14 # B6
      mode:
        input: true
        pullup: true
      inverted: true
    filters:
        - delayed_on: 20ms
    on_press:
      then:
        - switch.toggle: fan_auto
        
  # TLACITKO VIBRATOR AUTO 
  - platform: gpio #binary_sensor
    id: iudirna_button15_vibrator_auto
    pin:
      mcp23xxx: mcp23017_hub
      number: 15 # B7
      mode:
        input: true
        pullup: true
      inverted: true
    on_click:
    - min_length: 20ms
      max_length: 500ms
      then:
        - switch.toggle: vibrator_auto
    - min_length: 500ms
      max_length: 5s
      then:
        - fan.turn_on:
            id: vibrator_pwm
            speed: !lambda return (id(vibrator_pwm).speed = 10.0);
        - delay: 3s
        - fan.turn_on:
            id: vibrator_pwm
            speed: !lambda return (id(vibrator_pwm).speed = 1.0);
        - fan.turn_off:
            id: vibrator_pwm
            
########################################################### 
fan: #////////////////////////////////////////////////////////////////////////// FAN
########################################################### FAN PWM OUTPUT

  # FAN PWM SPEED
  - platform: speed #fan
    output: fan_output
    id: fan_pwm
    name: "iudirna_fan_pwm_switch"
    speed_count: 10
    restore_mode: ALWAYS_OFF
    
  # VIBRATOR PWM SPEED
  - platform: speed
    output: vibrator_output
    id: vibrator_pwm
    name: "iudirna_vibrator_pwm_switch"
    speed_count: 10
    restore_mode: ALWAYS_OFF
    
output: #/////////////////////////////////////////////////////////////////////// OUTPUT 

  # FAN PWM OUTPUT
  - platform: esp8266_pwm #output
    pin: GPIO13
    frequency: 80 Hz # 12V FAN 5015
    id: fan_output
    min_power: 0
    max_power: 0.7


    
  # VIBRATOR PWM OUTPUT
  - platform: esp8266_pwm
    pin: GPIO14
    frequency: 600 Hz # 1.5-6V vibrator
    id: vibrator_output
    max_power: 0.5 # 1=12V 0.5=6V
    
########################################################### 

########################################################### PID AUTOTUNE

  # PID - PWM output     
  - platform: slow_pwm #output
    pin: GPIO16
    id: heater
    period: 30s
    
switch: #/////////////////////////////////////////////////////////////////////// SWITCH  

  # PID - autotune    
  - platform: template #switch
    name: "iUdirna PID Climate Autotune"
    turn_on_action:
      - climate.pid.autotune: pid_climate
      
########################################################### 

########################################################### RELE

  # FAN AUTO - povoluje podminku intervalu automaticke regulace
  - platform: template
    name: "iudirna_fan_auto"
    id: fan_auto
    optimistic: true
    
  # VIBRATOR AUTO - povoluje podminku intervalu automaticke regulace tlacitkem
  - platform: template
    name: "iudirna_vibrator_auto"
    id: vibrator_auto
    optimistic: true
    turn_off_action: 
      - switch.turn_off: vibrator_wait_temp # pri manualnim vypnuti tlacitkem vypne i podminku wait_temp
      - fan.turn_on: # nastavi rychlost na minimum (1= vypnuto)
          id: vibrator_pwm
          speed: !lambda return (id(vibrator_pwm).speed = 1.0);
      - fan.turn_off: # a vypne vibrator
          id: vibrator_pwm 
          
  # VIBRATOR AUTO WAIT FOR TEMP               # podminka intervalu automaticke regulace 
  - platform: template                      # az po dosazeni dane teploty od startu ho zapne teplomer
    name: "iudirna_vibrator_wait_temp"      # tim se zajisti ze nebude vibrovat od zacatku pri roztapeni ale az po dosazeni urcene teploty
    id: vibrator_wait_temp
    optimistic: true
    
  # RELE2 - vnitrni svetlo
  - platform: gpio #switch
    id: iudirna_svetlo_in
    name: "iudirna_rele2_svetlo_vnitrni"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      inverted: false
      number: 6
      mode:
        output: true
        pullup: false
    on_turn_on:
        - switch.turn_on: iudirna_led1_vnitrni_svetlo
    on_turn_off:
        - switch.turn_off: iudirna_led1_vnitrni_svetlo
        
  # RELE3 - venkovni svetlo    
  - platform: gpio #switch
    id: iudirna_svetlo_out
    name: "iudirna_rele3_svetlo_venkovni"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      inverted: false
      number: 7
      mode:
        output: true
        pullup: false
    on_turn_on:
        - switch.turn_on: iudirna_led2_venkovni_svetlo
    on_turn_off:
        - switch.turn_off: iudirna_led2_venkovni_svetlo 
        
########################################################### 

########################################################### LED KONTROLKY

  # LED1 - kontrolka vnitrni svetlo - zluta
  - platform: gpio #switch     
    id: "iudirna_led0_termostat"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      number: 0 # A0
      mode:
        output: true
        pullup: false
      inverted: false 
      
  # LED1 - kontrolka vnitrni svetlo - zluta
  - platform: gpio #switch     
    id: "iudirna_led1_vnitrni_svetlo"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      number: 2 # A2
      mode:
        output: true
        pullup: false
      inverted: false 
      
  # LED2 - kontrolka venkovni svetlo - zluta
  - platform: gpio #switch     
    id: "iudirna_led2_venkovni_svetlo"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      number: 1 # A1
      mode:
        output: true
        pullup: false
      inverted: false 
      
  # LED3 - WIFI status - modra
  - platform: gpio #switch     
    id: "iudirna_led3_wifi_status"
    restore_mode: ALWAYS_OFF
    pin:
      mcp23xxx: mcp23017_hub
      number: 3 # A3
      mode:
        output: true
        pullup: false
      inverted: false 
      
      
      
  - platform: template                   
    id: pid_switch
    turn_on_action:
      if:
        condition:
          - sensor.in_range:
              id: pid_mode # 0=OFF 3=HEAT
              above: 1 # => ON
              below: 5 # => ON
        then:
          - climate.control:
              id: pid_climate
              mode: 'OFF'
        else:
          - climate.control:
              id: pid_climate
              mode: 'HEAT'
      

      
      
```

