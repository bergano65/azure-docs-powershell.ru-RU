---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316391"
---
# Get-AzTemplateSpec

## КРАТКИй обзор
Возвращает или приводит список спецификаций шаблонов

## Максимальное

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

## NОПИСАНИЕ
Этот командлет можно использовать для получения спецификаций шаблонов в подписке или группе ресурсов, а также при получении определенных спецификаций шаблонов по имени или идентификатору. При получении определенных спецификаций шаблона по имени или идентификатору можно дополнительно извлечь определенную версию, указав ее имя с помощью параметра **-Version** . Когда используется **Версия-Version** , в течение * может быть указана только определенная информация о версии *. Версии* возвращаемого объекта Spec шаблона. Если при извлечении спецификаций шаблона по имени или идентификатору не указана какая-либо определенная версия, все версии будут указаны в разделе * *. Свойство Versions* возвращаемого объекта.

**Примечание**. при составлении списка всех спецификаций шаблонов в подписке или группе ресурсов каждый возвращенный шаблон спецификации *". Versions* будет *значение NULL*. Сведения о версии включаются только в том случае, если указаны параметры-Name или-ResourceId (например, вы запрашиваете определенную спецификацию и версию шаблона).

## ИЛЛЮСТРИРУЮТ

### Пример 1: спецификации шаблона списка в текущей подписке
```powershell
PS C:\> Get-AzTemplateSpec
```

Список всех спецификаций шаблонов в текущей подписке.

### Пример 2: спецификации шаблона списка в группе ресурсов
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Список всех спецификаций шаблонов в группе ресурсов "myRG" текущей подписки.

### Пример 3: получение спецификации шаблона (со всеми версиями) по названию
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Возвращает сведения о спецификации Template с именем "MyTemplateSpec" в группе ресурсов "myRG".

**Примечание**. все версии спецификации шаблона будут представлены в разделе " *. Свойство "Versions* " возвращаемого объекта.

### Пример 4: получение спецификации шаблона (конкретной версии) по названию
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Возвращает сведения о версии "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG".

**Примечание** : *". Свойство Versions* возвращаемого объекта будет содержать только определенную версию.

### Пример 5: получение спецификаций шаблона (со всеми версиями) по идентификатору ресурса
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Возвращает сведения о спецификации Template с именем "MyTemplateSpec" в группе ресурсов "myRG" в \{ subId подписку \} .

**Примечание**. все версии спецификации шаблона будут представлены в разделе " *. Свойство "Versions* " возвращаемого объекта.

### Пример 6: получение спецификации шаблона (конкретной версии) по идентификатору ресурса
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Возвращает сведения о версии "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG" для подписки \{ subId \} .

**Примечание** : *". Свойство Versions* возвращаемого объекта будет содержать только определенную версию.

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
Название спецификации шаблона.

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
Полный идентификатор ресурса спецификации шаблона. Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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

### -Version
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplateSpec

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
