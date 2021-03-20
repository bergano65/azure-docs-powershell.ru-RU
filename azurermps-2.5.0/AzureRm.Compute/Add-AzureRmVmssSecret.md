---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
ms.openlocfilehash: f71af896d99bfcf6227fd805fb6896d4d28180d4
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104716274"
---
# Add-AzureRmVmssSecret

## SYNOPSIS
Добавляет секрет в VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## СИНТАКСИС

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Этот cmdlet добавляет секрет в набор масштаба виртуальной машины (VMSS) с использованием **add-AzureRmVmssSEcret.**
Секрет должен храниться в хранилище ключей Azure.
Дополнительные сведения, связанные с хранилищем ключей, см. в [подмносях "Что такое хранилище ключей Azure"?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Дополнительные сведения о cmdlets см. в Microsoft Developer Network библиотеке ключевых хранилищ [Azure](/powershell/module/azurerm.keyvault/) или в Microsoft Developer Network [Set-AzureKeyVaultSecret.](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret)

## ПРИМЕРЫ

### Пример 1. Добавление секрета в VMSS
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

В этом примере к службам VMSS добавляется секрет.
Первая команда использует Get-AzureRmKeyVault для получения секретного сейфа из сейфа ContosoVault и сохраняет результат в переменной с именем $Vault.
Вторая команда использует командлет **New-AzureRmVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с использованием указанного URL-адреса сертификата из хранилища сертификатов и хранения результатов в переменной с именем $CertConfig.
Третья команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.
Четвертая команда добавляет секрет в VMSS с использованием секрета сейфа, используя ключ ресурса и сертификат хранилища, $Vault и $CertConfig переменных.

## PARAMETERS

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

### -SourceVaultId
Определяет ИД ресурса хранилища ключей, который содержит сертификаты, которые можно добавить на виртуальную машину.
Это значение также является ключом для добавления нескольких сертификатов.
Это означает, что для параметра *SourceVaultId* можно использовать одно и то же значение при добавлении нескольких сертификатов из одного сейфа ключа.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultCertificate
Указывает объект **сертификата хранилища,** содержащий URL-адрес сертификата и имя сертификата.
Для создания этого объекта можно использовать новый для [AzureRmVmssVaultCertificateConfig.](./New-AzureRmVmssVaultCertificateConfig.md)

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает объект VMSS.
Для создания этого объекта можно использовать новый [cmdlet AzureRmVmssConfig.](./New-AzureRmVmssConfig.md)

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### VirtualMa ветвьScaleSet
Параметр VirtualMachineScaleSet принимает значение типа VirtualMascaleeScaleSet из конвейера.

## OUTPUTS

### Нет
Этот cmdlet не создает никаких выходных данных.

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
