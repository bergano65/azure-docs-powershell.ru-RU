---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560383"
---
# New-AzureRmDataMigrationConnectionInfo

## КРАТКИй обзор
Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## NОПИСАНИЕ
Командлет New-AzureRmDataMigrationConnectionInfo создает новый объект сведений о соединении, указывающий тип сервера для подключения. 



## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
В предыдущем примере создается объект сведений о соединении, предоставляющий SQL AS для параметра ServerType.


## ПАРАМЕТРЫ

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerType
Enum, описывающий тип сервера для подключения. В настоящее время поддерживаются значения SQL для SQL Server и SQLDB для базы данных SQL Azure. 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -AuthType
Тип проверки подлинности, который будет использоваться для подключения. Возможные значения — SqlAuthentication и WindowsAuthentication

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataSource
Сервер address\name, к которому нужно подключиться. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustServerCertificate
Логическое значение, указывающее, что шифрование будет происходить.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## ВХОДНЫЕ данные

### Ничего


## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. Migration. Models. ConnectionInfo


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

