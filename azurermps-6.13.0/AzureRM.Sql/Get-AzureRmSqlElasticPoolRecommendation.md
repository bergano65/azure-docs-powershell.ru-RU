---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 0769824bc0b50641f7b73cb530dde0a5f30bf7ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563971"
---
# Get-AzureRmSqlElasticPoolRecommendation

## КРАТКИй обзор
Получение рекомендаций пула эластичных БД.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmSqlElasticPoolRecommendation** получает рекомендации пула эластичных БД для сервера.
Эти рекомендации включают следующие значения:
- DatabaseCollection. Коллекция имен баз данных, которые принадлежат пулу. 
- DatabaseDtuMin. Гарантируется наличие модуля передачи данных (DTU) для баз данных в пуле эластичных БД. 
 -- DatabaseDtuMax. Ограничение DTU для баз данных в пуле эластичных БД. 
- Дополнительную. Гарантия DTU для эластичного пула. 
- StorageMb. Хранилище в мегабайтах для эластичного пула. 
- Ознакомитель. Выпуск для пула эластичных БД. Допустимые значения этого параметра: Basic, Standard и Premium. 
- IncludeAllDatabases. Указывает, должны ли возвращаться все базы данных в пуле эластичных БД. 
- Псевдоним. Имя эластичного пула.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение рекомендаций для сервера
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Эта команда получает рекомендации пула эластичных БД для сервера с именем Server01.

## ПАРАМЕТРЫ

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

### -ИмяСервера
Указывает имя сервера, для которого этот командлет получает рекомендации.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
