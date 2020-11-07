---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: fda088ff8e8b3942ca6dbf94605b3887e3f6884b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907689"
---
# Remove-AzWebAppSSLBinding

## КРАТКИй обзор
Удаление привязки SSL из отправленного сертификата.

## Максимальное

### Состояний
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzWebAppSSLBinding** удаляет привязку SSL (Secure Sockets Layer) из веб-приложения Azure.
Привязки SSL используются для связывания веб-приложения с сертификатом.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление привязки SSL для веб-приложения
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Эта команда удаляет привязку SSL для веб-приложения ContosoWebApp.
Так как параметр *DeleteCertificate* не включен, сертификат будет удален, если он больше не имеет каких-либо SSL-привязок.

### Пример 2: удаление привязки SSL без удаления сертификата
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Как и в примере 1, эта команда также удаляет привязку SSL для веб-приложения ContosoWebApp.
Тем не менее, в этом случае параметр *DeleteCertificate* включается, и значение параметра задается равным $false.
Это означает, что сертификат не будет удален независимо от того, есть ли у него привязки SSL или нет.

### Пример 3: использование ссылки на объект для удаления привязки SSL
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

В этом примере для удаления привязки SSL для веб-приложения используется ссылка на объект веб-приложения.
Первая команда использует командлет Get-AzWebApp для создания ссылки на объект веб-приложения с именем ContosoWebApp.
Ссылка на объект хранится в переменной с именем $WebApp.
Вторая команда использует ссылку на объект и командлет **Remove-AzWebAppSSLBinding** для удаления привязки SSL.

## ПАРАМЕТРЫ

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

### -DeleteCertificate
Указывает действие, которое будет выполнено, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.
Если для *DeleteCertificate* задано значение $false, сертификат не будет удален при удалении привязки.
Если *DeleteCertificate* имеет значение $true или не включено в команду, сертификат будет удален вместе с привязкой SSL.
Сертификат будет удален только в том случае, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.
Если у сертификата есть более одной привязки, сертификат не будет удален независимо от значения параметра *DeleteCertificate* .

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя веб-приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен сертификат.
В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Указывает слот развертывания веб-приложения.
Чтобы получить слот развертывания, используйте командлет Get-AzWebAppSlot.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Указывает веб-приложение.
Чтобы получить веб-приложение, используйте командлет Get-AzWebApp.
Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Указывает имя веб-приложения.
В одной команде нельзя использовать параметры *WebAppName* и *webapp* .

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется. Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Apps. PSSite

## НАПРЯЖЕНИЕ

### System. void

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


