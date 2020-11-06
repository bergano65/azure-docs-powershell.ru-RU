---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562732"
---
# Get-AzureRmRecoveryServicesBackupProperty

## КРАТКИй обзор
Получает свойства резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRecoveryServicesBackupProperty** получает свойства резервного копирования для хранилища служб восстановления.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

Получите свойство резервного хранилища для хранилища.

## ПАРАМЕТРЫ

### -Хранилище
Указывает имя хранилища.
Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
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

### Microsoft. Azure. Commands. RecoveryServices. ARSVault
Параметры: хранилище (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
