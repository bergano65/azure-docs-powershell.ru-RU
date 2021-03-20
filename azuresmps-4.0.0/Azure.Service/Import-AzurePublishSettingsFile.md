---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: e99e0c2605af1c6083ae571e6039f6d11e915648
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104716631"
---
# Import-AzurePublishSettingsFile

## SYNOPSIS
Импорт файла параметров публикации, который позволяет управлять учетными записями Azure в Windows PowerShell.

## СИНТАКСИС

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
С помощью cmdlet **Import-AzurePublishSettingsFile** импортируется файл параметров публикации (*.publishsettings), содержащий сведения об учетных записях Azure, и сохраняет файл данных о подписке на вашем компьютере.
После выполнения cmdlet вы можете управлять учетными записьми Azure в Windows PowerShell.

Перед запуском **Import-AzurePublishSettingsFile** запустите **get-AzurePublishSettingsFile,** который скачает и сохранит файл параметров публикации, чтобы его можно было импортировать.

Чтобы сделать учетную запись Azure доступной для Windows PowerShell, можно использовать файл параметров публикации или **cmdlet Add-AzureAccount.**
Файлы параметров публикации можно подготовить к сеансу заранее, чтобы можно было запускать сценарии и фоновые задания без дополнительных настроек.
Однако не все службы поддерживают файлы параметров публикации.
Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.

**Примечание для системы безопасности:** Файлы параметров публикации содержат сертификат управления, который закодирован, но не зашифрован.
Если злоумышленники имеют доступ к файлу параметров публикации, они могут редактировать, создавать и удалять службы Azure.
В целях безопасности сохраните файл в папке "Загрузки" или "Документы", а затем удалите его после импорта параметров с помощью cmdlet **Import-AzurePublishSettingsFile.**

## ПРИМЕРЫ

### Пример 1. Импорт файла
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Эта команда импортирует файл C:\Temp\MyAccount.publishsettings.

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
Accept pipeline input: False
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

### -PublishSettingsFile
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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### Нет
Этот cmdlet не создает никаких выходных данных.

## ПРИМЕЧАНИЯ
* "Файл параметров публикации" — это XML-файл с расширением имени файла Publishsettings. Файл содержит закодированный сертификат, который предоставляет учетные данные управления для ваших подписок Azure. После импорта файла удалите его, чтобы избежать угроз безопасности.
* "Файл данных подписки" — это XML-файл, который можно безопасно сохранить на компьютере. По умолчанию он сохранен в перемещаемом профиле пользователя ($home/AppData/Roaming).

## СВЯЗАННЫЕ ССЫЛКИ

[Установка и настройка Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


