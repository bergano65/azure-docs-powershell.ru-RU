---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559316"
---
# Get-AzureRmBatchAccount

## КРАТКИй обзор
Возвращает пакетную учетную запись в текущей подписке.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBatchAccount** получает пакетную учетную запись Azure в текущей подписке. Вы можете использовать параметр *AccountName* для получения одной учетной записи или с помощью параметра *ResourceGroupName* для получения учетных записей в этой группе ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение учетной записи пакетной службы по имени
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

Эта команда возвращает пакетную учетную запись с именем pfuller.

### Пример 2: получение пакетных учетных записей, связанных с группой ресурсов
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Эта команда получает учетные записи пакетов, связанные с группой ресурсов CmdletExampleRG.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Указывает имя учетной записи.
Если указать имя учетной записи, этот командлет вернет только эту учетную запись.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Указывает имя группы ресурсов.
Если указана группа ресурсов, этот командлет получает учетные записи в указанной группе ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

Этот командлет получает учетные записи, содержащие теги, которые указывает этот параметр.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmBatchAccount](./New-AzureRmBatchAccount.md)

[Remove-AzureRmBatchAccount](./Remove-AzureRmBatchAccount.md)

[Set-AzureRmBatchAccount](./Set-AzureRmBatchAccount.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)
