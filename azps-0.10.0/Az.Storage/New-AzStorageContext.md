---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910731"
---
# New-AzStorageContext

## КРАТКИй обзор
Создает контекст хранилища Azure.

## Максимальное

### AccountNameAndKey (по умолчанию)
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

### Подключения
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzStorageContext** создает контекст хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание контекста с указанием имени и ключа учетной записи хранения
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ.

### Пример 2: создание контекста путем указания строки соединения
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Эта команда создает контекст на основе указанной строки подключения для учетной записи ContosoGeneral.

### Пример 3: создание контекста для анонимной учетной записи хранения
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Эта команда создает контекст для анонимного использования учетной записи с именем ContosoGeneral.
Команда указывает HTTP как протокол подключения.

### Пример 4: создание контекста с помощью локальной учетной записи хранения для разработки
```
C:\PS>New-AzStorageContext -Local
```

Эта команда создает контекст с помощью локальной учетной записи хранения разработки.
Команда задает *локальный* параметр.

### Пример 5: получение контейнера для локальной учетной записи хранения разработчика
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

Эта команда создает контекст с помощью локальной учетной записи хранения разработки, а затем передает новый контекст командлету **Get-AzStorageContainer** с помощью оператора конвейера.
Команда получает контейнер хранилища Azure для локальной учетной записи хранилища разработчика.

### Пример 6: получение нескольких контейнеров
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Первая команда создает контекст с помощью локальной учетной записи хранения разработки и сохраняет этот контекст в переменной $Context 01.
Вторая команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот контекст в переменной $Context 02.
Последняя команда получает контейнеры для контекстов, которые хранятся в $Context 01 и $Context 02 с помощью **Get-AzStorageContainer**.

### Пример 7: создание контекста с конечной точкой
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Эта команда создает контекст хранилища Azure, который содержит указанную конечную точку хранилища.
Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.

### Пример 8: создание контекста с указанной средой
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Эта команда создает контекст хранилища Azure, который содержит указанную среду Azure.
Команда создает контекст для учетной записи с именем ContosoGeneral, которая использует указанный ключ.

### Пример 9: создание контекста с помощью маркера SAS
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Первая команда создает маркер SAS с помощью командлета **New-AzStorageContainerSASToken** для контейнера с именем ContosoMain и сохраняет этот маркер в переменной $SasToken.
Этот маркер предназначен для чтения, добавления, обновления и удаления разрешений.
Вторая команда создает контекст для учетной записи с именем ContosoGeneral, который использует маркер SAS, хранящийся в $SasToken, и сохраняет этот контекст в переменной $Context.
В последней команде перечисляются все BLOB-объекты, связанные с контейнером с именем ContosoMain, используя контекст, хранящийся в $Context.

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
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
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
Parameter Sets: SasTokenWithAzureEnvironment
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
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
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
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


