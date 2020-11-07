---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: f32b49e28f34b676c4154793ac37989b58b0c917
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914190"
---
# Set-AzureRmVMDiagnosticsExtension

## КРАТКИй обзор
Настраивает расширение диагностики Azure на виртуальной машине.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVMDiagnosticsExtension** настраивает расширение диагностики Azure на виртуальной машине.

## ИЛЛЮСТРИРУЮТ

### Пример 1: включение диагностики с помощью учетной записи хранения, указанной в файле конфигурации диагностики
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

Эта команда использует файл конфигурации диагностики, чтобы включить диагностику.
Файл diagnostics_publicconfig.xml содержит конфигурацию общедоступного XML для расширения диагностики, включая имя учетной записи хранения, в которую будут отправлены диагностические данные.
Учетная запись хранения диагностики должна находиться в той же подписке, что и виртуальная машина.

### Пример 2: включение диагностики с помощью имени учетной записи хранения
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

Эта команда использует имя учетной записи хранения, чтобы включить диагностику.
Если в конфигурации диагностики не указано имя учетной записи хранения или вы хотите переопределить имя учетной записи хранения диагностики, указанное в файле конфигурации, используйте параметр *StorageAccountName* .
Учетная запись хранения диагностики должна находиться в той же подписке, что и виртуальная машина.

### Пример 3: включение диагностики с помощью имени и ключа учетной записи хранения
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

Эта команда использует имя учетной записи хранения и ключ для включения диагностики.
Если учетная запись хранения диагностических данных находится в другой подписке, чем виртуальная машина, включите отправку диагностических данных в эту учетную запись хранения, явно указав ее имя и ключ.

## ПАРАМЕТРЫ

### -AutoUpgradeMinorVersion
Указывает, допускает ли этот командлет Гостевой агент Azure автоматическое обновление расширения до более поздней дополнительной версии.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
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

### -DiagnosticsConfigurationPath
Задает путь к файлу конфигурации.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Указывает расположение виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя расширения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

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

### -StorageAccountEndpoint
Указывает конечную точку учетной записи хранения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Указывает ключ учетной записи хранения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя учетной записи хранения.

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

### -StorageContext
Указывает контекст хранилища Azure.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Указывает версию расширения, используемую для этой виртуальной машины.
Чтобы получить версию, выполните командлет Get-AzureRmVMExtensionImage со значением Microsoft. COMPUTE для параметра *PublisherName* и VMAccessAgent для параметра *Type* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которой работает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVMDiagnosticsExtension](./Get-AzureRMVMDiagnosticsExtension.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[Remove-AzureRmVMDiagnosticsExtension](./Remove-AzureRmVMDiagnosticsExtension.md)


