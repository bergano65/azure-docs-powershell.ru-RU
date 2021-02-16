---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211876"
---
# Update-AzCloudService

## SYNOPSIS
Создайте или обновйте облачную службу.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

## СИНТАКСИС

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Создайте или обновйте облачную службу.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

## ПРИМЕРЫ

### Пример 1. Добавление расширения RDP в существующую облачную службу
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Над набором команд добавляется расширение RDP к уже существующей облачной службе ContosoCS, которая принадлежит к группе ресурсов ContosOrg.

### Пример 2. Удаление всех расширений из облачной службы
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Набор команд выше удаляет все расширения из существующей облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.

### Пример 3. Удаление расширения RDP из облачной службы
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Над набором команд удаляется расширение RDP из существующей облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.

### Пример 4. Scale-Out и Scale-In роли
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Над набором команд показано, как масштабировать и масштабировать количество экземпляров ролей для облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.

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

### -InputObject
Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Parameter
Описание облачной службы.
Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств PARAMETER и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : Параметр identity
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: путь удостоверения ресурса
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: Имя экземпляра роли.
  - `[RoleName <String>]`: Название роли.
  - `[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure. Он является частью URI каждого звонка службы.
  - `[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления. Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.

PARAMETER <ICloudService> : Описание облачной службы.
  - `Location <String>`: расположение ресурса.
  - `[Configuration <String>]`Определяет конфигурацию службы XML (CSCFG) для облачной службы.
  - `[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес. URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.         Это свойство является свойством только для записи и не возвращается при звонках GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.
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
      - `[TypeHandlerVersion <String>]`: Определяет версию расширения. Определяет версию расширения. Если этот элемент не указан или в качестве значения используется звездочка (*), используется последняя версия расширения. Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии. Если указан основной и второстепенный номер версии (X.Y), будет выбрана конкретная версия расширения. Если указана версия, для экземпляра роли выполняется автоматическое обновление.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Профиль сети для облачной службы.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.
        - `[PublicIPAddressId <String>]`: ИД ресурса
        - `[SubnetId <String>]`: ИД ресурса
      - `[Name <String>]`: Название ресурса
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: ИД ресурса
  - `[OSProfile <ICloudServiceOSProfile>]`: описание профиля ОС для облачной службы.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Набор сертификатов, которые нужно установить на экземпляры ролей.
      - `[SourceVaultId <String>]`: ИД ресурса
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.
        - `[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.
  - `[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета обслуживания в службе BLOB-бизнес. URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.         Это свойство является свойством только для записи и не возвращается при звонках GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.
      - `[Name <String>]`: название ресурса.
      - `[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.
      - `[SkuName <String>]`: название SKU. ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наемное облачным сервисом, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.
      - `[SkuTier <String>]`: уровень облачной службы. Возможные значения <br /><br /> **Стандартный** <br /><br /> **Базовая**
  - `[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания. Значение по `true` умолчанию: .         Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится. Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена. С развернутой службы по-прежнему взимается плата, даже если она отключена.
  - `[Tag <ICloudServiceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы. При развертывании службы для обновления доменов выделяются экземпляры ролей. Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.         Возможные значения <br /><br />**Авто**<br /><br />**Вручную** <br /><br />**Одновременный**<br /><br />         Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain. Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.

## СВЯЗАННЫЕ ССЫЛКИ

