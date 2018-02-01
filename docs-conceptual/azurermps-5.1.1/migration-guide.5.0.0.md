# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Критические изменения для Microsoft Azure PowerShell 5.0.0

Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell. В каждом разделе описана причина критического изменения и самый простой путь миграции. Подробное описание см. в запросах на вытягивание для каждого изменения.

## <a name="table-of-contents"></a>Оглавление

- [Критические изменения в командлетах ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
- [Критические изменения в командлетах Batch](#breaking-changes-to-batch-cmdlets)
- [Критические изменения в командлетах Compute](#breaking-changes-to-compute-cmdlets)
- [Критические изменения в командлетах EventHub](#breaking-changes-to-eventhub-cmdlets)
- [Критические изменения в командлетах Insights](#breaking-changes-to-insights-cmdlets)
- [Критические изменения в командлетах Network](#breaking-changes-to-network-cmdlets)
- [Критические изменения в командлетах Resources](#breaking-changes-to-resources-cmdlets)
- [Критические изменения в командлетах ServiceBus](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Критические изменения в командлетах ApiManagement

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Параметры UserName и Password заменены на PSCredential.

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Параметр Password заменен на SecureString.

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Критические изменения в командлетах Batch

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Параметр `Password` заменен на SecureString.

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Параметр `Password` заменен на SecureString.

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Параметр `Password` заменен на SecureString.

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Переключатель `RunElevated` удален и заменен на `UserIdentity`.

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- Конструктор `PSMultiInstanceSettings` больше не принимает обязательный параметр `numberOfInstances`. Вместо него он принимает обязательный параметр `coordinationCommandLine`.

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - Удалено свойство `RunElevated` в `PSCloudTask`. Добавлено свойство `UserIdentity` для замены `RunElevated`.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Это также касается свойства `RunElevated` в `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` и `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Несколько типов**

- Свойство `SchedulingError` в `PSExitConditions` переименовано в `PreProcessingError`.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Несколько типов**

- Свойство `SchedulingError` в `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` и `PSTaskExecutionInformation` переименовано в `FailureInformation`.
  - `FailureInformation` возвращается при каждом сбое задачи. Сюда входят все предыдущие случаи ошибок планирования, а также коды завершения задач со значением, отличным от нуля, и ошибки передачи файлов из новой функции выходных файлов.
  - Структура не изменилась, поэтому при использовании этого типа не нужно преобразовывать код.

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Это также касается Get-AzureBatchPool, Get-AzureBatchSubtask и Get-AzureBatchJobPreparationAndReleaseTaskStatus.

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - Параметр `TargetDedicated` удален и заменен на `TargetDedicatedComputeNodes` и `TargetLowPriorityComputeNodes`.
 - Псевдоним `TargetDedicatedComputeNodes` — `TargetDedicated`.

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Это также касается Start AzureBatchPoolResize.

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Свойства `TargetDedicated` и `CurrentDedicated` в `PSCloudPool` переименованы в `TargetDedicatedComputeNodes` и `CurrentDedicatedComputeNodes`.

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**Тип PSCloudPool**

- Параметр `ResizeError` в `PSCloudPool` переименован в `ResizeErrors` и теперь является коллекцией.

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- Свойство `TargetDedicated` в `PSPoolSpecification` переименовано в `TargetDedicatedComputeNodes`.

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - Параметр `Name` удален и заменен на `Path`.
 - Псевдоним `Path` — `Name`.

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Это также касается Get-AzureBatchNodeFileContent и Remove-AzureBatchNodeFile.

### <a name="type-psnodefile"></a>Тип **PSNodeFile**

 - Свойство `Name` в `PSNodeFile` переименовано в `Path`.

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Свойства `PreviousState` и `State` для `PSSubtaskInformation` больше не относятся к типу `TaskState`. Теперь они относятся к типу `SubtaskState`.
  - В отличие от `TaskState`, для `SubtaskState` не устанавливается значение `Active`, так как состояние подзадачи не может иметь значение `Active`.

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Критические изменения в командлетах Compute

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Параметры UserName и Password заменены на PSCredential.

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Критические изменения в командлетах EventHub

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- Командлет New-AzureRmEventHubNamespaceAuthorizationRule удален. Используйте командлет New-AzureRmEventHubAuthorizationRule.
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- Командлет Get-AzureRmEventHubNamespaceAuthorizationRule удален. Используйте командлет Get-AzureRmEventHubAuthorizationRule.
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- Командлет Set-AzureRmEventHubNamespaceAuthorizationRule удален. Используйте командлет Set-AzureRmEventHubAuthorizationRule.
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- Командлет Remove-AzureRmEventHubNamespaceAuthorizationRule удален. Используйте командлет Remove-AzureRmEventHubAuthorizationRule.
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- Командлет New-AzureRmEventHubNamespaceKey удален. Используйте командлет New-AzureRmEventHubKey.
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- Командлет Get-AzureRmEventHubNamespaceKey удален. Используйте командлет Get-AzureRmEventHubKey.
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Свойство Status и Enabled из NamespceAttributes будут удалены. 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Свойства Status и Enabled из NamespceAttributes будут удалены. 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Свойства Status и Enabled из NamespceAttributes будут удалены. 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- Свойство EventHubPath из ConsumerGroupAttributes будет удалено.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- Свойство EventHubPath из ConsumerGroupAttributes будет удалено.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- Свойство EventHubPath из ConsumerGroupAttributes будет удалено.

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Критические изменения в командлетах Insights

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Командлет **Add-AzureRMLogAlertRule** отмечен как нерекомендуемый.
- Начиная с 1 октября этот командлет не будет действовать, так как эта функция заменена на оповещения журнала действий. Дополнительные сведения см. по адресу https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- Командлет **Get AzureRMUsage** отмечен как нерекомендуемый.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Изменение выходных данных: поле EventChannels из объекта EventData (возвращаемое этими командлетами) отмечено как нерекомендуемое, так как теперь возвращается константа (Admin, Operation).

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Изменение выходных данных: выходные данные командлета будут преобразованы в плоскую структуру, т. е. будет исключено поле свойств, чтобы повысить удобство работы для пользователей.

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Изменение выходных данных: поле AutoscaleSettingResourceName будет отмечено как нерекомендуемое, так как оно всегда будет иметь значение, аналогичное установленному в поле Name.

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Изменение выходных данных: тип выходных данных будет изменен. Будет возвращаться один объект с идентификатором запроса и кодом состояния.

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Критические изменения в командлетах Network

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Параметр Password заменен на SecureString.

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Параметр Password заменен на SecureString.

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Критические изменения в командлетах Resources

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Параметр Password заменен на SecureString.

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Параметр Password заменен на SecureString.

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Критические изменения в командлетах ServiceBus

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- Командлет Get-AzureRmServiceBusTopicAuthorizationRule удален. Используйте командлет Get-AzureRmServiceBusAuthorizationRule.    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- Командлет Get-AzureRmServiceBusTopicKey удален. Используйте командлет Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- Командлет New-AzureRmServiceBusTopicAuthorizationRule удален. Используйте командлет New-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- Командлет New-AzureRmServiceBusTopicKey удален. Используйте командлет New-AzureRmServiceBusKey.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- Командлет Remove-AzureRmServiceBusTopicAuthorizationRule удален. Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- Командлет Set-AzureRmServiceBusTopicAuthorizationRule удален. Используйте командлет Set-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- Командлет New-AzureRmServiceBusNamespaceKey удален. Используйте командлет New-AzureRmServiceBusKey.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- Командлет Get-AzureRmServiceBusQueueAuthorizationRule удален. Используйте командлет Get-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- Командлет Get-AzureRmServiceBusQueueKey удален. Используйте командлет Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- Командлет New-AzureRmServiceBusQueueAuthorizationRule удален. Используйте командлет New-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- Командлет New-AzureRmServiceBusQueueKey удален. Используйте командлет New-AzureRmServiceBusKey.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- Командлет Remove-AzureRmServiceBusQueueAuthorizationRule удален. Используйте командлет GRemove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- Командлет Set-AzureRmServiceBusQueueAuthorizationRule удален. Используйте командлет Set-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- Командлет Get-AzureRmServiceBusNamespaceAuthorizationRule удален. Используйте командлет Get-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- Командлет Get-AzureRmServiceBusNamespaceKey удален. Используйте командлет Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- Командлет New-AzureRmServiceBusNamespaceAuthorizationRule удален. Используйте командлет New-AzureRmServiceBusAuthorizationRule.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- Командлет Remove-AzureRmServiceBusNamespaceAuthorizationRule удален. Используйте командлет Remove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- Командлет Set-AzureRmServiceBusNamespaceAuthorizationRule удален. Используйте командлет Set-AzureRmServiceBusAuthorizationRule.

### <a name="type-namespaceattributes"></a>**Тип NamespaceAttributes**
- Следующие свойства удалены:
    - Включено
    - Status
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**Тип QueueAttribute**
- Следующие свойства отмечены как устаревшие:
    - EnableBatchedOperations
    - EntityAvailabilityStatus.
    - IsAnonymousAccessible;
    - SupportOrdering.

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a>**Тип TopicAttribute**
- Следующие свойства отмечены как устаревшие:
    - Расположение
    - IsExpress;
    - IsAnonymousAccessible;
    - FilteringMessagesBeforePublishing;
    - EnableSubscriptionPartitioning;
    - EntityAvailabilityStatus.

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a>**Тип SubscriptionAttribute**
- Следующие свойства отмечены как устаревшие:
    - DeadLetteringOnFilterEvaluationExceptions;
    - EntityAvailabilityStatus.
    - IsReadOnly
    - Расположение
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```