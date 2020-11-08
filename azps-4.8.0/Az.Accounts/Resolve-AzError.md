---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/resolve-azerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Resolve-AzError.md
ms.openlocfilehash: 446b9e107f49b0032b4905cb9d0beee5160d3733
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025002"
---
# <span data-ttu-id="696f0-101">Resolve-AzError</span><span class="sxs-lookup"><span data-stu-id="696f0-101">Resolve-AzError</span></span>

## <span data-ttu-id="696f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="696f0-102">SYNOPSIS</span></span>
<span data-ttu-id="696f0-103">Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.</span><span class="sxs-lookup"><span data-stu-id="696f0-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

## <span data-ttu-id="696f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="696f0-104">SYNTAX</span></span>

### <span data-ttu-id="696f0-105">AnyErrorParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="696f0-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="696f0-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="696f0-106">LastErrorParameterSet</span></span>
```
Resolve-AzError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696f0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="696f0-107">DESCRIPTION</span></span>
<span data-ttu-id="696f0-108">Megoldja és részletezi az aktuális PowerShell-munkamenet hibáit, többek között a parancsfájlokban, a halomban és az összes belső és összesítési kivétellel.</span><span class="sxs-lookup"><span data-stu-id="696f0-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="696f0-109">Az Azure PowerShell-hibák további részleteket nyújtanak a hibakeresési szolgáltatással kapcsolatos hibákról, többek között a hibát okozó kérés és kiszolgálói válasz részletes leírását.</span><span class="sxs-lookup"><span data-stu-id="696f0-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="696f0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="696f0-110">EXAMPLES</span></span>

### <span data-ttu-id="696f0-111">1. példa: az utolsó hiba megoldása</span><span class="sxs-lookup"><span data-stu-id="696f0-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzError -Last

   HistoryId: 3


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="696f0-112">Az utolsó hiba részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="696f0-112">Get details of the last error.</span></span>

### <span data-ttu-id="696f0-113">2. példa: a munkamenet minden hibájának elhárítása</span><span class="sxs-lookup"><span data-stu-id="696f0-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzSubscription}
Line           : Get-AzSubscription
Position       : At line:1 char:1
                 + Get-AzSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="696f0-114">Megtudhatja, hogy milyen hibák történtek az aktuális munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="696f0-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="696f0-115">3. példa: adott hiba megoldása</span><span class="sxs-lookup"><span data-stu-id="696f0-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzStorageAccount}
Line           : Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="696f0-116">A megadott hiba részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="696f0-116">Get details of the specified error.</span></span>

## <span data-ttu-id="696f0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="696f0-117">PARAMETERS</span></span>

### <span data-ttu-id="696f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696f0-118">-DefaultProfile</span></span>
<span data-ttu-id="696f0-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="696f0-119">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="696f0-120">-Hiba</span><span class="sxs-lookup"><span data-stu-id="696f0-120">-Error</span></span>
<span data-ttu-id="696f0-121">Egy vagy több, a megoldandó hibához tartozó rekord.</span><span class="sxs-lookup"><span data-stu-id="696f0-121">One or more error records to resolve.</span></span>  <span data-ttu-id="696f0-122">Ha nincs megadva paraméter, a program a munkamenet minden hibáját megoldja.</span><span class="sxs-lookup"><span data-stu-id="696f0-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696f0-123">-Last</span><span class="sxs-lookup"><span data-stu-id="696f0-123">-Last</span></span>
<span data-ttu-id="696f0-124">Csak a munkamenet utolsó hibájának feloldása.</span><span class="sxs-lookup"><span data-stu-id="696f0-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696f0-125">CommonParameters</span></span>
<span data-ttu-id="696f0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="696f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696f0-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="696f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696f0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="696f0-128">INPUTS</span></span>

### <span data-ttu-id="696f0-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="696f0-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="696f0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="696f0-130">OUTPUTS</span></span>

### <span data-ttu-id="696f0-131">Microsoft. Azure. Command. profil. errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="696f0-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="696f0-132">Microsoft. Azure. Command. profil. errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="696f0-132">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="696f0-133">Microsoft. Azure. Command. profil. errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="696f0-133">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="696f0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="696f0-134">NOTES</span></span>

## <span data-ttu-id="696f0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="696f0-135">RELATED LINKS</span></span>
