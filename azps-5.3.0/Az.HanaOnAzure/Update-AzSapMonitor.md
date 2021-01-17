---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469598"
---
# <span data-ttu-id="be53d-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="be53d-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="be53d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be53d-102">SYNOPSIS</span></span>
<span data-ttu-id="be53d-103">Javítja egy SAP-monitor Címkék mezőjét a megadott előfizetéshez, erőforráscsoporthoz és monitornévhez.</span><span class="sxs-lookup"><span data-stu-id="be53d-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="be53d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be53d-104">SYNTAX</span></span>

### <span data-ttu-id="be53d-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be53d-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be53d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="be53d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be53d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be53d-107">DESCRIPTION</span></span>
<span data-ttu-id="be53d-108">Javítja egy SAP-monitor Címkék mezőjét a megadott előfizetéshez, erőforráscsoporthoz és monitornévhez.</span><span class="sxs-lookup"><span data-stu-id="be53d-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="be53d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be53d-109">EXAMPLES</span></span>

### <span data-ttu-id="be53d-110">1. példa: SAP-monitor frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="be53d-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="be53d-111">Ez a parancs név szerint frissíti az SAP-monitort.</span><span class="sxs-lookup"><span data-stu-id="be53d-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="be53d-112">2. példa: SAP-monitor frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="be53d-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="be53d-113">Ez a parancs objektumról objektumra frissíti az SAP-monitort.</span><span class="sxs-lookup"><span data-stu-id="be53d-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="be53d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be53d-114">PARAMETERS</span></span>

### <span data-ttu-id="be53d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be53d-115">-DefaultProfile</span></span>
<span data-ttu-id="be53d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be53d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be53d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be53d-117">-InputObject</span></span>
<span data-ttu-id="be53d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="be53d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be53d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="be53d-119">-Name</span></span>
<span data-ttu-id="be53d-120">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be53d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be53d-121">-ResourceGroupName</span></span>
<span data-ttu-id="be53d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be53d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be53d-123">-SubscriptionId</span></span>
<span data-ttu-id="be53d-124">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="be53d-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be53d-125">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="be53d-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be53d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="be53d-126">-Tag</span></span>
<span data-ttu-id="be53d-127">Az erőforrás Címkék mezője.</span><span class="sxs-lookup"><span data-stu-id="be53d-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="be53d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be53d-128">-Confirm</span></span>
<span data-ttu-id="be53d-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="be53d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be53d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be53d-130">-WhatIf</span></span>
<span data-ttu-id="be53d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="be53d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be53d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be53d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be53d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be53d-133">CommonParameters</span></span>
<span data-ttu-id="be53d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be53d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be53d-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be53d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be53d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be53d-136">INPUTS</span></span>

### <span data-ttu-id="be53d-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="be53d-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="be53d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be53d-138">OUTPUTS</span></span>

### <span data-ttu-id="be53d-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="be53d-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="be53d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be53d-140">NOTES</span></span>

<span data-ttu-id="be53d-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="be53d-141">ALIASES</span></span>

<span data-ttu-id="be53d-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="be53d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be53d-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="be53d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be53d-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be53d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be53d-145">INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="be53d-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be53d-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="be53d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be53d-147">`[Location <String>]`: A törölt tároló helye.</span><span class="sxs-lookup"><span data-stu-id="be53d-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="be53d-148">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="be53d-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="be53d-149">`[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="be53d-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="be53d-151">`[ResourceName <String>]`: Az identitáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="be53d-152">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="be53d-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="be53d-153">`[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre.</span><span class="sxs-lookup"><span data-stu-id="be53d-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="be53d-154">Felügyelt identitásokkal bővített szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="be53d-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="be53d-155">`[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="be53d-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="be53d-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="be53d-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="be53d-157">`[VaultName <String>]`: A tároló neve</span><span class="sxs-lookup"><span data-stu-id="be53d-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="be53d-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be53d-158">RELATED LINKS</span></span>

