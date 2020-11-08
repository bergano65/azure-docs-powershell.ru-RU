---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077351"
---
# Set-AzureVMDscExtension

## КРАТКИй обзор
Настраивает расширение DSC на виртуальной машине.

## Максимальное

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureVMDscExtension** настраивает расширение конфигурации нужного состояния (DSC) на виртуальной машине.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка расширения DSC на виртуальной машине
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

Эта команда настраивает расширение DSC на виртуальной машине.

Пакет MyConfiguration.ps1.zip должен быть предварительно загружен в хранилище Azure с помощью команды **Publish-AzureVMDscConfiguration** и включает сценарий MyConfiguration.ps1 и модули, от которых он зависит.

Аргумент MyConfiguration указывает определенную конфигурацию DSC в сценарии для выполнения.
Параметр- *ConfigurationArgument* указывает Hashtable с аргументами, которые передаются в функцию конфигурации.

### Пример 2: Настройка расширения DSC на виртуальной машине с помощью пути к данным конфигурации
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

Эта команда настраивает расширение DSC на виртуальной машине, используя путь к данным конфигурации.

## ПАРАМЕТРЫ

### -ConfigurationArchive
Указывает имя пакета конфигурации (ZIP-файла), который ранее был передан командой Publish — AzureVMDscConfiguration.
Этот параметр должен указывать только имя файла без пути.

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

### -ConfigurationArgument
Указывает хэш-таблицу, указывающую аргументы для функции конфигурации.
Ключи соответствуют именам параметров и значениям для значений параметров.

Для этого параметра допустимы следующие значения:

- примитивные типы
- подстрок
- IsArray
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Указывает путь к PSD1-файлу, который определяет данные для функции конфигурации.
Этот файл должен содержать Hashtable, как описано в разделе разделение конфигурации и данных среды https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Указывает имя сценария конфигурации или модуля, вызываемого расширением DSC.

Значение этого параметра должно быть именем одной из функций конфигурации, которые содержатся в сценариях или модулях, упакованных в *ConfigurationArchive*.

Этот командлет по умолчанию имеет имя файла, заданного параметром *ConfigurationArchive* , если опустить этот параметр, исключая все расширения.
Например, если *ConfigurationArchive* "SalesWebSite.ps1.zip", для *configurationName* используется значение по умолчанию "SalesWebSite".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContainerName
Указывает имя контейнера хранилища Azure, где расположен *ConfigurationArchive* .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Коллекция
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Указывает на то, что этот командлет перезапишет существующие большие двоичные объекты.

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

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferenceName
Задает пользовательскую строку, которую можно использовать для ссылки на расширение.
Этот параметр задается, когда расширение добавляется на виртуальную машину в первый раз.
При последующих обновлениях необходимо указать ранее использованное Справочное имя, когда вы обновите расширение.
*ReferenceName* , назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Указывает контекст хранилища Azure, предоставляющий параметры безопасности, используемые для доступа к сценарию конфигурации.
Этот контекст предоставляет доступ на чтение к контейнеру, указанному в параметре *ContainerName* .

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Задает суффикс DNS Endpoint для всех служб хранилища (например, "core.contoso.net").

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Указывает определенную версию расширения DSC, которую вы хотите использовать.
По умолчанию задано значение "1. *", если этот параметр не указан.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Указывает Сохраняемый объект виртуальной машины.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
Указывает версию платформы управления Windows (WMF) для установки на виртуальной машине.
Расширение DSC зависит от функций DSC, которые доступны только в обновлениях WMF.
Этот параметр указывает версию обновления для установки на виртуальной машине.
Для этого параметра допустимы следующие значения:

- 4,0.
Устанавливает WMF 4,0, если уже не установлена более новая версия.
- 5,0.
Установка последней версии WMF 5,0.
- последнюю.
Установка последней версии WMF, в настоящее время WMF 5,0.

Значение по умолчанию — новейшее.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Publish-AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


