---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563476"
---
# Remove-AzureKeyVaultKey

## КРАТКИй обзор
Удаление ключа из хранилища ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByVaultName (по умолчанию)
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Remove-AzureKeyVaultKey удаляет раздел из хранилища ключей.
Если клавиша была случайно удалена, ключ может быть восстановлен с помощью Undo-AzureKeyVaultKeyRemoval пользователем, у которого есть особые разрешения на восстановление.
Этот командлет имеет значение High для свойства **ConfirmImpact** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление ключа из хранилища ключей
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.

### Пример 2: Удаление ключа без подтверждения пользователя
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.
Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.

### Пример 3: Удаление удаленного ключа из хранилища ключей без возможности восстановления
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Эта команда удаляет ключ с именем ITSoftware из хранилища ключей Contoso без возможности восстановления.
Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.

### Пример 4: Удаление ключей с помощью оператора Pipeline
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

Эта команда получает все ключи из хранилища ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.
Этот командлет передает ключи со значением $False для атрибута **Enabled** для текущего командлета.
Этот командлет удаляет эти ключи.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -InputObject
Объект KeyBundle

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Удаление ранее удаленного ключа без возможности восстановления.

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

### -Name (имя)
Задает имя удаляемого ключа.
Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** .
По умолчанию этот командлет не создает никаких выходных данных.

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

### -VaultName
Указывает имя хранилища ключей, из которого нужно удалить ключ.
Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется. Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey
Этот командлет возвращает значение только в том случае, если указан параметр *PassThru* .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

[Undo-AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

