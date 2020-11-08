---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187389"
---
# <span data-ttu-id="3347a-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="3347a-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="3347a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3347a-102">SYNOPSIS</span></span>
<span data-ttu-id="3347a-103">A megadott előfizetés, erőforráscsoport és monitor neve melletti SAP-monitor címkék mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347a-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="3347a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3347a-104">SYNTAX</span></span>

### <span data-ttu-id="3347a-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3347a-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3347a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3347a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3347a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3347a-107">DESCRIPTION</span></span>
<span data-ttu-id="3347a-108">A megadott előfizetés, erőforráscsoport és monitor neve melletti SAP-monitor címkék mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3347a-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="3347a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3347a-109">EXAMPLES</span></span>

### <span data-ttu-id="3347a-110">Példa 1: SAP-monitor frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="3347a-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="3347a-111">Ezek a parancsok a SAP-monitorokat név szerint frissítik.</span><span class="sxs-lookup"><span data-stu-id="3347a-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="3347a-112">2. példa: SAP-monitor objektumon keresztüli frissítése</span><span class="sxs-lookup"><span data-stu-id="3347a-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="3347a-113">Ezekkel a parancsokkal frissítheti az SAP-monitort objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="3347a-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="3347a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3347a-114">PARAMETERS</span></span>

### <span data-ttu-id="3347a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3347a-115">-DefaultProfile</span></span>
<span data-ttu-id="3347a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3347a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3347a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3347a-117">-InputObject</span></span>
<span data-ttu-id="3347a-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3347a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3347a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3347a-119">-Name</span></span>
<span data-ttu-id="3347a-120">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="3347a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3347a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3347a-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="3347a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3347a-123">-SubscriptionId</span></span>
<span data-ttu-id="3347a-124">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3347a-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3347a-125">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3347a-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3347a-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="3347a-126">-Tag</span></span>
<span data-ttu-id="3347a-127">Az erőforrás címkék mezője</span><span class="sxs-lookup"><span data-stu-id="3347a-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="3347a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3347a-128">-Confirm</span></span>
<span data-ttu-id="3347a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3347a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3347a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3347a-130">-WhatIf</span></span>
<span data-ttu-id="3347a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3347a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3347a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3347a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3347a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3347a-133">CommonParameters</span></span>
<span data-ttu-id="3347a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3347a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3347a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3347a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3347a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3347a-136">INPUTS</span></span>

### <span data-ttu-id="3347a-137">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="3347a-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="3347a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3347a-138">OUTPUTS</span></span>

### <span data-ttu-id="3347a-139">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. modellek. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="3347a-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="3347a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3347a-140">NOTES</span></span>

<span data-ttu-id="3347a-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3347a-141">ALIASES</span></span>

<span data-ttu-id="3347a-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3347a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3347a-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3347a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3347a-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3347a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3347a-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3347a-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3347a-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3347a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3347a-147">`[Location <String>]`: A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="3347a-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="3347a-148">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="3347a-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="3347a-149">`[ProviderInstanceName <String>]`: A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="3347a-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3347a-151">`[ResourceName <String>]`: Az identitás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="3347a-152">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3347a-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="3347a-153">`[Scope <String>]`: Az erőforrás-szolgáltató hatóköre.</span><span class="sxs-lookup"><span data-stu-id="3347a-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="3347a-154">A fölérendelt erőforrás a felügyelt identitások segítségével meghosszabbodik.</span><span class="sxs-lookup"><span data-stu-id="3347a-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="3347a-155">`[SubscriptionId <String>]`: Az előfizetés azonosítója, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3347a-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3347a-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3347a-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3347a-157">`[VaultName <String>]`: A boltozat neve</span><span class="sxs-lookup"><span data-stu-id="3347a-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="3347a-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3347a-158">RELATED LINKS</span></span>

