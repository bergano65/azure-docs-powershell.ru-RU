---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561559"
---
# Set-AzureRmWcfRelay

## КРАТКИй обзор
Обновляет описание WcfRelay в указанном пространстве имен ретрансляции.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### WcfRelayInputObjectSet
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Set-AzureRmWcfRelay обновляет описание для WcfRelay в указанном пространстве имен ретрансляции.

## ИЛЛЮСТРИРУЮТ

### Пример 1-InputObject
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### Пример 2: свойства
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

Обновляет указанную WcfRelay с помощью нового описания в указанном пространстве имен.
В этом примере свойство UserMetadata обновляется новым значением.

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
Объект WcfRelay.

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
WcfRelay имя.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Имя пространства имен.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### -ResourceGroupName
System. String

### -+ +
System. String

### -WcfRelayName
System. String

### -InputObject
Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### -WcfRelayType
System. String

### -UserMetadata
System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### Пример 1-InputObject

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
RelayType: HTTP CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true Dynamic: false UserMetadata: UserMetadata — заполнитель для хранения данных, определенных пользователем, для конечной точки HybridConnection. Например: Он может использоваться для хранения данных DESC riptive, таких как список групп и контактные данные, а также пользовательские параметры конфигурации.
ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays

### Пример 2: свойства

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true Dynamic: false UserMetadata: ID метаданных пользователя:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel AY/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

