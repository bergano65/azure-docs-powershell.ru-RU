---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562200"
---
# Get-AzureRmADGroup

## КРАТКИй обзор
Фильтрует группы Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### EmptyParameterSet (по умолчанию)
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Фильтрует группы Active Directory.

## ИЛЛЮСТРИРУЮТ

### --------------------------Группы фильтров с использованием идентификатора объекта--------------------------
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

Получает группу с ИД 85F89C90-780E-4AA6-9F4F-6F268D322EEE

### --------------------------Группы фильтров с помощью строки поиска--------------------------
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

Фильтрует все группы баннеров, в отображаемом имени которых есть Joe.

### --------------------------Групп рекламы--------------------------
```
PS C:\> Get-AzureRmADGroup
```

Получает все группы Active Directory

## ПАРАМЕТРЫ

### -ObjectId
Идентификатор объекта группы.

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
Отображаемое имя группы

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmADUser](./Get-AzureRmADUser.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

[Get-AzureRmADGroupMember](./Get-AzureRmADGroupMember.md)

