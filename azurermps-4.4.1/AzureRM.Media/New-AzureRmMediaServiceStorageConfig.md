---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 236486af937a99812f4979ed4db089002fb9ad30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567114"
---
# New-AzureRmMediaServiceStorageConfig

## КРАТКИй обзор
Создайте конфигурацию учетной записи хранения для командлетов службы мультимедиа.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmMediaServiceStorageConfig** создает конфигурацию учетной записи хранения для командлетов службы мультимедиа.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание конфигурации учетной записи хранения для командлетов службы мультимедиа
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

Первая команда создает объект учетной записи хранения с помощью командлета **New-AzureRmStorageAccount** .
Команда называет эту учетную запись хранения Storage1 и тип с именем Standard_GRS и сохраняет результат в переменной с именем $StorageAccount.

Вторая команда создает объект конфигурации хранилища в качестве основной учетной записи хранилища, связанной со службой мультимедиа, с помощью ИДЕНТИФИКАЦИОНных данных учетной записи хранения, сохраненных в переменной $StorageAccount.

## ПАРАМЕТРЫ

### -Primary
Указывает на то, что командлет создает учетную запись хранения в качестве основного хранилища для службы мультимедиа.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountId
Указывает идентификатор учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Media. Models. PSStorageAccount

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Sync (синхронизация) — AzureRmMediaServiceStorageKeys](./Sync-AzureRmMediaServiceStorageKeys.md)


