---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 1c89db6267fffeb73820150d1c73c3225f45cde2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559960"
---
# Enable-AzureRmBackupContainerReregistration

## КРАТКИй обзор
Перерегистрация сервера для подключения к резервному хранилищу.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Enable-AzureRmBackupContainerReregistration** перерегистрирует сервер для подключения к хранилищу архивации Azure и продолжит создание резервной копии цепочки точек восстановления.

Если вы уничтожаете сервер, все его облачные точки резервного копирования остаются в хранилище резервных копий.
Если вы создаете заменяемый сервер и присвойте ему полное доменное имя, вы можете подключить сервер к тому же хранилищу.
Этот командлет позволяет создавать резервные копии и добавлять новые точки резервного копирования в существующий комплект.
Новый сервер продолжает работать в цепочке резервных копий.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -Container
Указывает контейнер, который перерегистрируется этим командлетом.
Чтобы получить **AzureRmBackupContainer** , используйте командлет Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureBackupContainer

## НАПРЯЖЕНИЕ

### Ничего

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Регистрация — AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


