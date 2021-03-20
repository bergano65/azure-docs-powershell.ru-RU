---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4eb278998220de08f81aa3a023070c5961273c63
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104718602"
---
# Get-AzurePublishSettingsFile

## SYNOPSIS
Скачивает файл параметров публикации для подписки Azure.

## СИНТАКСИС

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **использованием cmdlet get-AzurePublishSettingsFile** скачивает файл параметров публикации для подписки в вашей учетной записи.
После выполнения команды можно воспользоваться командлетом **Import-PublishSettingsFile,** чтобы сделать параметры файла доступными для Windows PowerShell.

Чтобы сделать учетную запись Azure доступной для Windows PowerShell, можно использовать файл параметров публикации или **cmdlet Add-AzureAccount.**
Файлы параметров публикации можно подготовить к сеансу заранее, чтобы можно было запускать сценарии и фоновые задания без дополнительных настроек.
Однако не все службы поддерживают файлы параметров публикации.
Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.

При запуске **Get-AzurePublishSettingsFile** открывается браузер по умолчанию, в который вам будет предложено войти в учетную запись Azure, выбрать подписку и выбрать расположение файловой системы для файла параметров публикации.
Затем он скачивает файл параметров публикации для подписки в выбранный файл.

"Файл параметров публикации" — это XML-файл с расширением имени файла Publishsettings.
Файл содержит закодированный сертификат, который предоставляет учетные данные управления для ваших подписок Azure.

**Примечание для системы безопасности:** Файлы параметров публикации содержат учетные данные, которые используются для администрирования подписок и служб Azure.
Злоумышленники, которые имеют доступ к файлу параметров публикации, могут изменять, создавать и удалять службы Azure.
В целях безопасности сохраните файл в папке "Загрузки" или "Документы", а затем удалите его после импорта параметров с помощью cmdlet **Import-AzurePublishSettingsFile.**

В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

## ПРИМЕРЫ

### Пример 1. Скачивание файла параметров публикации
```
PS C:\> Get-AzurePublishSettingsFile
```

Эта команда открывает браузер по умолчанию, подключается к учетной записи Windows Azure и скачивает файл PUBLISHSETTINGS для вашей учетной записи.

### Пример 2. Указание области
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Эта команда скачивает файл параметров публикации для учетной записи в contoso.com домене.
Используйте команду с параметром **Realm** при входе в Azure с помощью учетной записи организации, а не учетной записи Майкрософт.

## PARAMETERS

### -Среда
Указывает среду Azure.

Среда Azure — независимое развертывание Microsoft Azure, например AzureCloud для глобального azure и AzureChinaCloud для Azure, управляемый компанией 21Vianet в Китае.
Вы также можете создавать локально среды Azure с помощью пакетов Azure и cmdlets WAPack.
Дополнительные сведения см. в [пакете Azure.](/previous-versions/azure/windows-server-azure-pack/)

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

### -PassThru
Возвращает $True, если команда будет успешной, $False если она не будет возвращена.
По умолчанию этот cmdlet не возвращает никаких выходных данных.

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

### -Реалм
Указывает организацию в ИД организации.
Например, если войти в Azure как, значение параметра admin@contoso.com **Realm** будет contoso.com.
Используйте этот параметр при входе на портал Azure с помощью ИД организации.
Этот параметр не требуется при использовании учетной записи Майкрософт, например учетной записи outlook.com или live.com учетной записи.

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

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### None или System.Boolean
При использовании *параметра PassThru* этот cmdlet возвращает boolean value.
В противном случае этот cmdlet не возвращает результатов.

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


