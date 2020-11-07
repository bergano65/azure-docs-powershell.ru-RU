---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
ms.openlocfilehash: 9c31442e1242114572540c23049f26715fc3099e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913695"
---
# Add-AzureRmVmssSecret

## КРАТКИй обзор
Добавляет секрет в VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVmssSecret** добавляет секрет в набор масштабов виртуальных машин (VMSS).
Секрет должен храниться в хранилище ключей Azure.
Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft Developer или командлет [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление секрета в VMSS
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

В этом примере в VMSS добавляется секрет.
Первая команда использует командлет Get-AzureRmKeyVault для получения секрета из хранилища с именем ContosoVault и сохраняет результат в переменной с именем $Vault.
Вторая команда использует командлет **New-AzureRmVmssVaultCertificateConfig** для создания конфигурации сертификата хранилища ключей с помощью указанного URL-адреса сертификата из хранилища сертификатов с именем Certificates и сохраняет результаты в переменной с именем $CertConfig.
Третья команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.
Четвертая команда добавляет секрет в VMSS с помощью секретного ключа хранилища, используя идентификатор ресурса Key и сертификат хранилища, хранящийся в переменных $Vault и $CertConfig.

## ПАРАМЕТРЫ

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
Указывает идентификатор ресурса для хранилища ключей, содержащего сертификаты, которые можно добавить на виртуальную машину.
Это значение также действует в качестве ключа для добавления нескольких сертификатов.
Это означает, что вы можете использовать одно и то же значение для параметра *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.

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
Указывает объект **сертификата** хранилища, который содержит URL-адрес сертификата и имя сертификата.
Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) .

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
Чтобы создать этот объект, можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### VirtualMachineScaleSet
Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.

## НАПРЯЖЕНИЕ

### Ничего
Этот командлет не создает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
