---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567075"
---
# New-AzureRmResourceGroupDeployment

## КРАТКИй обзор
Добавляет развертывание Azure в группу ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Развертывание с помощью файла шаблона без параметров (по умолчанию)
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Развертывание с помощью файла шаблона и объекта "Параметры шаблона"
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью URI шаблона и объекта "Параметры шаблона"
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью файла шаблона и файла параметров шаблона
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью URI шаблона и файла параметров шаблона
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью URI параметров шаблона файла шаблона
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью URI шаблона и URI параметров шаблона
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Развертывание с помощью URI шаблона без параметров
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.
Сюда входят ресурсы, необходимые для развертывания.

Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.
Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.
Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.
Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzureRmResource.

Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.
Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.
Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.
Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.
Вы можете использовать командлет **Get-AzureRmResourceGroupGalleryTemplate** , чтобы найти шаблон в галерее.

Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .
Каждый шаблон имеет параметры для настраиваемых свойств.
Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .
Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.
Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.
Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.

## ИЛЛЮСТРИРУЮТ

### Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске.
В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.
Для указания версии шаблона используется параметр *TemplateVersion* .

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentDebugLogLevel
Задает уровень журнала отладки.
Для этого параметра допустимы следующие значения:

- RequestContent 
- ResponseContent 
- Весь 
- Ничего

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Режим
Задает режим развертывания. Для этого параметра допустимы следующие значения:

- Полнот 
- Разност

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя создаваемого развертывания группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов для развертывания.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateFile
Указывает полный путь к файлу шаблона JSON.
Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzureRmResourceGroupGalleryTemplate** .

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.
Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .
Параметры шаблона динамически добавляются в команду при указании шаблона.

Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
Указывает хэш-таблицу имен и значений параметров шаблона.
Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .
Если у шаблона есть параметры, необходимо указать значения параметров.
Параметры шаблона динамически добавляются в команду при указании шаблона.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
Задает универсальный код ресурса (URI) файла параметров шаблона.

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
Задает универсальный код ресурса (URI) для файла шаблона JSON.
Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzureRmResourceGroupGalleryTemplate**.

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmResourceGroupDeployment](./Get-AzureRmResourceGroupDeployment.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[New-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Остановить-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


