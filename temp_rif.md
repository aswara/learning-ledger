# Case Study:
* mengendalikan power supply ke mesin mekanik
* mendigitalisasi data mesin mekanik untuk analisa lebih lanjut

## Mesin Mekanik (mesin bubut) 
#### data yang ingin didapatkan:
* power supply (on / off)
* operasi (rpm)
* item yg dikerjakan (rfid tag)


## Device (controller, module: sensor)
#### instalasi komponen tambahan:
* relay (power supply)
* sensor (rpm)

#### komunikasi dengan main controller
* socket client: send data, recv command

## Device (main controller)
#### instalasi komponen tambahan:
* rfid reader
* lampu indikator

#### fungsi
* connect rfid (serial / socket)
* socket server: recv data, send command
* queue data ke api server bila gagal simpan lokal untuk dikirim ulang
* gpio: mengendalikan lampu indikator

## Server
* api untuk simpan data
* dashboard analisa data
