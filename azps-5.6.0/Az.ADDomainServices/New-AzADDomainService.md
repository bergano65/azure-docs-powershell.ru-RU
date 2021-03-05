---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986320"
---
# New-AzADDomainService

## SYNOPSIS
В ходе операции создания службы домена создается новая служба домена с указанными параметрами.
Если определенная служба уже существует, все свойства, которые можно в обновлении, будут обновлены и неизменяемые свойства останутся без изменений.

## СИНТАКСИС

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
В ходе операции создания службы домена создается новая доменная служба с указанными параметрами.
Если определенная служба уже существует, все исправления будут обновлены и неизменяемые свойства останутся без изменений.

## ПРИМЕРЫ

### Пример 1. Создание новой службы ADDomainService
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

Создание ADDomainService

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

### -DomainConfigurationType
Тип конфигурации домена

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

### -DomainName
Имя домена Azure, для которого пользователь хочет развернуть доменные службы.

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

### -DomainSecuritySettingNtlmV1
Флажок для определения того, включена ли NtlmV1.

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

### -DomainSecuritySettingSyncKerberosPassword
Флаг для определения того, включена ли синхронизацияPasswords SyncKerberosPasswords.

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

### -DomainSecuritySettingSyncNtlmPassword
Флаг для определения того, включена ли синхронизация SyncNtlmPasswords.

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

### -DomainSecuritySettingSyncOnPremPassword
Флаг для определения того, включена ли синхронизацияOnPremPasswords.

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

### -DomainSecuritySettingTlsV1
Флажок для определения того, включена ли TlsV1.

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

### -FilteredSync
Включена или отключена пометка для включения отфильтрованной синхронизации с группировкой

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

### -ForestTrust
Список параметров для строительства леса ресурсов. См. раздел "ПРИМЕЧАНИЯ" для свойств FORESTTRUST и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapSettingExternalAccess
Флажок для определения того, включен ли безопасный доступ LDAP через Интернет.

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

### -LdapSettingLdaps
Флаг для определения того, включена ли защита LDAP.

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

### -LdapSettingPfxCertificate
Сертификат, необходимый для настройки Secure LDAP.
Параметр, переданный здесь, должен быть основанием64encoded представления pfx-файла сертификата.

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

### -LdapSettingPfxCertificatePassword
Пароль для расшифровки предоставленного PFX-файла сертификата LDAP.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя службы домена.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationSettingAdditionalRecipient
Список дополнительных получателей

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationSettingNotifyDcAdmin
Следует ли уведомить администраторов контроллера домена

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

### -NotificationSettingNotifyBalAdmin
Должны ли глобальные администраторы быть уведомлены

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

### -ReplicaSet
Список наборов реплик для сстройки, см. раздел "ЗАМЕТКИ" для свойств REPLICASET и создание таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceForest
Лес ресурсов

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
Имя группы ресурсов в подписке пользователя.
Имя нечувствительно к делу.

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

### -SKU
Тип SKU

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

### -SubscriptionId
Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.
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
Теги ресурсов

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

### Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


FORESTTRUST <IForestTrust[]>: список параметров для леса ресурсов
  - `[FriendlyName <String>]`: Удобное имя
  - `[RemoteDnsIP <String>]`: Remote DNS ips
  - `[TrustDirection <String>]`: Trust Direction
  - `[TrustPassword <String>]`: Trust Password
  - `[TrustedDomainFqdn <String>]`: Trusted Domain FQDN

REPLICASET <IReplicaSet[]>: список реплик
  - `[Location <String>]`: расположение в виртуальной сети
  - `[SubnetId <String>]`. Название виртуальной сети, в которую будут развернуты доменные службы. Id подсеть, в которую будут развернуты доменные службы. /virtualNetwork/vnetName/subnets/subnetName.

## СВЯЗАННЫЕ ССЫЛКИ

