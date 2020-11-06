---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559292"
---
# Stop-AzureBatchPoolResize

## КРАТКИй обзор
Останавливает операцию изменения размера пула.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureBatchPoolResize** останавливает пакетную операцию по изменению размера пакета Azure для пула.

## ИЛЛЮСТРИРУЮТ

### Пример 1: прекращение изменения размера пула
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

Эта команда останавливает операцию изменения размера в пуле с ИДЕНТИФИКАТОРом ContosoPool06.
Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.

### Пример 2: прекращение изменения размера пула с помощью конвейера
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

Эта команда останавливает изменение размера пула с помощью оператора конвейера.
Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.
Команда передает этот объект пула в текущий командлет.
Команда останавливает операцию изменения размера в этом пуле.

## ПАРАМЕТРЫ

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой. Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа. Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор пула, для которого этот командлет останавливает операцию изменения размера.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

### Подстрок
Параметр ID принимает значение типа String из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Start-AzureBatchPoolResize](./Start-AzureBatchPoolResize.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


