---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983400"
---
# New-AzCloudService

## SYNOPSIS
Создание или обновление облачной службы.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

## СИНТАКСИС

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Создание или обновление облачной службы.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

## ПРИМЕРЫ

### Пример 1. Создание облачной службы с одной ролью
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

Над набором команд создается облачная служба с одной ролью

### Пример 2. Создание облачной службы с одной ролью и расширением RDP
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

Над набором команд создается облачная служба с одной ролью и расширением RDP.

### Пример 3. Создание облачной службы с одной ролью и сертификатом из хранилища ключа
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

С помощью вышеуказанного набора команд создается облачная служба с одной ролью и сертификатом из хранилища ключей.

### Пример 4. Создание облачной службы с несколькими ролями и расширениями
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

С помощью вышеуказанного набора команд создается облачная служба с одной ролью и сертификатом из хранилища ключей.

## PARAMETERS

### -AsJob
Запуск команды в качестве задания

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

### -Configuration
Определяет конфигурацию службы XML (CSCFG) для облачной службы.

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

### -ConfigurationUrl
Указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-проект.
URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения. Это свойство является свойством только для записи и не возвращается при звонках GET.

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
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionProfile
Описание профиля расширения облачной службы.
Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPROFILE и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение ресурса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя облачной службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkProfile
Профиль сети для облачной службы.
Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств NETWORKPROFILE и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Запуск команды асинхронно

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

### -OSProfile
В статье описан профиль ОС для облачной службы.
Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств OSPROFILE и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageUrl
Url-адрес, который ссылается на расположение пакета службы в службе BLOB-документов.
URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения. Это свойство является свойством только для записи и не возвращается при звонках GET.

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleProfile
Описание профиля роли для облачной службы.
Чтобы построить новую таблицу, см. раздел "Заметки" для свойств ROLEPROFILE и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartCloudService
(Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.
Значение по `true` умолчанию: . Если это так, модель обслуживания по-прежнему развертывается, но код не будет запускаться сразу.
Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.
С развернутой службы по-прежнему взимается плата, даже если она отключена.

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

### -SubscriptionId
Учетные данные подписки, однозначно определяют подписку Microsoft Azure.
Он является частью URI каждого звонка службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Теги ресурсов.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeMode
Режим обновления облачной службы.
При развертывании службы для обновления доменов выделяются экземпляры ролей.
Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления. Возможные значения: автоматически вручную, если не указано, по умолчанию \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\> задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.
Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


EXTENSIONPROFILE <ICloudServiceExtensionProfile> : описание профиля расширения облачной службы.
  - `[Extension <IExtension[]>]`: Список расширений для облачной службы.
    - `[AutoUpgradeMinorVersion <Boolean?>]`. Явным образом укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более мелких версий, когда они станут доступны.
    - `[ForceUpdateTag <String>]`: примените к тегу предоставленные общедоступные и защищенные параметры.         Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.         Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.         Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет возможно повторное внедрение.
    - `[Name <String>]`: имя расширения.
    - `[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.
    - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
    - `[Publisher <String>]`: имя издателя обработера расширений.
    - `[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения. Если свойство не указано или указано "*", расширение применяется для всех ролей в облачной службе.
    - `[Setting <String>]`: общедоступные параметры расширения. Для расширений JSON это параметры JSON. Для расширения XML (например, RDP) это параметр XML для расширения.
    - `[SourceVaultId <String>]`: ИД ресурса
    - `[Type <String>]`: тип расширения.
    - `[TypeHandlerVersion <String>]`: определяет версию расширения. Определяет версию расширения. Если этот элемент не указан или в качестве значения используется звездочка (*), используется последняя версия расширения. Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии. Если указан основной и второстепенный номер версии (X.Y), будет выбрана конкретная версия расширения. Если указана версия, для экземпляра роли выполняется автоматическое обновление.

NETWORKPROFILE: <ICloudServiceNetworkProfile> профиль сети для облачной службы.
  - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.
    - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов
      - `[Name <String>]`: 
      - `[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.
      - `[PublicIPAddressId <String>]`: ИД ресурса
      - `[SubnetId <String>]`: ИД ресурса
    - `[Name <String>]`: Название ресурса
  - `[SwappableCloudService <ISubResource>]`: 
    - `[Id <String>]`: ИД ресурса

OSPROFILE <ICloudServiceOSProfile> : описание профиля ОС для облачной службы.
  - `[Secret <ICloudServiceVaultSecretGroup[]>]`: набор сертификатов, которые должны быть установлены на экземпляры ролей.
    - `[SourceVaultId <String>]`: ИД ресурса
    - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.
      - `[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.

ROLEPROFILE <ICloudServiceRoleProfile> : описание профиля роли для облачной службы.
  - `[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.
    - `[Name <String>]`: название ресурса.
    - `[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.
    - `[SkuName <String>]`: название SKU. ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наномном оборудовании сейчас работает облачная служба, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.
    - `[SkuTier <String>]`: определяет уровень облачной службы. Возможные значения <br /><br /> **Стандартный** <br /><br /> **Базовая**

## СВЯЗАННЫЕ ССЫЛКИ

