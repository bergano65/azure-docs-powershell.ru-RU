---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404179"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Создает контекст подключения к серверу.

## СИНТАКСИС

### ByServerNameWithSqlAuth (по умолчанию)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания контекста подключения к серверу базы данных Azure SQL Azure **создается cmdlet New-AzureSqlDataBaseServerContext.**
Используйте SQL Server проверки подлинности для создания контекста подключения к серверу SQL базы данных с использованием указанных учетных данных.
Вы можете указать SQL базы данных по имени, по полному имени или по URL-адресу.
Чтобы получить учетные данные, Get-Credential вводить имя пользователя и пароль с помощью Get-Credential.

С помощью cmdlet **New-AzureSqlDataBaseServerContext** с проверкой подлинности на основе сертификата создайте контекст подключения к указанному серверу базы данных SQL, используя указанные данные подписки Azure.
Вы можете указать SQL базы данных по имени или по полному имени.
Вы можете указать данные подписки в качестве параметра или получить их из текущей подписки Azure.
С помощью cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx выберите текущую подписку Azure.

## ПРИМЕРЫ

### Пример 1. Создание контекста с помощью проверки SQL Server подлинности
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

В этом примере используется SQL Server проверки подлинности.

Первая команда запросит учетные данные администратора сервера, а затем за нее будет $Credential переменную.

Вторая команда подключается к серверу SQL базы данных lpqd0zbr8y с помощью $Credential.

Конечная команда создает на сервере базу данных с именем Database17, которая входит в контекст $Context.

### Пример 2. Создание контекста с помощью проверки подлинности на основе сертификата
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

В этом примере используется проверка подлинности на основе сертификата.

Первые две команды присваивают значения $SubscriptionId и $Thumbprint переменным.

Третья команда получает сертификат, который определился с помощью $Thumbprint, и сохраняет его в $Certificate.

Четвертая команда задает подписку на Subscription07, а пятая выбирает ее.

Конечная команда создает контекст в текущей подписке для сервера с именем lpqd0zbr8y.

## PARAMETERS

### -Credential
Определяет объект учетных данных, SQL Server проверку подлинности для доступа к серверу.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Указывает полное доменное имя для сервера базы данных Azure SQL.
Например, Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Url-адрес, который этот cmdlet использует для доступа к порталу управления базами SQL Azure для сервера.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

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

### -ServerName
Имя сервера базы данных.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Указывает имя подписки Azure, которую этот cmdlet использует для создания контекста подключения.
Если значение для этого параметра не задано, используется текущая подписка.
Запустите Select-AzureSubscription, чтобы изменить текущую подписку.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Указывает на то, что для создания контекста подключения используется подписка Azure.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## OUTPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## ПРИМЕЧАНИЯ
* Если проверка подлинности проводится без указания домена, а также при использовании Windows PowerShell 2.0, Get-Credential-редактор возвращает зашлывку (), предшеную имени пользователя, например \\ \user. Windows PowerShell 3.0 не добавляет обратное слаш. Эта backslash не распознается параметром *Credential* в cmdlet **New-AzureSqlDatabaseServerContext.** Чтобы удалить его, используйте следующие команды:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## СВЯЗАННЫЕ ССЫЛКИ



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


