---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560543"
---
# Set-AzureRmAutomationModule

## КРАТКИй обзор
Обновляет модуль в автоматизации.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmAutomationModule** обновляет модуль в службе автоматизации Azure.
Эта команда принимает сжатый файл с расширением ZIP.
Файл содержит папку, в которую входит файл одного из следующих типов: 

- модуль wps_2, имеющий расширение имени файла. PSM1 или. dll 
- манифест модуля wps_2, имеющий расширение имени файла. PSD1

Имя ZIP-файла, имя папки, а также имя файла в папке должны совпадать.

Укажите ZIP-файл, который может получать Access служба автоматизации.

При импорте wps_2ного модуля в автоматизацию с помощью этого командлета или командлета New-AzureRmAutomationModule операция выполняется асинхронно.
Команда завершает выполнение импорта или завершается неуспешно.
Чтобы проверить, успешно ли она выполнена, выполните следующую команду:

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName

Установите для свойства **ProvisioningState** значение "успешно".

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление модуля
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Эта команда импортирует обновленную версию существующего модуля с именем ContosoModule в учетную запись автоматизации с именем Contoso17.

## ПАРАМЕТРЫ

### -AutomationAccountName
Указывает имя учетной записи автоматизации, для которой этот командлет обновляет модуль.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
Задает URL-адрес для файла ZIP, который содержит новую версию модуля, импортируемого этим командлетом.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Указывает версию модуля, для которого этот командлет обновляет автоматизацию.

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

### -Name (имя)
Указывает имя модуля, который импортирует этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, для которой этот командлет обновляет модуль.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. Automation. Model. Module

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[New-AzureRmAutomationModule](./New-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)


