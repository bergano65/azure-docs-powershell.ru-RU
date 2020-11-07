---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911384"
---
# Save-AzVMImage

## КРАТКИй обзор
Сохранение виртуальной машины в виде VMImage.

## Максимальное

### ResourceGroupNameParameterSetName (по умолчанию)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Save-AzVMImage** сохраняет виртуальную машину как VMImage.
Перед созданием образа виртуальной машины выполните команду Sysprep для виртуальной машины, а затем пометьте ее как обобщенную с помощью командлета Set-AzVM.

Результатом этого командлета является шаблон JSON (объектная нотация).
Вы можете развернуть виртуальные машины из записанного образа.

## ИЛЛЮСТРИРУЮТ

### Пример 1: запись виртуальной машины
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

Первая команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.

Вторая команда перехватывает виртуальную машину с именем VirtualMachine07 как VMImage.
Свойство **Output** ВОЗВРАЩАЕТ шаблон JSON.

## ПАРАМЕТРЫ

### -AsJob
Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.

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

### -DestinationContainerName
Указывает имя контейнера в контейнере System, который вы хотите хранить для изображений.

Если контейнер не существует, он создается для вас.
Виртуальные жесткие диски (VHD), составляющие VMImage, находятся в контейнере, указанном в этом параметре.
Если виртуальные жесткие диски распределены между несколькими учетными записями хранения, этот командлет создает один контейнер с этим именем в каждой учетной записи хранения.
URL-адрес сохраненного изображения подобен: 

HTTPS:// \< storageAccountName \> . BLOB.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.

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

### -ID
Указывает идентификатор ресурса виртуальной машины.

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Задает имя.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Указывает на то, что этот командлет перезаписывает все виртуальные жесткие диски с таким же префиксом в конечном контейнере.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Указывает путь к виртуальному жесткому диску.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
Указывает префикс в имени больших двоичных объектов, составляющих профиль хранилища для VMImage.

Например, префикс vhdPrefix для диска операционной системы приводит к имени vhdPrefix-osdisk. \< GUID \> . VHD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


