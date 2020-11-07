---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842589"
---
# <span data-ttu-id="13ad3-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="13ad3-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="13ad3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="13ad3-103">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="13ad3-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="13ad3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13ad3-104">SYNTAX</span></span>

### <span data-ttu-id="13ad3-105">RepairExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13ad3-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad3-106">Javítás</span><span class="sxs-lookup"><span data-stu-id="13ad3-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13ad3-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13ad3-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad3-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="13ad3-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13ad3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="13ad3-109">DESCRIPTION</span></span>
<span data-ttu-id="13ad3-110">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="13ad3-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="13ad3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="13ad3-111">EXAMPLES</span></span>

### <span data-ttu-id="13ad3-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="13ad3-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="13ad3-113">A Scale Unit csomópont kijavítása.</span><span class="sxs-lookup"><span data-stu-id="13ad3-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="13ad3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13ad3-114">PARAMETERS</span></span>

### <span data-ttu-id="13ad3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13ad3-115">-AsJob</span></span>
<span data-ttu-id="13ad3-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="13ad3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13ad3-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="13ad3-117">-BareMetalNode</span></span>
<span data-ttu-id="13ad3-118">A fürtök ScaleOut műveletéhez használt csupasz fém csomópont leírása.</span><span class="sxs-lookup"><span data-stu-id="13ad3-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="13ad3-119">A kivitelezéshez tekintse meg a BAREMETALNODE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="13ad3-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="13ad3-120">-BiosVersion</span></span>
<span data-ttu-id="13ad3-121">A fizikai gép BIOS-verziója.</span><span class="sxs-lookup"><span data-stu-id="13ad3-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="13ad3-122">-BmciPv4Address</span></span>
<span data-ttu-id="13ad3-123">A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="13ad3-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-124">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="13ad3-124">-ClusterName</span></span>
<span data-ttu-id="13ad3-125">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-126">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="13ad3-126">-ComputerName</span></span>
<span data-ttu-id="13ad3-127">A számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ad3-128">-DefaultProfile</span></span>
<span data-ttu-id="13ad3-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13ad3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ad3-130">-Force</span><span class="sxs-lookup"><span data-stu-id="13ad3-130">-Force</span></span>
<span data-ttu-id="13ad3-131">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13ad3-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="13ad3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13ad3-132">-InputObject</span></span>
<span data-ttu-id="13ad3-133">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="13ad3-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="13ad3-134">-Location</span></span>
<span data-ttu-id="13ad3-135">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="13ad3-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="13ad3-136">-MacAddress</span></span>
<span data-ttu-id="13ad3-137">A csupasz fém csomópont MAC-címének neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-138">– Modell</span><span class="sxs-lookup"><span data-stu-id="13ad3-138">-Model</span></span>
<span data-ttu-id="13ad3-139">A fizikai gép mintája.</span><span class="sxs-lookup"><span data-stu-id="13ad3-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13ad3-140">-Name</span></span>
<span data-ttu-id="13ad3-141">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="13ad3-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-142">-Várva</span><span class="sxs-lookup"><span data-stu-id="13ad3-142">-NoWait</span></span>
<span data-ttu-id="13ad3-143">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="13ad3-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13ad3-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13ad3-144">-PassThru</span></span>
<span data-ttu-id="13ad3-145">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="13ad3-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="13ad3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ad3-146">-ResourceGroupName</span></span>
<span data-ttu-id="13ad3-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="13ad3-148">-SerialNumber</span></span>
<span data-ttu-id="13ad3-149">A fizikai gép sorozatszáma.</span><span class="sxs-lookup"><span data-stu-id="13ad3-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13ad3-150">-SubscriptionId</span></span>
<span data-ttu-id="13ad3-151">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="13ad3-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="13ad3-152">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="13ad3-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="13ad3-153">-Vendor</span></span>
<span data-ttu-id="13ad3-154">A fizikai gép szállítója.</span><span class="sxs-lookup"><span data-stu-id="13ad3-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13ad3-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13ad3-155">-Confirm</span></span>
<span data-ttu-id="13ad3-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13ad3-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ad3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ad3-157">-WhatIf</span></span>
<span data-ttu-id="13ad3-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13ad3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ad3-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13ad3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ad3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ad3-160">CommonParameters</span></span>
<span data-ttu-id="13ad3-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13ad3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ad3-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13ad3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ad3-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ad3-163">INPUTS</span></span>

### <span data-ttu-id="13ad3-164">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="13ad3-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="13ad3-165">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="13ad3-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="13ad3-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ad3-166">OUTPUTS</span></span>

### <span data-ttu-id="13ad3-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13ad3-167">System.Boolean</span></span>



## <span data-ttu-id="13ad3-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13ad3-168">NOTES</span></span>

<span data-ttu-id="13ad3-169">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="13ad3-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13ad3-170">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="13ad3-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="13ad3-171">BAREMETALNODE <IBareMetalNodeDescription> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="13ad3-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="13ad3-172">`[BiosVersion <String>]`: A fizikai gép BIOS-verziója.</span><span class="sxs-lookup"><span data-stu-id="13ad3-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="13ad3-173">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="13ad3-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="13ad3-174">`[ClusterName <String>]`: A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="13ad3-175">`[ComputerName <String>]`: A számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="13ad3-176">`[MacAddress <String>]`: A csupasz fém csomópont MAC-címének neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="13ad3-177">`[Model <String>]`: A fizikai gép mintája.</span><span class="sxs-lookup"><span data-stu-id="13ad3-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="13ad3-178">`[SerialNumber <String>]`: A fizikai gép sorozatszáma.</span><span class="sxs-lookup"><span data-stu-id="13ad3-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="13ad3-179">`[Vendor <String>]`: A fizikai gép szállítója.</span><span class="sxs-lookup"><span data-stu-id="13ad3-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="13ad3-180">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="13ad3-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13ad3-181">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="13ad3-182">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="13ad3-183">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="13ad3-184">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="13ad3-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="13ad3-185">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="13ad3-186">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="13ad3-187">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="13ad3-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13ad3-188">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="13ad3-189">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="13ad3-190">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="13ad3-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="13ad3-191">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="13ad3-192">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="13ad3-193">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="13ad3-194">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="13ad3-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="13ad3-195">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="13ad3-196">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="13ad3-197">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="13ad3-198">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="13ad3-199">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="13ad3-200">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="13ad3-201">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="13ad3-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="13ad3-202">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="13ad3-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="13ad3-203">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="13ad3-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="13ad3-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13ad3-204">RELATED LINKS</span></span>

