---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404404"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection проверяет возможность подключения от локального узла с кластером к службам Azure, которые требуются azure Stack HCI.

## СИНТАКСИС

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## ОПИСАНИЕ
Test-AzStackHCIConnection проверяет возможность подключения от локального узла с кластером к службам Azure, которые требуются azure Stack HCI.

## ПРИМЕРЫ

### ПРИМЕР 1
```
Invoking on one of the cluster node. Success case.
```

C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded

### ПРИМЕР 2
```
Invoking on one of the cluster node. Failed case.
```

C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3

## PARAMETERS

### -ComputerName
Указывает один из узлов кластера в локальном кластере, регистрируется в Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Определяет учетные данные для computerName.
По умолчанию выполняется текущий пользователь, который выполняет cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Указывает среду Azure.
По умолчанию это AzureCloud.
Допустимые значения: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Регион
Определяет регион, к который нужно подключиться.
Используется, если только это не является canary region.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### PSCustomObject. Возвращает следующие свойства в PSCustomObject:
### Проверка: имя выполненного теста.
### Конечная точкаТест: используемая в тесте конечная точка.
### IsRequired: True или False
### Результат: "Успешно" или "Сбой"
### FailedNodes: список узлов, на которых не удалось проверить.
## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
