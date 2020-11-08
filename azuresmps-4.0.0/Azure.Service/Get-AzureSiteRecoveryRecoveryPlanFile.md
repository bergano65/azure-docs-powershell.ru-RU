---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075583"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## КРАТКИй обзор
Загружает план восстановления сайта Azure в формате XML.

## Максимальное

### ByRPObject (по умолчанию)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSiteRecoveryRecoveryPlanFile** загружает план восстановления сайта Azure в формате XML.
Вы можете использовать этот файл, чтобы обновить план восстановления, а затем отправить его на сервер восстановления сайта.

План восстановления собирает виртуальные машины в группе в целях перемещения при сбое и восстановления.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение файла плана восстановления
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Эта команда использует командлет **Get-AzureSiteRecoveryRecoveryPlan** для получения плана восстановления и сохраняет его в переменной $RecoveryPlan.

Вторая команда использует командлет **GetAzureSiteRecoveryRecoveryPlanFile** для получения XML-файла плана восстановления сайта в $RecoveryPlan.
Команда сохраняет XML-файл по указанному пути.

## ПАРАМЕТРЫ

### -ID
Указывает идентификатор плана восстановления, который требуется получить.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Указывает полный путь для хранения XML-файла плана восстановления.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Указывает объект **ASRRecoveryPlan** , для которого требуется получить план восстановления.
Чтобы получить объект **ASRRecoveryPlan** , используйте командлет **Get-AzureSiteRecoveryRecoveryPlan** .

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


