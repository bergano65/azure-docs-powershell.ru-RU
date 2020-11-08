---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076552"
---
# Get-AzureStorSimpleAccessControlRecord

## КРАТКИй обзор
Возвращает записи управления доступом в конфигурации службы.

## Максимальное

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorSimpleAccessControlRecord** получает записи управления доступом в конфигурации службы StorSimple Manager.
Этот командлет получает все записи или именованную запись.

Записи управления доступом — это контейнеры параметров инициатора iSCSI.
Эти параметры определяют, какие инициаторы могут получать доступ к тому.
Когда инициатор iSCSI пытается подключиться к тому, устройство проверяет записи управления доступом, назначенные этому тому.
Если инициатор iSCSI соответствует одной из записей в записи управления доступом, сопоставленных с этим томом, инициатор iSCSI может подключиться.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех записей контроля доступа
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Эта команда возвращает все записи управления доступом.

### Пример 2: получение конкретной записи контроля доступа
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Эта команда получает запись контроля доступа с именем Acr11.

## ПАРАМЕТРЫ

### -ACRName
Указывает имя записи контроля доступа, которую требуется получить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### AccessControlRecord, IList\<AccessControlRecord\>
Этот командлет возвращает объект **AccessControlRecord** или объект **IList \<AccessControlRecord\>** .
Объект **AccessControlRecord** состоит из следующих полей: 

- **GlobalId** ( **строка** ) 
- **InitiatorName** ( **строка** ) 
- **InstanceId** ( **строка** ) 
- **Name** ( **строка** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


