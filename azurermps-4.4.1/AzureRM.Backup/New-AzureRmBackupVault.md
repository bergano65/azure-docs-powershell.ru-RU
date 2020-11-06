---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565667"
---
# New-AzureRmBackupVault

## КРАТКИй обзор
Создание резервного хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmBackupVault** создает хранилище архивации Azure.
Этот командлет возвращает объект **AzureRmBackupVault** , который выступает в качестве ссылки на сущность хранилища.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание резервного хранилища
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Эта команда создает хранилище резервных копий Azure с именем Vault03.
Хранилище находится в группе ресурсов с именем ResourceGroup01 в регионе Западная часть США.
Хранилище использует тип хранилища с геоизбыточностью по умолчанию.

### Пример 2: создание хранилища резервных копий, использующего локально избыточное хранилище
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

Эта команда создает хранилище резервных копий Azure с именем Vault03.
Хранилище находится в группе ресурсов с именем ResourceGroup02 в регионе Западная часть США.
Хранилище использует тип хранилища LocallyRedundant.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя для хранилища резервных копий Azure.
Имя должно быть уникальным в группе ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region (регион)
Указывает регион Azure, в котором существует резервное хранилище.
В сценариях гибридного резервного копирования рекомендуется создать хранилище в регионе, близком к локальному серверу, чтобы уменьшить задержку.
Для резервного копирования инфраструктуры Azure в качестве виртуальных машин служб (IaaS) хранилище становится точкой обнаружения локальных виртуальных машин.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя существующей группы ресурсов Azure, в которой этот командлет создает резервное хранилище.
Чтобы создать группу ресурсов, используйте командлет New-AzureRMResourceGroup.
Группа ресурсов и хранилище резервных копий Azure не должны находиться в одном регионе.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает тип хранения архивных данных.
Допустимые значения этого параметра: LocallyRedundant и геоизбыточный.
Значение по умолчанию — геоизбыточное.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
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

### Ничего

## НАПРЯЖЕНИЕ

### AzureRmBackupVault

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


