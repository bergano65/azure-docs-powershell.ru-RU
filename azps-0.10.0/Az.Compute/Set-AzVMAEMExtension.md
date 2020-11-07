---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 87d7ff04b62bcee2e735dacbbdd9ddb3ab04d425
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911354"
---
# Set-AzVMAEMExtension

## КРАТКИй обзор
Обеспечивает поддержку наблюдения для систем SAP.

## Максимальное

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzVMAEMExtension** обновляет конфигурацию виртуальной машины, чтобы включить или обновить поддержку наблюдения для систем SAP, установленных на виртуальной машине.
Командлет устанавливает расширение службы улучшенного мониторинга Azure (AEM), которое собирает данные о производительности и делает его обнаруживаемым для системы SAP.

## ИЛЛЮСТРИРУЮТ

### Пример 1: использование расширения AEM
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Эта команда настраивает виртуальную машину с именем Contoso-Server на использование расширения AEM.
Команда задает учетную запись хранения с именем stdstorage.

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

### -DisableWAD
Указывает на то, что этот командлет не включает диагностику Azure для виртуальной машины.

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

### -EnableWAD
Если этот параметр указан, unifiedgroup включит диагностику Windows Azure для этой виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Указывает тип операционной системы диска операционной системы.
Если диск операционной системы не имеет типа, необходимо указать этот параметр.
Допустимые значения этого параметра: Windows и Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины, которую изменяет этот командлет.

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

### -SkipStorage
Указывает на то, что этот командлет пропускает конфигурацию хранилища.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины.
Этот командлет добавляет расширение AEM для виртуальной машины, указывающей этот параметр.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Указывает имя учетной записи хранения, которую этот командлет использует для настройки расширения LinuxDiagnostics или IaaSDiagnostics.
Если виртуальная машина не использует стандартную учетную запись хранения, необходимо указать значение для этого параметра.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzVMAEMExtension](./Get-AzVMAEMExtension.md)

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Test-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


