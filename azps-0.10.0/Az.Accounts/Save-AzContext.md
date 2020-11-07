---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909377"
---
# Save-AzContext

## КРАТКИй обзор
Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.

## Максимальное

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Save-AzContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Сохранение контекста текущего сеанса
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.

### Пример 2: сохранение определенного контекста
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, клиент и подписка, используемые для связи с Azure.

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
Перезаписать заданный файл, если он существует

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

### -Path
Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает контекст Azure, из которого считывается этот командлет.
Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
