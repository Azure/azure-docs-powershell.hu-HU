---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184517"
---
# <span data-ttu-id="fefa3-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="fefa3-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="fefa3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fefa3-102">SYNOPSIS</span></span>
<span data-ttu-id="fefa3-103">SAP-monitort hoz létre a megadott előfizetéshez, erőforrás csoporthoz és erőforrás nevéhez.</span><span class="sxs-lookup"><span data-stu-id="fefa3-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="fefa3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fefa3-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fefa3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fefa3-105">DESCRIPTION</span></span>
<span data-ttu-id="fefa3-106">SAP-monitort hoz létre a megadott előfizetéshez, erőforrás csoporthoz és erőforrás nevéhez.</span><span class="sxs-lookup"><span data-stu-id="fefa3-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="fefa3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fefa3-107">EXAMPLES</span></span>

### <span data-ttu-id="fefa3-108">1. példa: új SAP-monitor</span><span class="sxs-lookup"><span data-stu-id="fefa3-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="fefa3-109">A parancs SAP-monitort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fefa3-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="fefa3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fefa3-110">PARAMETERS</span></span>

### <span data-ttu-id="fefa3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fefa3-111">-AsJob</span></span>
<span data-ttu-id="fefa3-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="fefa3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fefa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefa3-113">-DefaultProfile</span></span>
<span data-ttu-id="fefa3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fefa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fefa3-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="fefa3-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="fefa3-116">Az az érték, amely azt jelzi, hogy az elemzést elküldi-e a Microsoftnak</span><span class="sxs-lookup"><span data-stu-id="fefa3-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="fefa3-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="fefa3-117">-Location</span></span>
<span data-ttu-id="fefa3-118">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="fefa3-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fefa3-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="fefa3-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="fefa3-120">A figyeléshez használni kívánt log Analytics-munkaterület munkaterület-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fefa3-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="fefa3-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fefa3-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="fefa3-122">A figyeléshez használt log Analytics-munkaterület ARM azonosítója</span><span class="sxs-lookup"><span data-stu-id="fefa3-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="fefa3-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="fefa3-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="fefa3-124">A figyeléshez használt log Analytics-munkaterület megosztott kulcsa</span><span class="sxs-lookup"><span data-stu-id="fefa3-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="fefa3-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="fefa3-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="fefa3-126">Az a hálózat, amelybe az SAP-monitort telepíteni fogják.</span><span class="sxs-lookup"><span data-stu-id="fefa3-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="fefa3-127">Ugyanannak a HANA-adatbázisnak ugyanannak a alhálózatának kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fefa3-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="fefa3-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fefa3-128">-Name</span></span>
<span data-ttu-id="fefa3-129">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fefa3-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="fefa3-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="fefa3-130">-NoWait</span></span>
<span data-ttu-id="fefa3-131">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="fefa3-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fefa3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefa3-132">-ResourceGroupName</span></span>
<span data-ttu-id="fefa3-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fefa3-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="fefa3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fefa3-134">-SubscriptionId</span></span>
<span data-ttu-id="fefa3-135">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="fefa3-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fefa3-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="fefa3-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fefa3-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="fefa3-137">-Tag</span></span>
<span data-ttu-id="fefa3-138">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="fefa3-138">Resource tags.</span></span>

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

### <span data-ttu-id="fefa3-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fefa3-139">-Confirm</span></span>
<span data-ttu-id="fefa3-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fefa3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fefa3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fefa3-141">-WhatIf</span></span>
<span data-ttu-id="fefa3-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fefa3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fefa3-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fefa3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fefa3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefa3-144">CommonParameters</span></span>
<span data-ttu-id="fefa3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fefa3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefa3-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fefa3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefa3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fefa3-147">INPUTS</span></span>

## <span data-ttu-id="fefa3-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fefa3-148">OUTPUTS</span></span>

### <span data-ttu-id="fefa3-149">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. modellek. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="fefa3-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="fefa3-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fefa3-150">NOTES</span></span>

<span data-ttu-id="fefa3-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fefa3-151">ALIASES</span></span>

## <span data-ttu-id="fefa3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fefa3-152">RELATED LINKS</span></span>

