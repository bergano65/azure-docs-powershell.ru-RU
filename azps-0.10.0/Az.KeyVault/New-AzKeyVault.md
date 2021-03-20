---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 9d452c888fd0fe302fd57792830c5bb2bf5ee8c0
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104713562"
---
# New-AzKeyVault

## SYNOPSIS
Создает хранилище ключей.

## СИНТАКСИС

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
При **нажатии на AzKeyVault** создается хранилище ключа в указанной группе ресурсов. Этот cmdlet также предоставляет текущим входя в систему пользователю разрешения на добавление, удаление и секрет списков и секретов в хранилище ключей.

Примечание. Если при попытке создать новое хранилище ключей подписка не зарегистрирована для использования пространства имен **Microsoft.KeyVault,** запустите **register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault",** а затем повторно запустите команду **New-AzKeyVault.** Дополнительные сведения см. в register-AzResourceProvider.

## ПРИМЕРЫ

### Пример 1. Создание стандартного хранилища ключей
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

Эта команда создает хранилище с именем Contoso03Vault в регионе Azure East US. Команда добавляет хранилище ключа в группу ресурсов с именем "Группа14". Так как команда не указывает значение параметра *SKU,* она создает стандартный сейф ключей.

### Пример 2. Создание сейфа ключа Premium
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

Эта команда создает хранилище ключей, как в предыдущем примере. Однако она указывает значение Premium для параметра *SKU,* чтобы создать хранилище ключей Premium.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Позволяет поставщику ресурсов Microsoft.Compute извлекать секрет из этого ключевого сейфа, когда на него ссылается создание ресурсов, например при создании виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Позволяет службе шифрования дисков Azure получать секрет и отобирать ключи из этого key vault.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Позволяет Диспетчеру ресурсов Azure получать секрет из этого сейфа ключа, если на этот ключ ссылается развертывание шаблона.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableSoftDelete
Указывает, что для этого key vault включена функциональность soft-delete. Если включено soft-delete, в течение льготного периода вы можете восстановить этот сейф ключа и его содержимое после удаления.

Дополнительные сведения об этой функции см. в обзоре [soft-delete key Vault Azure.](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete) Инструкции см. в инструкциях по использованию key [Vault soft-delete с помощью PowerShell.](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Определяет регион Azure, в котором нужно создать хранилище ключа. Используйте команду [Get-AzLocation,](/powershell/module/az.resources/get-azlocation) чтобы увидеть ваши варианты.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Указывает SKU экземпляра key vault. Сведения о том, какие функции доступны для каждого SKU, см. на веб-сайте цены на ключ хранилища Azure ( https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Пары значений ключа в виде hash table. Например:

@{key0="value0";key1=$null;key2="value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Указывает имя создаемого хранилища ключей. Имя может быть любым сочетанием букв, цифр или дефисов. Имя должно начинаться с буквы или цифры. Имя должно быть универсальным.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet не принимает входные данные.

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSVault

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVault](./Remove-AzKeyVault.md)
