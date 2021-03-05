---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002488"
---
# New-AzStorageContext

## SYNOPSIS
Создает контекст хранилища Azure.

## СИНТАКСИС

### OAuthAccount (по умолчанию)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### Local Темы
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания контекста хранилища Azure создается **cmdlet New-AzStorageContext.**
По умолчанию для контекста хранилища задана проверка подлинности OAuth (Azure AD), если она называется только входной учетной записью хранилища.
Подробные сведения о проверке подлинности службы хранилища см. в https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services .

## ПРИМЕРЫ

### Пример 1. Создание контекста путем указания имени учетной записи хранения и ключа
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.

### Пример 2. Создание контекста путем указания строки подключения
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.

### Пример 3. Создание контекста для анонимной учетной записи хранения
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Эта команда создает контекст для анонимного использования учетной записи ContosoGeneral.
Команда определяет HTTP как протокол подключения.

### Пример 4. Создание контекста с помощью локальной учетной записи хранилища разработки
```
PS C:\>New-AzStorageContext -Local
```

Эта команда создает контекст с использованием локальной учетной записи хранилища разработки.
Команда определяет *локальный* параметр.

### Пример 5. Получить контейнер для локальной учетной записи разработчика
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Эта команда создает контекст с использованием локальной учетной записи хранилища разработки, а затем передает новый контекст **командлету Get-AzStorageContainer** с помощью оператора конвейера.
Команда получает контейнер хранилища Azure для локальной учетной записи разработчика.

### Пример 6. Получите несколько контейнеров
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Первая команда создает контекст с использованием локальной учетной записи хранилища разработки, а затем сохраняет его в переменной $Context 01.
Вторая команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ, а затем сохраняет этот контекст в переменной $Context 02.
Конечная команда получает контейнеры контекстов, хранимых в $Context 01 и $Context 02, с помощью **Get-AzStorageContainer.**

### Пример 7. Создание контекста с конечной точкой
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Эта команда создает контекст хранилища Azure с указанной конечной точкой хранилища.
Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.

### Пример 8. Создание контекста с определенной средой
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Эта команда создает контекст хранилища Azure с указанной средой Azure.
Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ.

### Пример 9. Создание контекста с помощью маркера SAS
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Первая команда создает токен SAS с помощью командлета **New-AzStorageContainerSASToken** для контейнера ContosoMain, а затем сохраняет его в переменной $SasToken.
Этот маркер для разрешений на чтение, добавление, обновление и удаление.
Вторая команда создает контекст для учетной записи ContosoGeneral, использующей маркер SAS из $SasToken, а затем сохраняет этот контекст в переменной $Context.
В конечной команде перечислены все BLOB-lob-lob, связанные с контейнером ContosoMain, используя контекст, $Context.

### Пример 10. Создание контекста с помощью проверки подлинности OAuth
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Эта команда создает контекст с помощью проверки подлинности OAuth (Azure AD).

## PARAMETERS

### -Анонимный
Указывает на то, что этот cmdlet создает контекст хранилища Azure для анонимного логотипа.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Указывает строку подключения для контекста хранилища Azure.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Конечная точка
Указывает конечную точку для контекста хранилища Azure.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Среда
Указывает среду Azure.
Допустимыми значениями для этого параметра являются AzureCloud и AzureChinaCloud.
Для получения дополнительных сведений введите `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Указывает на то, что этот cmdlet создает контекст с использованием локальной учетной записи хранилища разработки.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Передача протокола (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Указывает маркер подписи общего доступа (SAS) для контекста.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Указывает ключ учетной записи хранилища Azure.
Этот cmdlet создает контекст для ключа, указанного этим параметром.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя учетной записи хранилища Azure.
Этот cmdlet создает контекст для учетной записи, указанной этим параметром.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Указывает на то, что этот cmdlet создает контекст хранилища Azure с проверкой подлинности OAuth (Azure AD).
По умолчанию для этого используется проверка подлинности OAuth, если не указана другая проверка подлинности.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


