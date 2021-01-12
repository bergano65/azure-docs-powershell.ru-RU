---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110484"
---
# New-AzureWebsite

## SYNOPSIS
Создайте веб-сайт, который будет работать в Azure.

## СИНТАКСИС

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

С помощью этой команды можно создать веб-сайт, который будет работать в Azure, и подготовиться к развертыванию через GitHub.

## ПРИМЕРЫ

### Пример 1. Создание веб-сайта с помощью Git
```
PS C:\> New-AzureWebsite mySite -Git
```

В этом примере создается новый веб-сайт в Azure и локальный репозиторий GIT, который можно использовать для развертывания файлов на новом веб-сайте.

### Пример 2. Создание веб-сайта, интегрированного с GitHub
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

В этом примере создается новый веб-сайт, связанный с репозиторием GitHub с именем myaccount/myrepo.
Обязательства для репозитория GitHub перенадвигаются на веб-сайт в Azure.

## PARAMETERS

### -Git
Настраивает локальный репозиторий GIT и связывает его с веб-сайтом.
При этом настраивается репозиторий GIT в локальном каталоге и добавляется удаленный репозиторий azure, который ссылется на веб-сайт в Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Указывает на то, что этот cmdlet связывает новый веб-сайт с существующим репозиторием GitHub.
Обязательства для репозитория Giuthub перенадвигаются на веб-сайт в Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubCredentials
Указывает имя пользователя и учетные данные для подключения к GitHub.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubRepository
Указывает полное имя репозитория GitHub, связываемого с этим веб-сайтом.
Например, `myaccount/myrepo` .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hostname
Указывает альтернативное имя для нового веб-сайта.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Указывает расположение центра обработки данных, в котором вы хотите развернуть веб-сайт.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Указывает имя веб-сайта.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Определяет профиль Azure, с которого этот cmdlet будет читать данные.
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

### -PublishingUsername
Указывает имя пользователя, указанное на портале Azure для развертывания Git.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Указывает название слота для веб-сайта.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## OUTPUTS

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Set-AzureWebsite](./Set-AzureWebsite.md)


