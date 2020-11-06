---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562527"
---
# Start-AzureRmSqlServerUpgrade

## КРАТКИй обзор
Запускает обновление сервера базы данных SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureRmSqlServerUpgrade** запускает обновление сервера базы данных SQL Azure версии 11 до версии 12.
Вы можете отслеживать ход выполнения обновления с помощью командлета Get-AzureRmSqlServerUpgrade.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление сервера
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Эта команда обновляет сервер с именем Server01, назначенный группе ресурсов TesourceGroup01.

### Пример 2: обновление сервера с помощью расписания и рекомендации по базе данных
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Первая команда создает время на пять минут в будущем с помощью командлета Get-Date.
Эта команда хранит дату в $ScheduleTime переменной.
Для получения дополнительных сведений введите `Get-Help Get-Date` .
Вторая команда создает объект **RecommendedDatabaseProperties** , а затем сохраняет этот объект в переменной $DatabaseMap.
Следующие три команды назначают значения свойствам объекта, хранящегося в $DatabaseMap.
Последняя команда обновляет существующий сервер с именем Server01 и версией 12,0.
Самое раннее время обновления — это пять минут после выполнения команды, как указано в переменной $ScheduleTime.
После обновления ContosoDB базы данных будет работать в стандартном выпуске и иметь уровень обслуживания объектив S0.

## ПАРАМЕТРЫ

### -DatabaseCollection
Задает массив объектов **RecommendedDatabaseProperties** , используемых этим командлетом для обновления сервера.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
Задает массив объектов **UpgradeRecommendedElasticPoolProperties** , которые нужно использовать для обновления сервера.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен сервер.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
Задает самое раннее время в качестве объекта **DateTime** , чтобы обновить сервер.
Укажите значение в формате ISO8601 в всеобщем скоординированном времени (UTC).
Для получения дополнительных сведений введите `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера, который обновляется этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Указывает версию, на которую этот командлет обновляет сервер.
Единственным допустимым значением является 12,0.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Остановить-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


