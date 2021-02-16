---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229180"
---
# Switch-AzCloudService

## SYNOPSIS
Обменивается VIP-решениями между двумя балансирными балансами нагрузки облачной службы (расширенной поддержки).

## СИНТАКСИС

### CloudServiceName (по умолчанию)
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Обменивается VIP-решениями между двумя балансирными балансами нагрузки облачной службы (расширенной поддержки).

## ПРИМЕРЫ

### Пример 1. Переключение облачной службы с использованием имени
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Команда выше вызывает операцию vipswap в облачной службе с именем "BService" и выполнит операцию, как только пользователь подтвердит действие в запросе на подтверждение.
"BService" с заменяемой облачной службой.

### Пример 2. Переключение облачной службы с помощью объекта облачной службы
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

Команда выше вызывает операцию vipswap в облачной службе с именем "BService" и выполнит операцию, как только пользователь подтвердит действие в запросе на подтверждение.
"BService" с заменяемой облачной службой.

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

### -Async


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

### -CloudService
Чтобы построить, см. раздел "Заметки" для свойств CLOUDSERVICE и создание таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
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

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: 
  - `Location <String>`: расположение ресурса.
  - `[Configuration <String>]`: определяет конфигурацию службы XML (CSCFG) для облачной службы.
  - `[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес. URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.         Это свойство является свойством только для записи и не возвращается при звонках GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.
    - `[Extension <IExtension[]>]`: Список расширений для облачной службы.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более высокого уровня, когда они становятся доступны.
      - `[ForceUpdateTag <String>]`Тег, чтобы принудительно применить предоставленные общедоступные и защищенные параметры.         Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.         Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.         Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет возможно повторное внедрение.
      - `[Name <String>]`: имя расширения.
      - `[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: имя издателя обработера расширений.
      - `[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения. Если свойство не указано или указано "*", расширение применяется для всех ролей в облачной службе.
      - `[Setting <String>]`: общедоступные параметры расширения. Для расширений JSON это параметры JSON. Для расширения XML (например, RDP) это параметр XML для расширения.
      - `[SourceVaultId <String>]`: ИД ресурса
      - `[Type <String>]`: тип расширения.
      - `[TypeHandlerVersion <String>]`: определяет версию расширения. Определяет версию расширения. Если этот элемент не указан или в качестве значения используется звездочка (*), используется последняя версия расширения. Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии. Если указан основной номер версии и небольшой номер версии (X.Y), будет выбрана конкретная версия расширения. Если указана версия, для экземпляра роли выполняется автоматическое обновление.
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
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: набор сертификатов, которые должны быть установлены на экземпляры ролей.
      - `[SourceVaultId <String>]`: ИД ресурса
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.
        - `[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.
  - `[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета службы в службе BLOB-бизнес. URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.         Это свойство является свойством только для записи и не возвращается при звонках GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.
      - `[Name <String>]`: название ресурса.
      - `[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.
      - `[SkuName <String>]`: название SKU. ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наномном устройстве в данный момент работает облачная служба, необходимо удалить и повторно создать облачную службу или вернуться к старым SKU.
      - `[SkuTier <String>]`: определяет уровень облачной службы. Возможные значения <br /><br /> **Стандартный** <br /><br /> **Базовая**
  - `[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания. Значение по `true` умолчанию: .         Если это так, модель обслуживания по-прежнему развертывается, но код не будет запускаться сразу. Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", после чего она будет запущена. С развернутой службы по-прежнему взимается плата, даже если она отключена.
  - `[Tag <ICloudServiceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы. При развертывании службы для обновления доменов выделяются экземпляры ролей. Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.         Возможные значения <br /><br />**Авто**<br /><br />**Вручную** <br /><br />**Одновременный**<br /><br />         Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain. Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.

## СВЯЗАННЫЕ ССЫЛКИ

