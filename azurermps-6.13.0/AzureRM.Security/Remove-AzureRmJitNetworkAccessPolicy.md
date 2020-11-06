---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562640"
---
# Remove-AzureRmJitNetworkAccessPolicy

## КРАТКИй обзор
Удаление политики доступа по JIT-сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupLevelResource (по умолчанию)
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Удаление политики сетевого доступа по времени.
После этого пользователь не сможет запросить временное сетевое подключение на виртуальных машинах, настроенных в удаленной политике.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

Удаление политики сетевого доступа по времени.

## ПАРАМЕТРЫ

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

### -InputObject
Объект input.

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Поиска.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Название ресурса.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает значение, указывающее, была ли операция выполнена успешно.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String
Microsoft. Azure. Commands. Security. командлеты. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
