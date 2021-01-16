---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407740"
---
# Restore-AzKeyVaultCertificate

## SYNOPSIS
Восстановление сертификата в хранилище ключа из файла резервной копии.

## СИНТАКСИС

### ByVaultName (по умолчанию)
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
При нажатии на **AzKeyVaultCertificate** в указанном хранилище ключа создается сертификат из файла резервной копии.
Этот сертификат является копией архивного сертификата в входной файле с тем же именем, что и у исходного сертификата.
Если хранилище ключей уже содержит сертификат с таким же именем, этот cmdlet не может переописать исходный сертификат.
Если резервная копия содержит несколько версий сертификата, восстанавливаются все версии.
Хранилище ключей, в которое вы восстанавливаете сертификат, может быть не таким, как в хранилище ключей, из хранилища, из который был восстановлен сертификат.
Однако ключ должен использовать ту же подписку и быть в регионе Azure в той же географической области (например, в Северной Америке).
См. центр управления доверием Microsoft Azure (сопоставление регионов https://azure.microsoft.com/support/trust-center/) Azure с регионами).

## ПРИМЕРЫ

### Пример 1. Восстановление back-up certificate
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

Эта команда восстанавливает сертификат, включая все его версии, из файла резервной копии Backup.blob в хранилище ключа MyKeyVault.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
Входной файл.
Входной файл, содержащий исходный BLOB-файл

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

### -InputObject
Объект KeyVault

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceId
KeyVault Resource Id

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Имя сейфа.
С его учетом именем и выбранной средой строится FQDN хранилища.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
