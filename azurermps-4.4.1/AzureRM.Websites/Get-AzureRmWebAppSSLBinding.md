---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae03fd4dedf1e0e6de91bd036180379c2be2cabe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561975"
---
# Get-AzureRmWebAppSSLBinding

## КРАТКИй обзор
Получение привязки SSL сертификата веб-приложения Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Состояний
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmWebAppSSLBinding** получает для веб-приложения Azure привязку SSL (Secure socketing Layer).
Привязки SSL используются для связывания веб-приложения с отправленным сертификатом.
Веб-приложения можно привязать к нескольким сертификатам.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение привязок SSL для веб-приложения
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Эта команда извлекает привязки SSL для веб-приложения ContosoWebApp, связанного с группой ресурсов ContosoResourceGroup.

### Пример 2: использование ссылки на объект для получения привязок SSL для веб-приложения
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

Команды в этом примере также получают привязки SSL для веб-приложения ContosoWebApp; Однако в этом случае вместо имени веб-приложения и имени связанной группы ресурсов используется ссылка на объект.
Эта ссылка на объект создана первой командой в примере, которая использует **Get-AzureRmWebApp** для создания ссылки на объект веб-приложения с именем ContosoWebApp.
Ссылка на объект хранится в переменной с именем $WebApp.

Эта переменная и командлет **Get-AzureRmWebAppSSLBinding** используются второй командой для получения привязок SSL.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя привязки SSL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
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
Чтобы получить слот развертывания, используйте командлет Get-AzureRMWebAppSlot.

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
Чтобы получить веб-приложение, используйте командлет Get-AzureRmWebApp.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Указывает имя веб-приложения, из которого этот командлет получает привязки SSL.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Семейств
Параметр "WebApp" принимает значение типа "сайт" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


