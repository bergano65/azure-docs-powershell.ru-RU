---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076261"
---
# Import-AzurePublishSettingsFile

## КРАТКИй обзор
Импорт файла параметров публикации, с помощью которого можно управлять учетными записями Azure в Windows PowerShell.

## Максимальное

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Import-AzurePublishSettingsFile** импортирует файл параметров публикации (*. publishsettings), содержащий сведения об учетных записях Azure, и сохраняет файл данных подписки на компьютере.
После завершения командлета вы можете управлять учетными записями Azure в Windows PowerShell.

Перед запуском команды **Import-AzurePublishSettingsFile** запустите **Get-AzurePublishSettingsFile** , который загрузит и сохранит файл параметров публикации, чтобы его можно было импортировать.

Чтобы сделать свою учетную запись Azure доступной для Windows PowerShell, вы можете использовать файл параметров публикации или командлет **Add-AzureAccount** .
Файлы параметров публикации позволяют заранее подготовить сеанс, чтобы можно было выполнять сценарии и фоновые задания без сопровождения.
Однако не все службы поддерживают файлы параметров публикации.
Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.

**Примечание о безопасности:** Файлы параметров публикации содержат сертификат управления, который закодирован, но не зашифрован.
Если пользователи могут получить доступ к файлу параметров публикации, они смогут редактировать, создавать и удалять службы Azure.
По соображениям безопасности сохраните файл в папке "Скачанные файлы" или "документы", а затем удалите ее после использования командлета **Import-AzurePublishSettingsFile** для импорта параметров.

## ИЛЛЮСТРИРУЮТ

### Пример 1: импорт файла
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Эта команда импортирует файл "C:\Temp\MyAccount.publishsettings".

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
Accept pipeline input: False
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Вы можете передавать входные данные командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### Ничего
Этот командлет не создает никаких выходных данных.

## Пуск
* Файл параметров публикации — это XML-файл с расширением имени файла. publishsettings. Файл содержит закодированный сертификат, который предоставляет учетные данные для управления подписками Azure. После импорта файла удалите его, чтобы избежать угрозы безопасности.
* Файл данных подписки — это XML-файл, который можно безопасно сохранить на компьютере. По умолчанию он сохраняется в перемещаемом профиле пользователя ($home/AppData/Roaming).

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Установка и настройка Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


