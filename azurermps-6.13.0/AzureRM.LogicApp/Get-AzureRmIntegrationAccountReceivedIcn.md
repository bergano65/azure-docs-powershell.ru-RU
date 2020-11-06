---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: b9defadc92619d136c82302203d296d6b71318ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562976"
---
# Get-AzureRmIntegrationAccountReceivedIcn

## КРАТКИй обзор
Этот командлет извлекает конкретный номер полученного элемента управления обменом для каждого соглашения и значения Control Number.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Этот командлет предназначен для использования в сценариях аварийного восстановления для проверки наличия полученного номера управления обменом и, при необходимости, для удаления этого объекта с помощью Remove-AzureRmIntegrationAccountReceivedIcn.
Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

Эта команда получает учетную запись интеграции X12, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.

### Пример 2
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

Эта команда получает учетную запись интеграции EDIFACT, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.

## ПАРАМЕТРЫ

### -AgreementName
Имя соглашения для учетной записи интеграции.

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

### -AgreementType
Тип соглашения для учетной записи интеграции.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNumberValue
Значение номера контроля учетной записи интеграции.

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

### -Name (имя)
Имя учетной записи интеграции.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов для учетной записи интеграции.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
