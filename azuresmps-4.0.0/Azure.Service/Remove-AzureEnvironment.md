---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: cca7a4dcef9d3579576114a532b5185cc52c70a0
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104718552"
---
# Remove-AzureEnvironment

## SYNOPSIS
Удаляет среду Azure из Windows PowerShell.

## СИНТАКСИС

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его Windows PowerShell azureEnvironment** среда Azure удаляется из перемещаемого профиля.
Этот cmdlet не удаляет среду из Microsoft Azure и не меняет ее.

Среда Azure — независимое развертывание Microsoft Azure, например AzureCloud для глобального azure и AzureChinaCloud для Azure, управляемый компанией 21Vianet в Китае.
Вы также можете создавать локально среды Azure с помощью пакетов Azure и cmdlets WAPack.
Дополнительные сведения см. в [пакете Azure.](/previous-versions/azure/windows-server-azure-pack/)

## ПРИМЕРЫ

### Пример 1. Удаление среды
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Эта команда удаляет среду ContosoEnv из Windows PowerShell.

### Пример 2. Удаление нескольких сред
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Эта команда удаляет среды, имена которых начинаются с contoso, из Windows PowerShell.

## PARAMETERS

### -Force
Подавления запроса на подтверждение.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя среды, которая будет удаляться.
Этот параметр является required(обязательно).
Это значение параметра с чувствительной к делу.
Поддиавные знаки не разрешены.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### None или System.Boolean
Если вы используете параметр *PassThru,* этот cmdlet возвращает boolean value.
В противном случае результаты не возвращаются.

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


