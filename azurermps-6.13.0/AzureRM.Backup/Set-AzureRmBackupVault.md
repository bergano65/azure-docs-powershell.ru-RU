---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561140"
---
# Set-AzureRmBackupVault

## КРАТКИй обзор
Изменяет тип хранилища резервного хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmBackupVault** изменяет тип хранилища для хранилища резервных копий Azure.
Изменить другие свойства хранилища нельзя.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение хранилища для существующего хранилища
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

Эта команда получает хранилище резервных копий Azure с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда передает это хранилище в текущий командлет с помощью оператора конвейера.
Текущий командлет изменяет тип хранилища на LocallyRedundant.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Хранилище
Указывает тип хранения архивных данных.
Допустимые значения этого параметра: LocallyRedundant и геоизбыточный.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, которое изменяет этот командлет.
Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Параметры: хранилище (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault

## Пуск
* При регистрации первого сервера или виртуальной машины для хранилища этот тип хранения заблокирован. Впоследствии изменить тип хранилища нельзя.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)


