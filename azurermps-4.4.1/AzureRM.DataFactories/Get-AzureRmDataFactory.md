---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 5a7faf2e3eebcb00650bce367747e1945f7524da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559951"
---
# Get-AzureRmDataFactory

## КРАТКИй обзор
Получение сведений о фабриках данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDataFactory** получает сведения о фабриках данных в группе ресурсов Azure.
Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.
Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех фабрик данных
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Эта команда отображает сведения обо всех фабриках данных в подписке Azure.

### Пример 2: получение определенной фабрики данных
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.
Укажите параметр *фактического* значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя фабрики данных, сведения о которой требуется получить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет получает сведения о фабриках данных, относящихся к группе, которую указывает этот параметр.

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

### System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmDataFactory](./New-AzureRmDataFactory.md)

[Remove-AzureRmDataFactory](./Remove-AzureRmDataFactory.md)


