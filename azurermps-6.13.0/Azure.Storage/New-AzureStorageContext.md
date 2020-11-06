---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566019"
---
# New-AzureStorageContext

## КРАТКИй обзор
Создает контекст хранилища Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### OAuthAccount (по умолчанию)
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### Подключения
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageContext** создает контекст хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание контекста с указанием имени и ключа учетной записи хранения
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ.

### Пример 2: создание контекста путем указания строки соединения
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.

### Пример 3: создание контекста для анонимной учетной записи хранения
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Эта команда создает контекст для анонимного использования учетной записи с именем ContosoGeneral.
Команда указывает HTTP как протокол подключения.

### Пример 4: создание контекста с помощью локальной учетной записи хранения для разработки
```
C:\PS>New-AzureStorageContext -Local
```

Эта команда создает контекст с помощью локальной учетной записи хранения разработки.
Команда задает *локальный* параметр.

### Пример 5: получение контейнера для локальной учетной записи хранения разработчика
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Эта команда создает контекст с помощью локальной учетной записи хранения разработки, а затем передает новый контекст командлету **Get-AzureStorageContainer** с помощью оператора конвейера.
Команда получает контейнер хранилища Azure для локальной учетной записи хранилища разработчика.

### Пример 6: получение нескольких контейнеров
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

Первая команда создает контекст с помощью локальной учетной записи хранения разработки и сохраняет этот контекст в переменной $Context 01.
Вторая команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот контекст в переменной $Context 02.
Последняя команда получает контейнеры для контекстов, которые хранятся в $Context 01 и $Context 02 с помощью **Get-AzureStorageContainer**.

### Пример 7: создание контекста с конечной точкой
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Эта команда создает контекст хранилища Azure, который содержит указанную конечную точку хранилища.
Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.

### Пример 8: создание контекста с указанной средой
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Эта команда создает контекст хранилища Azure, который содержит указанную среду Azure.
Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.

### Пример 9: создание контекста с помощью маркера SAS
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

Первая команда создает маркер SAS с помощью командлета **New-AzureStorageContainerSASToken** для контейнера с именем ContosoMain и сохраняет этот маркер в переменной $SasToken.
Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.
Вторая команда создает контекст для учетной записи с именем ContosoGeneral, который использует маркер SAS, хранящийся в $SasToken, и сохраняет этот контекст в переменной $Context.
В последней команде перечисляются все BLOB-объекты, связанные с контейнером с именем ContosoMain, используя контекст, хранящийся в $Context.

### Пример 10: создание контекста с использованием проверки подлинности OAuth
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Эта команда создает контекст с использованием проверки подлинности OAuth.

## ПАРАМЕТРЫ

### -Анонимный
Указывает на то, что этот командлет создает контекст хранилища Azure для анонимного входа.

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

### -Endpoint
Задает конечную точку контекста хранилища Azure.

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

### -Environment
Указывает среду Azure.
Допустимые значения этого параметра: AzureCloud и AzureChinaCloud.
Для получения дополнительных сведений введите `Get-Help Get-AzureEnvironment` .

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
Указывает на то, что этот командлет создает контекст с помощью локальной учетной записи хранения разработки.

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

### -Protocol (протокол)
Протокол передачи (HTTPS/HTTP).

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
Указывает маркер общего доступа к подписи (SAS) для контекста.

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
Указывает ключ учетной записи хранения Azure.
Этот командлет создает контекст для ключа, указывающего на этот параметр.

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
Указывает имя учетной записи службы хранилища Azure.
Этот командлет создает контекст для учетной записи, которую указывает этот параметр.

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
Указывает на то, что этот командлет создает контекст хранилища Azure с проверкой подлинности OAuth.
По умолчанию командлет использует проверку подлинности OAuth, если другие anthentication не указаны.

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Указывает на то, что этот командлет создает контекст хранилища Azure с проверкой подлинности OAuth.
По умолчанию командлет использует проверку подлинности OAuth, если другие anthentication не указаны.

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


