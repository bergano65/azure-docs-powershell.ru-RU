---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248870"
---
# New-AzMigrateNicMapping

## КРАТКИй обзор
Создает объект для обновления свойств сетевого адаптера сервера репликации.

## Максимальное

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет New-AzMigrateNicMapping создает сопоставление исходного сетевого адаптера, подключенного к серверу для миграции.
Этот объект предоставляется в качестве входных данных для командлета Set-AzMigrateServerReplication, чтобы обновить NIC и его свойства для сервера репликации.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта NIC
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

Создание объекта обновления сетевого адаптера.

## ПАРАМЕТРЫ

### -NicID
Указывает ИД сетевого адаптера, который нужно обновить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicIP
Указывает IP-адрес в конечной подсети, который будет использоваться для сетевого адаптера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSelectionType
Указывает, будет ли обновленная сетевая плата являться первичной, дополнительной или не перенесенной.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSubnet
Указывает имя подсети для NIC в виртуальной сети назначения, на которую необходимо выполнить миграцию сервера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IVMwareCbtNicInput

## Пуск

СВЯЗЫВАЮТ

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

