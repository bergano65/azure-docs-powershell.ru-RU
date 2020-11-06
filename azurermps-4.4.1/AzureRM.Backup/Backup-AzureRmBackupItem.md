---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559971"
---
# Backup-AzureRmBackupItem

## КРАТКИй обзор
Запуск резервного копирования для элемента резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **BACKUP-AzureRmBackupItem** запускает резервное копирование для защищенного элемента резервного копирования Azure, не привязанного к расписанию резервного копирования.
Вы можете выполнить начальную архивацию немедленно, после того как вы включите защиту или начнете создание резервной копии после сбоя архивации по расписанию.

При выполнении существующего задания резервного копирования этот командлет завершается сбоем.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Начало создания резервной копии виртуальной машины
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета Get-AzureRmBackupContainer.
Команда сохраняет этот объект в переменной $Container.

Последняя команда получает элементы резервного копирования в $Container с помощью командлета Get-AzureRmBackupItem.
Команда передает элементы в текущий командлет с помощью оператора конвейера.
Текущий командлет запускает резервное копирование виртуальной машины в контейнере.

## ПАРАМЕТРЫ

### -Item
Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### AzureRMBackupItem

## НАПРЯЖЕНИЕ

### AzureRmBackupJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Restore-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


