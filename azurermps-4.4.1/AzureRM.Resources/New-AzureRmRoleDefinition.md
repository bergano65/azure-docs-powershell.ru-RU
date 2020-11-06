---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567072"
---
# New-AzureRmRoleDefinition

## КРАТКИй обзор
Создание настраиваемой роли в Azure RBAC.
Укажите в качестве входных данных либо файл определения роли в формате JSON, либо объект PSRoleDefinition.
Сначала используйте команду Get-AzureRmRoleDefinition, чтобы создать объект определения базовой роли.
Затем измените его свойства в соответствии с требованиями.
Наконец, используйте эту команду, чтобы создать настраиваемую роль с помощью определения роли.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InputFileParameterSet
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет New-AzureRmRoleDefinition создает настраиваемую роль в Azure Role-Based управления доступом.
Предоставьте определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.

Определение роли ввода должно содержать следующие свойства:

1) DisplayName: имя настраиваемой роли

2) Описание: краткое описание роли, предоставляющей доступ, предоставленный ролью.

3) Действия. набор операций, для доступа к которым настраиваемая роль предоставляет доступ.
Используйте Get-AzureRmProviderOperations для получения операции для поставщиков ресурсов Azure, которые можно защитить с помощью Azure RBAC.
Ниже приведены некоторые допустимые строки операций.
 - "*/Read" предоставляет доступ к операциям чтения всех поставщиков ресурсов Azure.
 - "Microsoft. Network/*/Read" предоставляет доступ к операциям чтения для всех типов ресурсов в поставщике ресурсов Microsoft. Network для Azure.
 - "Microsoft. COMPUTE/virtualMachines/*" предоставляет доступ ко всем операциям виртуальных машин и его дочерним типам ресурсов.

4) AssignableScopes: набор областей (подписок или групп ресурсов для Azure), в которых настраиваемая роль будет доступна для назначения.
С помощью AssignableScopes вы можете сделать настраиваемую роль доступной для назначения только для подписок или групп ресурсов, которым он нужен, и не очень бессрочным для остальных подписок и групп ресурсов.
Ниже перечислены некоторые допустимые назначаемые области.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": делает роль доступной для назначения в двух подписках.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": роль становится доступной для назначения в одной подписке.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": роль станет доступна для задания только в группе сетевых ресурсов.

Определение роли ввода может содержать следующие свойства:

1) Неизмененные данные: набор операций, которые необходимо исключить из действий для определения действующих действий для настраиваемой роли.
Если вы не хотите предоставлять доступ в особой роли, вы можете использовать ненужные функции, чтобы исключить их, вместо того чтобы указывать все операции, отличные от той, которые выполняются в действиях.

Примечание. Если пользователю назначена роль, указывающая на операцию в состоянии "не отменять", а другая роль предоставляет доступ к одной и той же операции, пользователь сможет выполнить эту операцию.
"Мои изменения" не является правилом запретов — это просто удобный способ создания набора разрешенных операций, если требуется исключить определенные операции.

Ниже приведен пример определения роли JSON, которое может быть предоставлено как input {"имя": "компания Contoso On-Call", "Описание": "может отслеживать вычисление, сеть и хранение, а также перезапускать виртуальные машины", "действия": "Microsoft. COMPUTE//Read", "Microsoft. Вычисление/virtualMachines/начало/действие", "Microsoft. COMPUTE/virtualMachines/downloadRemoteDesktopConnectionFile/действие", "Microsoft. COMPUTE/ \[ *virtualMachines/Restart Network/* /Read", "Microsoft. Storage//Read", "Microsoft *. Authorization* //Read", "Microsoft. Resources/Subscriptions/resourceGroups/Resources/READS/", "Microsoft. Insights/alertRules/", "Microsoft *. support/* ", " \] AssignableScopes": \[ " \]

## ИЛЛЮСТРИРУЮТ

### --------------------------Создание с помощью PSRoleDefinitionObject--------------------------
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
          PS C:\> $role.Id = $null
          PS C:\> $role.Name = "Virtual Machine Operator"
          PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
          PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
          PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
          PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
          PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
          PS C:\> $role.Actions.Add("Microsoft.Support/*")
          PS C:\> $role.AssignableScopes.Clear()
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### --------------------------Создание с помощью файла JSON--------------------------
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## ПАРАМЕТРЫ

### -InputFile
Имя файла, в котором содержится одно определение роли JSON.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role (роль)
Объект определения роли.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
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

### Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Set-AzureRmRoleDefinition](./Set-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

