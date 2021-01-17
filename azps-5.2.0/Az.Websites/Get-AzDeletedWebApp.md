---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327140"
---
# Get-AzDeletedWebApp

## SYNOPSIS
Удаляется из подписки веб-приложения.

## СИНТАКСИС

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для получения всех удаленных веб-приложений в подписке **возвращается cmdlet Get-AzDeletedWebApp.** При желании удаленные приложения можно отфильтровать по группе ресурсов, имени и слоту. Может быть несколько удаленных приложений с одинаковыми именем и группой ресурсов. Проверьте DeletionTime, чтобы различать удаленные приложения с одинаковыми именами.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

Эта команда возвращает удаленные приложения ContosoSite, принадлежащие группе ресурсов Default-Web-WestUS.

## PARAMETERS

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

### -Location
Расположение удаленного приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя веб-приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Название слота веб-приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Restore-AzDeletedWebApp](./Restore-AzDeletedWebApp.md)