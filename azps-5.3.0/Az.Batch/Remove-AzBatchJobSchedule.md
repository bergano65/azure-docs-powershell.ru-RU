---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519788"
---
# Remove-AzBatchJobSchedule

## SYNOPSIS
Удаляет расписание пакетных рабочих мест.

## СИНТАКСИС

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его использованием удаляется** расписание рабочих мест Azure Batch.

## ПРИМЕРЫ

### Пример 1. Удаление графика пакетных задания
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

Эта команда удаляет расписание задания с календарем ID MyJobSchedule.
Перед удалением задания вам будет предложено подтвердить удаление.
Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.

### Пример 2. Удаление пакетного задания без подтверждения с помощью конвейера
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

Эта команда получает расписание задания, которое использует ID MyJobSchedule, с помощью Get-AzBatchJobSchedule командлета.
Эта команда передает расписание задания текущему командлету с помощью оператора конвейера.
Команда удаляет это расписание задания.
Так как команда содержит параметр *Force,* запрос на подтверждение не выдан.

## PARAMETERS

### -BatchContext
Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.
Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory. Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию. Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Force
Запуск команды без запроса подтверждения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Определяет ИД удаляемого расписания задания.

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

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Disable-AzBatchJobSchedule](./Disable-AzBatchJobSchedule.md)

[Enable-AzBatchJobSchedule](./Enable-AzBatchJobSchedule.md)

[Get-AzBatchJobSchedule](./Get-AzBatchJobSchedule.md)

[New-AzBatchJobSchedule](./New-AzBatchJobSchedule.md)

[Set-AzBatchJobSchedule](./Set-AzBatchJobSchedule.md)

[Stop-AzBatchJobSchedule](./Stop-AzBatchJobSchedule.md)


