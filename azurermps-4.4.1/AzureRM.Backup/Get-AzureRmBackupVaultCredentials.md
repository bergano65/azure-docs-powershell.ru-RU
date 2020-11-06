---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: b208602532428d14c2af1504c5b8af2cce0b155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560516"
---
# Get-AzureRmBackupVaultCredentials

## КРАТКИй обзор
Загружает файл учетных данных хранилища для резервного хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupVaultCredentials** загружает файл учетных данных хранилища для резервного хранилища Azure.

Функция резервного копирования использует файл учетных данных хранилища, чтобы подключить сервер к хранилищу резервных копий Azure и зарегистрировать его.
Вы должны зарегистрировать сервер перед тем, как резервная копия сможет отправлять резервные данные в хранилище.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -TargetLocation
Указывает конечный путь, по которому этот командлет хранит файл учетных данных хранилища.

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

### -Хранилище
Указывает хранилище резервных копий, для которого этот командлет получает файл учетных данных хранилища.
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

### AzureRMBackupVault

## НАПРЯЖЕНИЕ

### Подстрок
Этот командлет возвращает имя файла учетных данных хранилища.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


