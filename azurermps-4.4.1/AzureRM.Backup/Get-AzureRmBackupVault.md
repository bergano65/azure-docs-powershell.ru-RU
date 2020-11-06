---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560519"
---
# Get-AzureRmBackupVault

## КРАТКИй обзор
Возвращает хранилище резервных копий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupVault** получает резервные хранилища Azure.
Этот командлет возвращает объекты **AzureRmBackupVault** для использования с другими командлетами.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Просмотр всех резервных хранилищ
```
PS C:\>Get-AzureRmBackupVault
```

Эта команда получает все резервные хранилища Azure.

### Пример 2: Просмотр всех хранилищ, созданных в Запад США
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Эта команда возвращает все резервные хранилища.
Команда передает их в командлет Where-Object с помощью оператора конвейера.
Этот командлет фильтрует результаты, основываясь на свойстве **Region** .
Для получения дополнительных сведений введите `Get-Help Where-Object` .

### Пример 3: получение определенного хранилища
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Эта команда получает хранилище с именем Vault03.

### Пример 4: подсчет количества хранилищ с локально избыточным хранилищем
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Эта команда получает все резервные хранилища Azure.
Команда передает их в **Where-Object** , который фильтрует результаты на основе свойства **Storage** .
Команда передается командлету Measure-Object, который содержит значение "LocallyRedundant", в котором учитываются результаты.
Для получения дополнительных сведений введите `Get-Help Measure-Object` .

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя хранилища резервных копий, которое получает этот командлет.
Если несколько хранилищ резервных копий имеют одинаковое имя, этот командлет возвращает их все.
Укажите параметр *ResourceGroupName* , чтобы получить уникальное хранилище.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure, в которой этот командлет получает резервное хранилище.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
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

## НАПРЯЖЕНИЕ

### AzureRmBackupVault

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


