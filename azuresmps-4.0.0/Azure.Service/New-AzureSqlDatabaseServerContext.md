---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075970"
---
# New-AzureSqlDatabaseServerContext

## КРАТКИй обзор
Создает контекст подключения сервера.

## Максимальное

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

## NОПИСАНИЕ
Командлет **New-AzureSqlDatabaseServerContext** создает контекст подключения к серверу базы данных SQL Azure.
Использование проверки подлинности SQL Server для создания контекста подключения к серверу базы данных SQL с использованием указанных учетных данных.
Вы можете указать сервер базы данных SQL по имени, по полному имени или по URL-адресу.
Чтобы получить учетные данные, используйте командлет Get-Credential, который предлагает указать имя пользователя и пароль.

Используйте командлет **New-AzureSqlDatabaseServerContext** с проверкой подлинности на основе сертификатов для создания контекста подключения к указанному серверу базы данных SQL, используя указанные данные подписки Azure.
Сервер базы данных SQL можно указать по имени или по полному имени.
Вы можете указать данные подписки в качестве параметра или получить их из текущей подписки Azure.
С помощью командлета Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx выберите текущую подписку Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание контекста с использованием проверки подлинности SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

В этом примере используется проверка подлинности SQL Server.

В первой команде вам будет предложено ввести учетные данные администратора сервера и сохранить учетные данные в переменной $Credential.

Вторая команда подключается к серверу базы данных SQL с именем lpqd0zbr8y с помощью $Credential.

Последняя команда создает базу данных с именем Database17 на сервере, который является частью контекста в $Context.

### Пример 2: создание контекста с использованием проверки подлинности на основе сертификатов
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

В этом примере используется проверка подлинности на основе сертификата.

Первые две команды назначают значения для переменных $SubscriptionId и $Thumbprint.

Третья команда получает сертификат, идентифицированный отпечатком, в $Thumbprint и сохраняет его в $Certificate.

Четвертая команда устанавливает подписку на Subscription07, а пятая команда выбирает эту подписку.

Последняя команда создает контекст в текущей подписке для сервера с именем lpqd0zbr8y.

## ПАРАМЕТРЫ

### -Credential
Указывает объект учетных данных, который обеспечивает проверку подлинности SQL Server для доступа к серверу.

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
Указывает полное доменное имя (FQDN) для сервера базы данных SQL Azure.
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
Указывает URL-адрес, используемый этим командлетом для доступа к порталу SQL DatabaseManagement Azure для сервера.

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

### -ИмяСервера
Указывает имя сервера базы данных.

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
Указывает имя подписки Azure, которую этот командлет использует для создания контекста подключения.
Если значение для этого параметра не задано, командлет использует текущую подписку.
Запустите командлет Select-AzureSubscription, чтобы изменить текущую подписку.

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
Указывает на то, что этот командлет использует подписку Azure для создания контекста подключения.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. IServerDataServiceContext

## Пуск
* Если при проверке подлинности не указан домен и вы используете Windows PowerShell 2,0, командлет Get-Credential Возвращает обратную косую черту ( \\ ) в начале имени пользователя (например, \USER.). В Windows PowerShell 3,0 обратная косая черта не добавляется. Эта обратная косая черта не распознается параметром *Credential* командлета **New-AzureSqlDatabaseServerContext** . Чтобы удалить его, используйте команды, похожие на приведенные ниже.

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Командлеты базы данных SQL Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


