# Получение сведений о системе
Поспелова Ульяна БИСО-03-20

# Системы аутентификации и защиты от несанкционированного доступа

## Лабораторная работа №1

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  ОС Windows 10
2.  WSL2
3.  Ноутбук ASUS

## План

1.  Выполнить команду uname -r
2.  Выполнить команду cat /proc/cpuinfo | grep “model name”
3.  Выполнить команду journalctl -q -b | tail -n 30

## Ход работы

1\. Первым шагом выполним команду uname -r для вывода информации о
системе.

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

2\. Далее выполним команду cat /proc/cpuinfo | grep “model name” для
вывода информации о процессоре, строки которой содержат “model name”.

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name  : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name  : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name  : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz

3\. Позже выполним команду dmesg | tail -n 30 для вывода последних 30
строк логов.

``` bash
dmesg | tail -n 30
```

    [    6.059321] pci d4cc:00:00.0: [1af4:1049] type 00 class 0x010000
    [    6.063733] pci d4cc:00:00.0: reg 0x10: [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    6.067303] pci d4cc:00:00.0: reg 0x18: [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    6.071879] pci d4cc:00:00.0: reg 0x20: [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    6.083021] pci_bus d4cc:00: busn_res: [bus 00-ff] end is updated to 00
    [    6.085337] pci d4cc:00:00.0: BAR 0: assigned [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    6.088762] pci d4cc:00:00.0: BAR 2: assigned [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    6.091644] pci d4cc:00:00.0: BAR 4: assigned [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    6.831117] hv_pci 774a89a4-d0de-42d3-bfe3-742f619bba2a: PCI VMBus probing: Using version 0x10003
    [    6.844541] hv_pci 774a89a4-d0de-42d3-bfe3-742f619bba2a: PCI host bridge to bus d0de:00
    [    6.847500] pci_bus d0de:00: root bus resource [mem 0x9ffe0c000-0x9ffe0efff window]
    [    6.850329] pci_bus d0de:00: No busn resource found for root bus, will use [bus 00-ff]
    [    6.861507] pci d0de:00:00.0: [1af4:1049] type 00 class 0x010000
    [    6.875248] pci d0de:00:00.0: reg 0x10: [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    6.884060] pci d0de:00:00.0: reg 0x18: [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    6.891005] pci d0de:00:00.0: reg 0x20: [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    6.916220] pci_bus d0de:00: busn_res: [bus 00-ff] end is updated to 00
    [    6.919496] pci d0de:00:00.0: BAR 0: assigned [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    6.925655] pci d0de:00:00.0: BAR 2: assigned [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    6.931772] pci d0de:00:00.0: BAR 4: assigned [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    8.158162] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.159387] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.161002] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.162912] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.166837] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
    [    8.169665] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.171845] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.173221] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.175050] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    8.176632] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2

## Оценка результата

В результате лабораторной работы №1 мы получили основную информацию об
ОС и процессоре и логи системы.

## Вывод

Таким образом, мы научились работать с базовыми командами Linux и
получать информацию об операционной системе.
