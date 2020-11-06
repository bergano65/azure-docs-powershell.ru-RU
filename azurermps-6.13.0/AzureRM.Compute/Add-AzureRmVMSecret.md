---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 539c9306709b7044f2a3d7263ac8168d59f54e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566827"
---
# Add-AzureRmVMSecret

## КРАТКИй обзор
Добавляет секрет для виртуальной машины.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVMSecret** добавляет секрет на виртуальную машину.
Это значение позволяет добавить сертификат на виртуальную машину.
Секрет должен храниться в хранилище ключей.
Дополнительные сведения о хранилище ключей можно найти в разделе [что такое Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Дополнительные сведения о командлетах можно найти в статьях [командлетов Azure Key Vault](https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft или командлете [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление секрета на виртуальную машину
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.
Команда назначает имя и размер виртуальной машине.
Вторая команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.
В командной строке будет предложено ввести имя пользователя и пароль.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .
Третья команда использует командлет **Set-AzureRmVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.
Четвертая команда назначает идентификатор исходного хранилища переменной $SourceVaultId для последующего использования.
Предполагается, что переменной $SubscriptionId присвоено нужное значение.
Пятая команда присваивает значение переменной $CertificateStore 01 для последующего использования.
Шестая команда назначает URL-адрес для хранилища сертификатов.
Седьмая команда добавляет секрет на виртуальную машину, хранящуюся в $VirtualMachine.
Параметр SourceVaultId указывает хранилище ключей.
Команда задает имя хранилища сертификатов и URL-адрес сертификата.
Вы можете повторно запустить **надстройку "AzureRmVMSecret** ", чтобы добавить секреты для других сертификатов.

## ПАРАМЕТРЫ

### -CertificateStore
Указывает имя хранилища сертификатов на виртуальной машине, работающей под управлением операционной системы Windows.
Этот командлет добавляет сертификат в хранилище, которое указывает этот параметр.
Этот параметр можно задать только для виртуальных машин, работающих под управлением операционной системы Windows.

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
Указывает URL-адрес, указывающий на секретный ключ хранилища, который содержит сертификат.
Сертификат — это кодировка Base64 следующего объекта JSON, который кодируется в кодировке UTF-8: {"Data": "", "Password": "" \<Base64-encoded-file\> \<file-format\> , \<pfx-file-password\> в настоящее время DataType принимает только PFX-файлы.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Это означает, что вы можете использовать одно и то же значение для *SourceVaultId* при добавлении нескольких сертификатов из одного и того же хранилища ключей.

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
Указывает объект виртуальной машины, измененный этим командлетом.
Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .
Вы можете использовать командлет [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) для создания объекта виртуальной машины.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
