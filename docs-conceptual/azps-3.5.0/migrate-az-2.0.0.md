---
title: Руководство по переходу на Az версии 2.0.0
description: Это руководство по переходу содержит список критических изменений, внесенных в выпуск Az версии 2.0 в Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 133769c09f74e1d0d90eff0c6c4bdbb90d1ebe24
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477752"
---
# <a name="migration-guide-for-az-200"></a>Руководство по переходу на Az версии 2.0.0

Этот документ описывает изменения между Az версии 1.0.0 и Az версии 2.0.0. 

## <a name="table-of-contents"></a>Оглавление
- [Критические изменения модуля](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Критические изменения модуля

### <a name="azcompute"></a>Az.Compute

- Параметр `Managed` удален из командлетов `New-AzAvailabilitySet` и `Update-AzAvailabilitySet`. Теперь используется ```Sku = Aligned```.

  #### <a name="before"></a>Перед

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>После

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Для согласованности параметр `Image` удален из наборов параметров ByName и ByResourceId в `Update-AzImage`. 
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр ImageName не используется, поэтому удаление этого параметра не влияет на функциональность.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>После

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Restart-AzVM`.
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>После

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Start-AzVM`.
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>После

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Stop-AzVM`.
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>После

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Remove-AzVM`.
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>После

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Set-AzVM`.
  
  #### <a name="before"></a>Перед

  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>После

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Save-AzVMImage`. 
  
  #### <a name="before"></a>Перед
  Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>После
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- Добавлено свойство ProtectionPolicy для инкапсуляции свойства `ProtectFromScaleIn` в классе `PSVirtualMachineScaleSetVM`.

  #### <a name="before"></a>Перед

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>После

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- Добавлено свойство ```EncryptionSettingsCollection``` для заключения свойства `EncryptionSettings` в классе `PSDisk`.

  #### <a name="before"></a>Перед

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>После

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Добавлено свойство ```EncryptionSettingsCollection``` для заключения свойства `EncryptionSettings` в классе `PSSnapshot`.

  #### <a name="before"></a>Перед

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>После

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Удалено свойство `VirtualMachineProfile` из класса `PSVirtualMachineScaleSet`.

  #### <a name="before"></a>Перед

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>После

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- Для командлета `Set-AzVMBootDiagnostic` удален устаревший псевдоним (ранее — `Set-AzVMBootDiagnostics`).

  #### <a name="before"></a>Перед

  Использование устаревшего псевдонима

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>После

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- Для командлета `Export-AzLogAnalyticThrottledRequest` удален устаревший псевдоним (ранее — `Export-AzLogAnalyticThrottledRequests`).

  #### <a name="before"></a>Перед

  Использование устаревшего псевдонима

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>После

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Удалены командлеты `Grant-AzHDInsightHttpServicesAccess` и `Revoke-AzHDInsightHttpServicesAccess`. Они больше не требуются, потому что доступ по протоколу HTTP всегда включен во всех кластерах HDInsight.
- Добавлен новый командлет `Set-AzHDInsightGatewayCredential`. С помощью этого командлета можно изменить имя пользователя и пароль HTTP шлюза (заменяет `Grant-AzHDInsightHttpServicesAccess`).
- Обновлен командлет `Get-AzHDInsightJobOutput` для поддержки детализированного доступа на основе ролей к ключу к хранилищу.
    - На пользователей с ролями оператора, участника или владельца кластера HDInsight это не повлияет.
    - Только пользователям с ролью читателя нужно указывать параметр `DefaultStorageAccountKey` явным образом.

Дополнительные сведения об этих изменениях доступа на основе ролей см. по адресу [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update).

  #### <a name="before"></a>Перед

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>После

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Пользователи только с ролью читателя для командлета Get-AzHDInsightJobOutput

  ####  <a name="before"></a>Перед

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>После

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Пространства имен для типов, возвращаемых командлетами, выполняющими действия с большими двоичными объектами, очередями и файлами, были изменены с `Microsoft.WindowsAzure.Storage` на `Microsoft.Azure.Storage`.  Хотя согласно политике критических изменений технически это не является критическим изменением, для взаимодействия с объектами, возвращаемыми этими командлетами, может потребоваться внести некоторые изменения в код, использующий методы из пакета SDK .NET для службы хранилища.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Пример 1:  Добавление сообщения в очередь (изменение пространства имен объекта CloudQueueMessage)

  Перед следующей операцией. 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  После следующих операций.

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Пример 2.  Получение атрибутов файла или большого двоичного объекта с условием AccessCondition (изменение пространства имен объекта AccessCondition)

  Перед следующей операцией. 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  После следующих операций.

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Хотя технически это не является критическим изменением, вы обнаружите различия в значениях свойства SKU.Name учетных записей хранения в выходных данных, возвращенных из `New/Get/Set-AzStorageAccount`. Ниже приведены эти изменения. (После изменения значения SkuName в выходных и входных данных согласовываются.)
  - "StandardLRS" -> "Standard_LRS".
  - "StandardGRS" -> "Standard_GRS".
  - "StandardRAGRS" -> "Standard_RAGRS".
  - "StandardZRS" -> "Standard_ZRS".
  - "PremiumLRS" -> "Premium_LRS".

- Изменено поведение службы по умолчанию при создании учетной записи хранения без указания параметра Kind.  В предыдущих версиях при создании учетной записи хранения без указания параметра `Kind` использовался тип `Storage`. В новой версии значением параметра `Kind` по умолчанию является `StorageV2`. Если вам нужно создать учетную запись хранения версии 1 с параметром Kind со значением Storage, добавьте параметр -Kind Storage.

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Пример. Создание учетной записи хранения (изменение значения Kind по умолчанию)  

  Перед следующей операцией.

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  После следующих операций.

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
