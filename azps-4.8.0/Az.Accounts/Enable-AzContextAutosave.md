---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236396"
---
# Enable-AzContextAutosave

## КРАТКИй обзор
Контексты Azure — это объекты PowerShell, представляющие активную подписку, для которой выполняются команды, и сведения для проверки подлинности, необходимые для подключения к облаку Azure. При использовании контекстов Azure для Azure PowerShell не требуется повторная аутентификация учетной записи при каждом переключении подписок. Дополнительные сведения можно найти в разделе [объекты контекста Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Этот командлет позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell. Например, при открытии нового окна.

## Максимальное

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ

Позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell. Контекст сохраняется по завершении выполнения любого командлета, влияющего на контекст. Например, любой командлет профиля. Если вы используете проверку подлинности пользователя, то при запуске любого командлета можно обновить маркеры.

## ИЛЛЮСТРИРУЮТ

### Пример 1: включение учетных данных автосохранения для текущего пользователя

Включите Автосохранение учетных данных для текущего пользователя. Всякий раз, когда открывается окно PowerShell, текущий контекст запоминается без входа.

```powershell
Enable-AzContextAutosave
```

### Пример 2

Вы можете сохранять и автоматически загружать данные об учетных данных Azure, учетной записи и подписках, когда вы открываете окно PowerShell в этом сеансе PowerShell. (автоматически сформированные)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## ПАРАМЕТРЫ

### -DefaultProfile

Учетные данные, клиент и подписка, используемые для связи с Azure

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

### -Scope

Определяет область действия контекстных изменений. Например, изменения применяются только к текущему процессу или ко всем сеансам, запускаемым этим пользователем. Изменения, внесенные в область, `CurrentUser` влияют на все сеансы PowerShell, запускаемые пользователем. Если для определенного сеанса требуются разные параметры, используйте область `Process` .

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
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

### Общие параметры

Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
