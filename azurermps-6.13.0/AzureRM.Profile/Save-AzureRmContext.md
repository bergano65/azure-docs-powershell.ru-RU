---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560768"
---
# Save-AzureRmContext

## КРАТКИй обзор
Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Save-AzureRmContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Сохранение контекста текущего сеанса
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.

### Пример 2: сохранение определенного контекста
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, клиент и подписка, используемые для связи с Azure.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile
Параметры: Profile (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Profile. Models. PSAzureProfile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
