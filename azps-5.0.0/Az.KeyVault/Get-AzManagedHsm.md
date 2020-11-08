---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247727"
---
# Get-AzManagedHsm

## КРАТКИй обзор
Получить управляемый HSMs.

## Максимальное

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzManagedHsm** получает сведения об управляемых HSMsх в подписке. Вы можете просмотреть все управляемые экземпляры HSMs в подписке или отфильтровать результаты по группе ресурсов или определенному управляемому HSM.
Обратите внимание на то, что, хотя указание группы ресурсов является необязательным для этого командлета при получении единого управляемого HSM-ключа, для лучшей производительности необходимо сделать это.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех управляемых HSMs в текущей подписке
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Эта команда получает все управляемые HSMs в текущей подписке.

### Пример 2: получение определенного управляемого HSM
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Эта команда получает управляемый HSM, именуемый myhsm, в текущей подписке.

### Пример 3: получение управляемых HSMs в группе ресурсов
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Эта команда получает все управляемые HSMs в группе ресурсов с именем myrg1.

### Пример 4: получение управляемых HSMs с помощью фильтрации
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Эта команда получает все управляемые HSMs в подписке, которые начинаются с "myhsm".

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя HSM. Командлет создает полное доменное имя (FQDN) для HSM на основе имени и выбранной в данный момент среды.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, связанной с запрашиваемым управляемым HSM.

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

### -Тег
Задает ключ и необязательное значение указанного тега для фильтрации списка управляемых HSMs.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm

### Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultIdentityItem

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzManagedHsm](./New-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Update-AzManagedHsm](./Update-AzManagedHsm.md)