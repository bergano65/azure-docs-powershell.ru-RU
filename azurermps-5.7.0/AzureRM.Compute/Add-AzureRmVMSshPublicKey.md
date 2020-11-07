---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732387"
---
# Add-AzureRmVMSshPublicKey

## КРАТКИй обзор
Добавляет открытые ключи для SSH для виртуальной машины.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVMSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальной машине по защищенной оболочке (SSH).

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление открытого ключа для виртуальной машины
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .
Команда сохраняет виртуальную машину в переменной $VirtualMachine.

Вторая команда добавляет открытый ключ в расположение в VirtualMachine07, которое указывает параметр path.

## ПАРАМЕТРЫ

### -KeyData
Задает базовую кодировку 64 для открытого ключа.
Вы можете подключаться к виртуальной машине с помощью SSH или ключа, который указывает этот параметр.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.
Если файл уже существует, этот командлет добавляет ключ к файлу.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Указывает объект виртуальной машины, измененный этим командлетом.
Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .
Вы можете использовать командлет [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) для создания объекта виртуальной машины.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
