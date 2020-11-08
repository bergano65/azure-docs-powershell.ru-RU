---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: aa8dde2683dcc939bb84e9f2026131cd8cc15b1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073600"
---
# Add-AzLogProfile

## КРАТКИй обзор
Создание нового профиля журнала активности. Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке. 

## Максимальное

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzLogProfile** создает профиль журнала.
- **Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения. Возможно, он либо имеет тип ARM, либо классический. Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение. На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку. 
- **Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку. Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий. В журнале активности события могут относиться к региону или быть "глобальным". Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию. Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе. При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона. 
**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.** Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление нового профиля журнала для экспорта журнала активности, соответствующего условию расположения, в учетной записи хранения
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## ПАРАМЕТРЫ

### -Категория
Указывает список категорий.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Location
Указывает расположение профиля журнала.
Допустимые значения. чтобы получить актуальный список расположений, выполните указанные ниже командлеты. Get-AzLocation | Выберите DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя профиля.

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

### -RetentionInDays
Указывает политику хранения в днях. Количество дней, в течение которых журналы сохраняются в указанной учетной записи хранения. Чтобы сохранить данные в неизменном виде, установите для него значение **0**. Если он не указан, по умолчанию используется значение **0**. Для хранения данных обычно применяются нормы выставления счетов в стандартном хранилище или центрах событий.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Указывает идентификатор правила служебной шины.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Указывает идентификатор учетной записи хранения. Идентификатор — это полный ИД ресурса для учетной записи хранения, например  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


