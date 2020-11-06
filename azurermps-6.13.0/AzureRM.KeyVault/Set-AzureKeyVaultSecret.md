---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 820406a3fe4bebfd0b2a972bb8676bbd483f7080
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560148"
---
# Set-AzureKeyVaultSecret

## КРАТКИй обзор
Создание или обновление секрета в хранилище ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### По умолчанию (по умолчанию)
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureKeyVaultSecret** создает или обновляет секретный ключ в хранилище ключей Azure Key Vault. Если секрет не существует, этот командлет создаст его. Если секрет уже существует, этот командлет создает новую версию этого секрета.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение значения секрета с помощью атрибутов по умолчанию
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret. Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .
Вторая команда изменяет значение секрета с именем ITSecret в хранилище ключей, именуемом contoso. Секретное значение становится значением, хранящимся в $Secret.

### Пример 2: изменение значения секрета с помощью настраиваемых атрибутов
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret. Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .
Следующие команды определяют пользовательские атрибуты для даты окончания срока действия, тегов и типа контекста и хранят атрибуты в переменных.
Последняя команда изменяет значения секрета ITSecret в хранилище ключей, именуемом Contoso, используя значения, указанные ранее в качестве переменных.

## ПАРАМЕТРЫ

### -ContentType
Указывает тип содержимого секрета.
Чтобы удалить существующий тип контента, укажите пустую строку.

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

### -Отключение
Указывает на то, что этот командлет отключает секрет.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Истекает
Задает время истечения срока действия, как объект **DateTime** , для секрета, который обновляется этим командлетом.
Этот параметр использует координированное координированное время (UTC). Чтобы получить объект **DateTime** , используйте командлет **Get-Date** . Для получения дополнительных сведений введите `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Секретный объект

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя секрета, который нужно изменить. Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Указывает время в виде объекта **DateTime** , перед которым нельзя использовать секрет. Этот параметр использует время в формате UTC. Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecretValue
Задает значение для секрета как объект **SecureString** . Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** . Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Указывает имя хранилища ключей, к которому относится этот секрет. Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecretIdentityItem
Параметры: InputObject (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)
