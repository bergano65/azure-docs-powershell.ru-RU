---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075549"
---
# Get-AzureStorageAccount

## КРАТКИй обзор
Возвращает учетные записи хранения для текущей подписки Azure.

## Максимальное

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageAccount** возвращает объект, содержащий сведения об учетных записях хранения для текущей подписки.
Если указан параметр *StorageAccountName* , возвращаются только сведения о указанной учетной записи хранения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: возврат всех учетных записей хранения
```
PS C:\> Get-AzureStorageAccount
```

Эта команда возвращает объект со всеми учетными записями хранения, связанными с текущей подпиской.

### Пример 2: возврат сведений об учетной записи для указанной учетной записи
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Эта команда возвращает объект, содержащий только данные учетной записи ContosoStore01.

### Пример 3: отображение таблицы учетных записей хранения
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Эта команда возвращает объект со всеми учетными записями хранения, связанными с текущей подпиской, и выводит их в виде таблицы, в которой указано имя учетной записи, метка учетной записи и место хранения.

## ПАРАМЕТРЫ

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -StorageAccountName
Указывает имя учетной записи хранения.
Если указан, этот командлет возвращает только указанный объект учетной записи хранения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### ManagementOperationContext

## Пуск
* Введите `help node-dev` сведения о Node.js командлетах, связанных с разработкой. Введите `help php-dev` справку по командлетам, связанным с разработкой PHP.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


