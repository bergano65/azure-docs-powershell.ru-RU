---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396212"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Шифрует конфиденциальные данные.

## СИНТАКСИС

### ByFactoryName (По умолчанию)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet New-AzDataFactoryEncryptValue** шифрует конфиденциальные данные, такие как пароль или Microsoft SQL Server подключения, и возвращает зашифрованное значение.

## ПРИМЕРЫ

### Пример 1. Шифрование строки подключения, не ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Первая команда использует ConvertTo-SecureString для преобразования указанной строки подключения в объект **SecureString,** а затем сохраняет этот объект в $Value переменной.
Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .
Разрешенные значения: SQL Server или строка подключения Oracle.
Вторая команда создает зашифрованное значение для объекта, храняого в $Value для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.

### Пример 2. Шифрование строки подключения, не относяскойся к ODBC, с использованием проверки подлинности Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки подключения в объект безопасной строки, а затем сохраняет этот объект в переменной $Value.
Вторая команда использует Get-Credential для сбора проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет объект **PSCredential** в переменной $Credential.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .
Третья команда создает зашифрованное значение для объекта, который хранится в $Value и $Credential для указанной фабрики данных, шлюза, группы ресурсов и связанного типа службы.

### Пример 3. Шифрование имени сервера и учетных данных для связанной службы файловой системы
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки в безопасную строку, а затем сохраняет объект в $Value переменной.
Вторая команда использует **get-Credential** для сбора проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет объект **PSCredential** в $Credential переменной.
Третья команда создает зашифрованное значение для объекта, который хранится в $Value и $Credential для указанной фабрики данных, шлюза, группы ресурсов и связанного типа службы.

### Пример 4. Шифрование учетных данных для связанной службы HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.
Команда **"Создать объект"** создает объект PSCredential, используя строки защищенного имени пользователя и пароля.
Вместо этого можно использовать команду **Get-Credential** для сбора проверки подлинности Windows (имени пользователя и пароля), а затем сохранить возвращенный **объект PSCredential** в переменной $credential, как показано в предыдущих примерах.
Команда **New-AzDataFactoryEncryptValue** создает зашифрованное значение для объекта, храняого в $Credential для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.

### Пример 5. Шифрование учетных данных для связанной службы ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.
Команда **New-AzDataFactoryEncryptValue** создает зашифрованное значение для объекта, храняого в $Value для указанного фабрики данных, шлюза, группы ресурсов и связанного типа службы.

## PARAMETERS

### -AuthenticationType
Определяет тип проверки подлинности, которая будет использоваться для подключения к источнику данных.
Допустимыми значениями для этого параметра являются:
- Windows
- Базовая
- Анонимный.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Определяет учетные данные для проверки подлинности Windows (имя пользователя и пароль), которые нужно использовать.
Этот cmdlet шифрует учетные данные, которые вы здесь указали.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Указывает имя базы данных связанной службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Указывает объект **PSDataFactory.**
Этот cmdlet шифрует данные для фабрики данных, указанной этим параметром.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Название фабрики данных.
Этот cmdlet шифрует данные для фабрики данных, указанной этим параметром.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -GatewayName
Указывает имя шлюза.
Этот cmdlet шифрует данные шлюза, указанные этим параметром.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Указывает часть подключения ODBC, которая не является частью подключения к базе данных без учетных данных.
Этот параметр действует только для связанной службы ODBC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов Azure.
Этот cmdlet шифрует данные для группы, указанной этим параметром.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Указывает имя сервера связанной службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Указывает связанный тип службы.
Этот cmdlet шифрует данные для связанного типа службы, указанного этим параметром.
Допустимыми значениями для этого параметра являются:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Указывает значение для шифрования.
Для локальной службы SQL Server и связанной службы Oracle используйте строку подключения.
Для локальной связанной службы ODBC используйте часть учетных данных строки подключения.
Если файловая система локально подключена к компьютеру шлюза, используйте local or localhost, а если файловая система находится на сервере, другом компьютере шлюза, используйте имя \\ \\ сервера.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


