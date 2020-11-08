---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075633"
---
# Get-AzurePublishSettingsFile

## КРАТКИй обзор
Загружает файл параметров публикации для подписки Azure.

## Максимальное

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzurePublishSettingsFile** загружает файл параметров публикации для подписки в своей учетной записи.
После завершения команды можно использовать командлет **Import-PublishSettingsFile** , чтобы сделать параметры в файле доступными для Windows PowerShell.

Чтобы сделать свою учетную запись Azure доступной для Windows PowerShell, вы можете использовать файл параметров публикации или командлет **Add-AzureAccount** .
Файлы параметров публикации позволяют заранее подготовить сеанс, чтобы можно было выполнять сценарии и фоновые задания без сопровождения.
Однако не все службы поддерживают файлы параметров публикации.
Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.

При запуске **Get-AzurePublishSettingsFile** открывается браузер по умолчанию и появляется запрос на вход в учетную запись Azure, выберите подписку и укажите расположение файловой системы для файла параметров публикации.
После этого файл параметров публикации для вашей подписки загружается в выбранный файл.

Файл параметров публикации — это XML-файл с расширением имени файла. publishsettings.
Файл содержит закодированный сертификат, который предоставляет учетные данные для управления подписками Azure.

**Примечание о безопасности:** Файлы параметров публикации содержат учетные данные, которые используются для управления подписками и службами Azure.
Пользователи, которые имеют доступ к файлу параметров публикации, могут редактировать, создавать и удалять службы Azure.
По соображениям безопасности сохраните файл в папке "Скачанные файлы" или "документы", а затем удалите ее после использования командлета **Import-AzurePublishSettingsFile** для импорта параметров.

В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка файла параметров публикации
```
PS C:\> Get-AzurePublishSettingsFile
```

Эта команда открывает браузер по умолчанию, подключается к вашей учетной записи Windows Azure и загружает файл publishsettings для своей учетной записи.

### Пример 2: указание сферы
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Эта команда загружает файл параметров публикации для учетной записи в домене contoso.com.
Используйте команду с параметром **realm** при входе в Azure с помощью учетной записи организации вместо учетной записи Майкрософт.

## ПАРАМЕТРЫ

### -Environment
Указывает среду Azure.

Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.
Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.
Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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
Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.
По умолчанию этот командлет не возвращает никаких выходных данных.

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
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -Realm
Определяет организацию в ИДЕНТИФИКАТОРе Организации.
Например, если вы входите в Azure как admin@contoso.com , значение параметра **Realm** — contoso.com.
Используйте этот параметр, если вы используете идентификатор организации для входа на портал Azure.
Этот параметр не требуется при использовании учетной записи Майкрософт, например учетной записи outlook.com или live.com.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Вы можете передавать входные данные командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### None и System. Boolean
При использовании параметра *PassThru* этот командлет возвращает логическое значение.
В противном случае этот командлет не возвращает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


