---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405852"
---
# Add-AzVMSecret

## SYNOPSIS
Добавляет секрет в виртуальную машину.

## СИНТАКСИС

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Add-AzVMSecret** добавляет секрет в виртуальную машину.
Это значение позволяет добавить сертификат на виртуальную машину.
Секрет должен храниться в хранилище ключей.
Дополнительные сведения о хранилище ключей см. в [подмносях "Хранилище ключей Azure".](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
Дополнительные сведения о [cmdlets](/powershell/module/az.keyvault/set-azkeyvaultsecret) см. в [cmdlets хранилища](/powershell/module/az.keyvault) ключей Azure или в этом наборе.

## ПРИМЕРЫ

### Пример 1. Добавление секрета на виртуальную машину
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Вторая команда создает объект учетных данных с Get-Credential командлета, а затем сохраняет результат в $Credential переменной.
В результате будет предложено вводить имя пользователя и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .
Третья команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, $VirtualMachine.
Четвертая команда назначает исходный код хранилища переменной $SourceVaultId для использования в дальнейшем.
Предполагается, что переменная $SubscriptionId имеет соответствующее значение.
Пятая команда назначает значение переменной $CertificateStore 01 для использования в дальнейшем.
Шестая команда назначает URL-адрес для магазина сертификатов.
Седьмой команда добавляет секрет к виртуальной машине, которая хранится в $VirtualMachine.
Параметр SourceVaultId определяет хранилище ключей.
Команда указывает имя магазина сертификатов и URL-адрес сертификата.
Вы можете несколько раз запустить **надстройку "AzVMSecret",** чтобы добавить секрет для других сертификатов.

## PARAMETERS

### -CertificateStore
Указывает имя магазина сертификатов на виртуальной машине, на которую работает операционная система Windows.
Этот cmdlet добавляет сертификат в хранилище, указанное этим параметром.
Этот параметр можно указать только для виртуальных машин, работающих в операционной системе Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Указывает URL-адрес, который указывает на секрет ключного сейфа, который содержит сертификат.
Сертификат — это кодировки Base64 для следующего объекта нотации объектов JavaScript (JSON), который закодирован в UTF-8: { "data": \<Base64-encoded-file\> " ", "dataType": " ", "password": " " } В настоящее время dataType принимает только \<file-format\> \<pfx-file-password\> PFX-файлы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SourceVaultId
Определяет ИД ресурса хранилища ключей, который содержит сертификаты, которые можно добавить на виртуальную машину.
Это значение также является ключом для добавления нескольких сертификатов.
Это означает, что для *SourceVaultId* можно использовать одинаковое значение при добавлении нескольких сертификатов из одного хранилища ключей.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект виртуальной машины, который изменяет этот cmdlet.
Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)
Для создания объекта виртуальной машины можно использовать [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
