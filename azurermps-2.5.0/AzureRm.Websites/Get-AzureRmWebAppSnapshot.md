---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913413"
---
# Get-AzureRmWebAppSnapshot

## КРАТКИй обзор
Получает снимки, доступные для веб-приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### FromResourceName
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### FromWebApp
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmWebAppSnapshot** возвращает все снимки для веб-приложения. Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения. Снимок можно восстановить с помощью командлета **RESTORE-AzureRmWebAppSnapshot** .

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

Получение моментальных снимков для веб-приложения с именем "ConstosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"

## ПАРАМЕТРЫ

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

### -Name (имя)
Имя веб-приложения.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Имя области веб-приложения.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
Объект веб-приложения

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### System. String
Microsoft. Azure. Management. website. Models. site


## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

