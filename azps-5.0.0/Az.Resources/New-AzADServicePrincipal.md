---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "94319472"
---
# New-AzADServicePrincipal

## КРАТКИй обзор
Создание нового субъекта-службы Azure Active Directory.

## Максимальное

### SimpleParameterSet (по умолчанию)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ

Создание нового субъекта-службы Azure Active Directory. Параметр по умолчанию использует значения по умолчанию для параметров, если они не заданы. Дополнительные сведения о значениях по умолчанию можно найти в описании каждого параметра. Этот командлет может назначать роль субъекту-службы с параметрами **роли** и **области** . Если оба аргумента опущены, роль участника назначается участнику службы. Значения по умолчанию для **роли** и параметров **области** являются **сотрудниками** текущей подписки. Командлет создает приложение и задает его свойства, если не задано значение ApplicationId. Чтобы обновить параметры, зависящие от приложения, используйте командлет [Update-AzADApplication](./update-azadapplication.md) .

> [!WARNING]
> Когда вы создаете участника службы с помощью команды **New-AzADServicePrincipal** , выходные данные включают учетные данные, которые необходимо защитить. Убедитесь в том, что эти учетные данные не включены в код, или проверьте учетные данные в системе управления версиями. В качестве альтернативы можно использовать [управляемые удостоверения](/azure/active-directory/managed-identities-azure-resources/overview) , чтобы избежать необходимости использовать учетные данные.
>
> По умолчанию в разделе **New-AzADServicePrincipal** назначается [роль "участник"](/azure/role-based-access-control/built-in-roles#contributor) для субъекта-службы в области подписки. Чтобы уменьшить риск скомпрометированного субъекта-службы, назначайте более конкретные роли и ограничьте область ресурсом или группой ресурсов. Дополнительные сведения [можно найти в разделе инструкции по добавлению назначения роли](/azure/role-based-access-control/role-assignments-steps) .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание участника простой службы AD

В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны. Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы. Так как для **роли** или **области** не предоставлены значения, созданному участнику службы назначается роль **участника** для текущей подписки.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Пример 2: Создание участника простой службы AD с указанной ролью и областью по умолчанию

В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны. Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы. Субъект-служба создается с разрешениями на **Чтение** для текущей подписки, так как для параметра **Scope** не задано значение.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### Пример 3: Создание участника простой службы AD с заданной областью и ролью по умолчанию

В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны. Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы. Субъект-служба создается с разрешениями **участника** для указанной области группы ресурсов, так как для параметра **Role** не задано значение.

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Пример 4: Создание участника простой службы AD с указанной областью и ролью

В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны. Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы. Субъект-служба создается с разрешениями на **Чтение** для указанной области группы ресурсов.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Пример 5: Создание участника службы AD с помощью идентификатора приложения с назначением роли

В следующем примере создается субъект-служба AD для приложения с ИДЕНТИФИКАТОРом приложения "00000000-0000-0000-0000-000000000000". Так как для **роли** или **области** не предоставлены значения, созданному участнику службы назначается роль **участника** для текущей подписки.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Пример 6: создание нового участника службы AD с помощью конвейера

В следующем примере извлекается приложение с ИДЕНТИФИКАТОРом объекта "3ede3c26-b443-4e0b-9efc-b05e68338dc3" с помощью командлета [Get-AzADApplication](./get-azadapplication.md) . Результаты будут переданы `New-AzADServicePrincipal` командлету для создания нового субъекта-службы для этого приложения.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Пример 7: Создание участника службы AD с использованием DisplayName и учетных данных пароля

В следующем примере создается новое приложение **с именем "** имя для" и пароль для **StrongPassworld! 23**. Он создает субъект-службу на основе созданного приложения. Дата начала и Дата окончания добавляются в учетные данные пароля.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### Пример 8: создание субъекта-службы AD с использованием учетных данных DisplayName и открытого ключа

В следующем примере создается новое приложение **с именем "** имя программного кода" и **$certом** сертификата. Он создает участника службы на основе созданного приложения. Дата окончания добавляется к учетным данным ключа.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## ПАРАМЕТРЫ

### -ApplicationId

Уникальный идентификатор приложения для субъекта-службы в клиенте. После создания это свойство невозможно изменить. Если идентификатор приложения для существующего приложения не указан, создается приложение.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

Объект, представляющий приложение, для которого создается субъект-служба.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Значение типа асимметричных учетных данных. Он представляет сертификат в кодировке Base64.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
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

### -DisplayName

Понятное имя субъекта-службы. Если отображаемое имя не указано, это значение будет использоваться по умолчанию для **Azure-PowerShell-mm-дд-гггг-чч-мм-SS** , где этот суффикс является временем создания приложения.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

Эффективная дата окончания использования учетных данных. Значение даты окончания по умолчанию — это год от сегодняшнего дня.
Для учетных данных асимметричного типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential

Коллекция ключевых учетных данных, связанных с приложением.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

Коллекция учетных данных пароля, связанных с приложением.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role (роль)

Роль, которую участник службы имеет над областью. Если значение не задано, **по умолчанию используется** роль **участника** .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

Область, для которой у субъекта-службы есть разрешения. Если значение не задано, **по** умолчанию используется текущая подписка.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment

Если задано, пропускать создание назначения роли по умолчанию для субъекта-службы.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate

Фактическая дата начала использования учетных данных. Значение даты начала по умолчанию — сегодня. Для учетных данных асимметричного типа это значение должно быть установлено на on или после даты, с которой сертификат X509 является действительным.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Запрашивает подтверждение перед запуском командлета.

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

Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).
## ВХОДНЫЕ данные

### System. GUID

### System. String

### Microsoft. Azure. Commands. ActiveDirectory. PSADApplication

### Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []

### Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []

### System. DateTime

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal

### Microsoft. Azure. Commands. Resources. Authorization. PSADServicePrincipalWrapper

## Пуск

Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)