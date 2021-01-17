---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327113"
---
# Get-AzDataBoxJob

## SYNOPSIS
Сведения о заданиях работы с данными

## СИНТАКСИС

### ListParameterSet (по умолчанию)
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для получения сведений о заданиях работы с почтовыми ящиками в подписке Azure возвращается cmdlet **Get-AzDataBoxJobs.**
Если указать группу ресурсов, этот cmdlet получит все задания для работы с почтовыми ящиками в этой группе ресурсов. Если вы указываете имя задания вместе с именем группы ресурсов, этот cmdlet получает сведения об этом конкретном сообщении в почтовом ящике.
Если не указать ничего, кроме кодов подписки, этот cmdlet получит сведения обо всех заданиях работы с почтовыми ящиками в этой подписке.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

Get-AzDataBoxJob без параметра извлекает все задания обработки данных в подписке

### Пример 2
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

Get-AzDataBoxJob с параметром ResourceGroupName извлекает все задания почтового ящика в указанной группе ресурсов

### Пример 3
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

Get-AzDataBoxJob, для которого заданы имя и имя ресурса, будет извлекаться из этого задания

### Пример 4
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

Get-AzDataBoxJob с заданным ид.ресурса извлекет определенное задание для почтового ящика

## PARAMETERS

### -Aborted
Переключение параметра для получения прерванных заданий

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отменено
Переключение параметра для получения отмененных заданий

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Completed
Переключение параметра для получения завершенных заданий

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompletedWithError
Переключение параметра для получения заданий, завершенных с ошибками

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Name
Имя задания для почтового ящика

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов задания в почтовом ящике

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ИД задания для почтового ящика

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDAtaBoxJob

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
