---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016884"
---
# <span data-ttu-id="b93bb-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="b93bb-101">New-AzsIPPool</span></span>

## <span data-ttu-id="b93bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b93bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b93bb-103">IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b93bb-103">Create an IP pool.</span></span>
<span data-ttu-id="b93bb-104">Miután létrehozta az IP-készletet, nem lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="b93bb-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="b93bb-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b93bb-105">SYNTAX</span></span>

### <span data-ttu-id="b93bb-106">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b93bb-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b93bb-107">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="b93bb-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b93bb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b93bb-108">DESCRIPTION</span></span>
<span data-ttu-id="b93bb-109">IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b93bb-109">Create an IP pool.</span></span>
<span data-ttu-id="b93bb-110">Miután létrehozta az IP-készletet, nem lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="b93bb-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="b93bb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b93bb-111">EXAMPLES</span></span>

### <span data-ttu-id="b93bb-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="b93bb-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="b93bb-113">Új IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b93bb-113">Create a new IP pool.</span></span>



## <span data-ttu-id="b93bb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b93bb-114">PARAMETERS</span></span>

### <span data-ttu-id="b93bb-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b93bb-115">-AddressPrefix</span></span>
<span data-ttu-id="b93bb-116">A cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="b93bb-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b93bb-117">-AsJob</span></span>
<span data-ttu-id="b93bb-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="b93bb-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b93bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93bb-119">-DefaultProfile</span></span>
<span data-ttu-id="b93bb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b93bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b93bb-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b93bb-121">-EndIPAddress</span></span>
<span data-ttu-id="b93bb-122">A záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="b93bb-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="b93bb-123">-Location</span></span>
<span data-ttu-id="b93bb-124">Az a terület, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="b93bb-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b93bb-125">-Name</span></span>
<span data-ttu-id="b93bb-126">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="b93bb-126">IP pool name.</span></span>

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

### <span data-ttu-id="b93bb-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="b93bb-127">-NoWait</span></span>
<span data-ttu-id="b93bb-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="b93bb-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b93bb-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="b93bb-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="b93bb-130">Az aktuálisan lefoglalt IP-címek száma.</span><span class="sxs-lookup"><span data-stu-id="b93bb-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="b93bb-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="b93bb-132">Az IP-címek teljes száma.</span><span class="sxs-lookup"><span data-stu-id="b93bb-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="b93bb-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="b93bb-134">Az IP-címek jelenlegi száma az áttűnésben.</span><span class="sxs-lookup"><span data-stu-id="b93bb-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-135">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="b93bb-135">-Pool</span></span>
<span data-ttu-id="b93bb-136">Ez az erőforrás azt határozza meg, hogy az IP-címek tartománya milyen címekhez van hozzárendelve egy alhálózaton belül.</span><span class="sxs-lookup"><span data-stu-id="b93bb-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="b93bb-137">A kivitelezéshez lásd: jegyzetek szakasz a készlet tulajdonságaihoz, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b93bb-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93bb-138">-ResourceGroupName</span></span>
<span data-ttu-id="b93bb-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b93bb-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b93bb-140">-StartIPAddress</span></span>
<span data-ttu-id="b93bb-141">A kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="b93bb-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b93bb-142">-SubscriptionId</span></span>
<span data-ttu-id="b93bb-143">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b93bb-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b93bb-144">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b93bb-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b93bb-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="b93bb-145">-Tag</span></span>
<span data-ttu-id="b93bb-146">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="b93bb-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b93bb-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b93bb-147">-Confirm</span></span>
<span data-ttu-id="b93bb-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b93bb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93bb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93bb-149">-WhatIf</span></span>
<span data-ttu-id="b93bb-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b93bb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b93bb-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b93bb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93bb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93bb-152">CommonParameters</span></span>
<span data-ttu-id="b93bb-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b93bb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93bb-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b93bb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93bb-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b93bb-155">INPUTS</span></span>

### <span data-ttu-id="b93bb-156">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="b93bb-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="b93bb-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b93bb-157">OUTPUTS</span></span>

### <span data-ttu-id="b93bb-158">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="b93bb-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="b93bb-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b93bb-159">NOTES</span></span>

<span data-ttu-id="b93bb-160">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b93bb-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b93bb-161">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b93bb-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b93bb-162">POOL (POOL) <IIPPool> : ez az erőforrás azt határozza meg, hogy az IP-címek tartománya milyen címekhez van hozzárendelve egy alhálózaton belül.</span><span class="sxs-lookup"><span data-stu-id="b93bb-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="b93bb-163">`[Location <String>]`: Az a terület, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="b93bb-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="b93bb-164">`[Tag <IResourceTags>]`: A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="b93bb-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="b93bb-165">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="b93bb-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b93bb-166">`[AddressPrefix <String>]`: A cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="b93bb-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="b93bb-167">`[EndIPAddress <String>]`: A záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="b93bb-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="b93bb-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Az aktuálisan lefoglalt IP-címek száma.</span><span class="sxs-lookup"><span data-stu-id="b93bb-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="b93bb-169">`[NumberOfIPAddresses <Int64?>]`: Az IP-címek teljes száma.</span><span class="sxs-lookup"><span data-stu-id="b93bb-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="b93bb-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Az IP-címek aktuális száma az áttűnésben.</span><span class="sxs-lookup"><span data-stu-id="b93bb-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="b93bb-171">`[StartIPAddress <String>]`: A kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="b93bb-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="b93bb-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b93bb-172">RELATED LINKS</span></span>

