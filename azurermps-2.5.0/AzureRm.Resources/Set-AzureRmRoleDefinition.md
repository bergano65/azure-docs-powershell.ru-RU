---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913967"
---
# Set-AzureRmRoleDefinition

## КРАТКИй обзор
Изменяет настраиваемую роль в Azure RBAC.
Укажите измененное определение роли либо в виде JSON-файла, либо в виде PSRoleDefinition.
Сначала используйте команду Get-AzureRmRoleDefinition, чтобы получить настраиваемую роль, которую вы хотите изменить.
Затем измените свойства, которые вы хотите изменить.
Наконец, сохраните определение роли с помощью этой команды.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Set-AzureRmRoleDefinition обновляет существующую настраиваемую роль в Azure Role-Based управления доступом.
Предоставьте обновленное определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.
Определение роли для обновленной настраиваемой роли должно содержать идентификатор и все другие обязательные свойства роли, даже если они не были обновлены: DisplayName, описание, действия, AssignableScopes.
Не все изменения, макрокоманды, NotDataActions являются необязательными.
Ниже приведен пример обновленного определения роли JSON для Set-AzureRmRoleDefinition {"ИД": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "имя": "обновленная роль", "Описание": "может отслеживать все ресурсы, запускать и перезапускать виртуальные машины", "действия": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/перезапустить/действие", "Microsoft. ClassicCompute/virtualmachines/Start/Action", "незащищенные" \] : \[ "* /Write" \] , "Actions": " \[ Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/большие/двоичные \] объекты/BLOB/ \[ записи" \] , "NotDataActions": \[ "storageAccounts") \]

## ИЛЛЮСТРИРУЮТ

### Обновление с помощью PSRoleDefinitionObject
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### Создание с помощью JSON File
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -InputFile
Имя файла, содержащего одно определение роли JSON, которое требуется обновить.
Включайте только свойства, которые должны быть обновлены в JSON.
Требуется свойство ID.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role (роль)
Обновляемый объект определения роли

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition
Параметры: role (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

