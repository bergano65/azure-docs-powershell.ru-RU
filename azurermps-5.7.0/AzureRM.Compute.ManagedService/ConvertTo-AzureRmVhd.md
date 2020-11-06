---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561931"
---
# ConvertTo-AzureRmVhd

## КРАТКИй обзор
Преобразование виртуальной машины Hyper-V в Azure файлы виртуальных жестких дисков поддерживаются

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Преобразование виртуальной машины Hyper-V в Azure файлы виртуальных жестких дисков поддерживаются

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

Преобразование виртуальной машины Hyper-V с именем "тест" в службу Azure Поддерживаемые виртуальные жесткие диски в текущую папку.

## ПАРАМЕТРЫ

### -AsJob
Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExportPath
Путь к папке для экспорта, в которой будут храниться файлы на диске.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительно выполнить экспорт, даже если найдена существующая папка.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVServer
DNS-имя сервера Hyper-V, в качестве значения по умолчанию — "localhost".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVVMName
Имя Hyper-V.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### System. Management. Automation. PathInfo

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

