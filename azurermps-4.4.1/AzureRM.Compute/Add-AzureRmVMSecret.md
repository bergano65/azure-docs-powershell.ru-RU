---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 6faeed8ecfd3dfb02bf761458e6a2c5a68af27a6
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104715626"
---
# Add-AzureRmVMSecret

## SYNOPSIS
Добавляет секрет в виртуальную машину.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## СИНТАКСИС

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Благодаря **cmdlet Add-AzureRmVMSecret** вы можете добавить секрет в виртуальную машину.
Это значение позволяет добавить сертификат на виртуальную машину.
Секрет должен храниться в хранилище ключей.
Дополнительные сведения о хранилище ключей см. в [подмносях "Хранилище ключей Azure".](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
Дополнительные сведения о cmdlets см. в Microsoft Developer Network библиотеке ключевых хранилищ [Azure](/powershell/module/azurerm.keyvault/) или в Microsoft Developer Network [Set-AzureKeyVaultSecret.](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret)

## ПРИМЕРЫ

### Пример 1. Добавление секрета на виртуальную машину
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.

Вторая команда создает объект учетных данных с Get-Credential командлета, а затем сохраняет результат в $Credential переменной.
В командной области будет предложено вводить имя пользователя и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

Третья команда использует командлет **Set-AzureRmVMOperatingSystem** для настройки виртуальной машины, $VirtualMachine.

Четвертая команда назначает исходный код хранилища переменной $SourceVaultId для использования в дальнейшем.
Предполагается, что переменная $SubscriptionId имеет соответствующее значение.

Пятая команда назначает значение переменной $CertificateStore 01 для использования в дальнейшем.

Шестая команда назначает URL-адрес для магазина сертификатов.

Седьмой команда добавляет секрет к виртуальной машине, которая хранится в $VirtualMachine.
Параметр SourceVaultId определяет хранилище ключей.
Команда указывает имя магазина сертификатов и URL-адрес сертификата.
Вы можете несколько раз запустить **надстройку Add-AzureRmVMSecret,** чтобы добавить секрет других сертификатов.

## PARAMETERS

### -CertificateStore
Указывает имя магазина сертификатов на виртуальной машине, на которую работает операционная система Windows.
Этот cmdlet добавляет сертификат в хранилище, указанное этим параметром.
Этот параметр можно указать только для виртуальных машин, работающих в операционной системе Windows.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Url-адрес, который указывает на секрет ключного сейфа, который содержит сертификат.

Сертификат — это кодировки Base64 для следующего объекта Нотации объектов JavaScript (JSON), который закодирован в UTF-8:

{ "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": \<pfx-file-password\> " " }


В настоящее время dataType принимает только PFX-файлы.

```yaml
Type: String
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
Это означает, что для *SourceVaultId* можно использовать одно и то же значение при добавлении нескольких сертификатов из одного сейфа ключа.

```yaml
Type: String
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
Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzureRmVM.](./Get-AzureRmVM.md)
Для создания объекта виртуальной машины можно использовать новый для [AzureRmVMConfig.](./New-AzureRmVMConfig.md)

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### PSVirtualMachine
Параметр VM принимает значение типа PSVirtualMa в конвейере

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
