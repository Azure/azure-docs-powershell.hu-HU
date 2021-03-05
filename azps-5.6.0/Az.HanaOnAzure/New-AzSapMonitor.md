---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: a13b0a936eeecd1d7a18b18bb8878b79225da030
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013365"
---
# <span data-ttu-id="3e487-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="3e487-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="3e487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e487-102">SYNOPSIS</span></span>
<span data-ttu-id="3e487-103">Sap-monitort hoz létre a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="3e487-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3e487-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e487-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e487-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e487-105">DESCRIPTION</span></span>
<span data-ttu-id="3e487-106">Sap-monitort hoz létre a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="3e487-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3e487-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e487-107">EXAMPLES</span></span>

### <span data-ttu-id="3e487-108">1. példa: Új SAP-monitor</span><span class="sxs-lookup"><span data-stu-id="3e487-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="3e487-109">Ez a parancs SAP-monitort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3e487-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="3e487-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e487-110">PARAMETERS</span></span>

### <span data-ttu-id="3e487-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e487-111">-AsJob</span></span>
<span data-ttu-id="3e487-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="3e487-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3e487-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e487-113">-DefaultProfile</span></span>
<span data-ttu-id="3e487-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e487-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="3e487-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="3e487-116">Az az érték, amely azt jelzi, hogy el kell-e küldeni analitikát a Microsoftnak</span><span class="sxs-lookup"><span data-stu-id="3e487-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="3e487-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3e487-117">-Location</span></span>
<span data-ttu-id="3e487-118">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="3e487-118">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3e487-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="3e487-120">A figyeléshez használt naplóelemzési munkaterület munkaterület-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e487-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="3e487-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3e487-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="3e487-122">A ARM a figyeléshez használt Log Analytics Workspace azonosítószáma</span><span class="sxs-lookup"><span data-stu-id="3e487-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3e487-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="3e487-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="3e487-124">A figyeléshez használt naplóelemzési munkaterület megosztott kulcsa</span><span class="sxs-lookup"><span data-stu-id="3e487-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3e487-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="3e487-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="3e487-126">Az alhálózat, amelyben az SAP-monitor üzembe fog helyezni.</span><span class="sxs-lookup"><span data-stu-id="3e487-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="3e487-127">A HANA-adatbázisnak azonos alhálózatnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3e487-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="3e487-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3e487-128">-Name</span></span>
<span data-ttu-id="3e487-129">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3e487-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e487-130">-NoWait</span></span>
<span data-ttu-id="3e487-131">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="3e487-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e487-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e487-132">-ResourceGroupName</span></span>
<span data-ttu-id="3e487-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e487-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e487-134">-SubscriptionId</span></span>
<span data-ttu-id="3e487-135">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3e487-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e487-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3e487-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e487-137">-Tag</span></span>
<span data-ttu-id="3e487-138">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="3e487-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e487-139">-Confirm</span></span>
<span data-ttu-id="3e487-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e487-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e487-141">-WhatIf</span></span>
<span data-ttu-id="3e487-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e487-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e487-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e487-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e487-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e487-144">CommonParameters</span></span>
<span data-ttu-id="3e487-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e487-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e487-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e487-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e487-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e487-147">INPUTS</span></span>

## <span data-ttu-id="3e487-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e487-148">OUTPUTS</span></span>

### <span data-ttu-id="3e487-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="3e487-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="3e487-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e487-150">NOTES</span></span>

<span data-ttu-id="3e487-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3e487-151">ALIASES</span></span>

## <span data-ttu-id="3e487-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e487-152">RELATED LINKS</span></span>

