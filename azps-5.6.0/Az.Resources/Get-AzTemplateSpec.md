---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960115"
---
# Get-AzTemplateSpec

## SYNOPSIS
Возвращает или перечисляет спецификации шаблона.

## СИНТАКСИС

### ListTemplateSpecsParameterSet (по умолчанию)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С помощью этого cmdlet можно использовать для списка спецификаций шаблона в группе подписок и ресурсов или получения определенной спецификации шаблона по имени или коду. При получении определенной спецификации шаблона по имени или ид можно при желании получить конкретную версию, указав имя версии с помощью параметра **-Version.** Если **используется версия** -, в пределах * будут представлены только конкретные сведения о *версии. Версии возвращенного* объекта Template Spec. Если при искомой спецификации шаблона не указана конкретная версия, будут представлены все версии в формате **. Свойство Версий* возвращаемого объекта.

**Примечание.** При перечислении всех спецификаций шаблона в рамках подписки или группы ресурсов каждый возвращаемый шаблон *". Свойство Versions* (Версии) будет *иметь null.* Сведения о версии включаются только в том случае, если заданы параметры -Name или -ResourceId (например, вы запрашиваете определенный шаблон спецификации/версии).

## ПРИМЕРЫ

### Пример 1. Спецификации шаблона списка в текущей подписке
```powershell
PS C:\> Get-AzTemplateSpec
```

Список всех спецификаций шаблона в текущей подписке.

### Пример 2. Спецификации шаблона списка в группе ресурсов
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Список всех спецификаций шаблона в группе ресурсов MyRG текущей подписки.

### Пример 3. Получить спецификацию шаблона (со всеми версиями) по имени
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Возвращает сведения о спецификации шаблона MyTemplateSpec в группе ресурсов myRG.

**Примечание.** Все версии шаблона Спецификации будут представлены в *Свойство Versions*(Версии) возвращаемого объекта.

### Пример 4. Получить шаблон спецификации (конкретную версию) по имени
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Сведения о версии "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG.

**Примечание.** *Свойство «Версии»* возвращаемого объекта будет содержать только запрашиваемую версию.

### Пример 5. Получить шаблон спецификации (со всеми версиями) по ид ресурса
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Возвращает сведения о спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов myRG подид \{ \} подписки.

**Примечание.** Все версии шаблона Спецификации будут представлены в *Свойство Versions*(Версии) возвращаемого объекта.

### Пример 6. Получить спецификацию шаблона (конкретную версию) по ид ресурса
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Сведения о версии "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG из \{ subId \} подписки.

**Примечание.** *Свойство «Версии»* возвращаемого объекта будет содержать только запрашиваемую версию.

## PARAMETERS

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

### -Name
Имя спецификации шаблона.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
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
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Полное имя ресурса спецификации шаблона. Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Версия
Версия спецификации шаблона.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
