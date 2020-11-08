---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075883"
---
# Publish-AzureServiceProject

## КРАТКИй обзор
Опубликуйте текущую службу в Windows Azure.

## Максимальное

### PublishFromServiceDefinition (по умолчанию)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Publish-AzureServiceProject** публикует текущую службу в облаке.
Вы можете указать конфигурацию публикации (например, **подписку** , **StorageAccountName** , **Расположение** , **гнездо** ) в командной строке или локальные параметры с помощью командлета **Set-AzureServiceProject** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: публикация проекта службы со значениями по умолчанию
```
PS C:\> Publish-AzureServiceProject
```

В этом примере текущая служба публикуется с использованием текущих параметров службы и текущего профиля публикации Azure.

### Пример 2: создание пакета развертывания
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

В этом примере создается файл пакета развертывания (CSPKG) в каталоге службы и не публикуется в Windows Azure.

## ПАРАМЕТРЫ

### -AffinityGroup
Указывает территориальную группу, которую должна использовать служба.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configuration
Указывает файл конфигурации службы.
Если указать этот параметр, укажите параметр *Package* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
Указывает имя развертывания.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Launch
Открывает окно браузера, чтобы можно было просмотреть приложение после его развертывания.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Область, в которой будет размещено приложение.
Возможны следующие значения: 
  
- В любом уголке Азии
- В любом уголке Европы
- Где бы мы ни находились
- Восточная Азия
- Восточная часть США
- Северный Центральный США
- Северная Европа
- Южная Центральная американская
- Юго-Восточная Азия
- Западная Европа
- Западная часть США
 
Если расположение не указано, будет использоваться расположение, указанное в последнем вызове **Set-AzureServiceProject** . Если вы не указали расположение, оно будет выбрано случайным образом из расположений "Северный центр США" и "Южная Центральная США".

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Package
Указывает файл пакета для развертывания.
Укажите локальный файл, содержащий расширение имени файла cspkg или URI-код большого двоичного объекта, содержащего пакет.
Если вы задаете этот параметр, не указывайте параметр *ServiceName* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -ServiceName
Указывает имя, которое будет использоваться службой при публикации в Windows Azure.
Имя определяет часть метки в дочернем домене cloudapp.net, которая используется для адресации службы при размещении в Windows Azure (то есть **Name**. cloudapp.NET).
Имя, указанное при публикации, переопределяет имя, указанное при создании службы.
(Дополнительные сведения о командлете **New-AzureServiceProject** ).

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Слот развертывания, который будет использоваться для этой службы.
Возможные значения: "промежуточные и производственные".
Если ячейка не указана, используется гнездо, указанное в последнем вызове Set-AzureDeploymentSlot.
Если слот не указан, используется гнездо "производство".

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя учетной записи хранения Windows Azure, которое будет использоваться при публикации службы.
Это значение не используется, пока служба не опубликована.
Если этот параметр не указан, значение извлекается из последней команды **Set-AzureServiceProject** .
Если учетная запись хранения не была указана, будет использоваться учетная запись хранилища, соответствующая имени службы.
Если такой учетной записи хранения не существует, командлет попытается создать новый.
Однако попытка может завершиться ошибкой, если учетная запись хранения, совпадающая с именем службы, существует в другой подписке.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


