---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015302"
---
# <span data-ttu-id="5915a-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5915a-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="5915a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5915a-102">SYNOPSIS</span></span>
<span data-ttu-id="5915a-103">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="5915a-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="5915a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5915a-104">SYNTAX</span></span>

### <span data-ttu-id="5915a-105">RepairExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5915a-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5915a-106">Javítás</span><span class="sxs-lookup"><span data-stu-id="5915a-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5915a-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5915a-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5915a-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5915a-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5915a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5915a-109">DESCRIPTION</span></span>
<span data-ttu-id="5915a-110">A fürt egy csomópontjának kijavítása.</span><span class="sxs-lookup"><span data-stu-id="5915a-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="5915a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5915a-111">EXAMPLES</span></span>

### <span data-ttu-id="5915a-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="5915a-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="5915a-113">A Scale Unit csomópont kijavítása.</span><span class="sxs-lookup"><span data-stu-id="5915a-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="5915a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5915a-114">PARAMETERS</span></span>

### <span data-ttu-id="5915a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5915a-115">-AsJob</span></span>
<span data-ttu-id="5915a-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5915a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5915a-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="5915a-117">-BareMetalNode</span></span>
<span data-ttu-id="5915a-118">A fürtök ScaleOut műveletéhez használt csupasz fém csomópont leírása.</span><span class="sxs-lookup"><span data-stu-id="5915a-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="5915a-119">A kivitelezéshez tekintse meg a BAREMETALNODE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5915a-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5915a-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="5915a-120">-BiosVersion</span></span>
<span data-ttu-id="5915a-121">A fizikai gép BIOS-verziója.</span><span class="sxs-lookup"><span data-stu-id="5915a-121">Bios version of the physical machine.</span></span>

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

### <span data-ttu-id="5915a-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="5915a-122">-BmciPv4Address</span></span>
<span data-ttu-id="5915a-123">A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="5915a-123">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="5915a-124">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="5915a-124">-ClusterName</span></span>
<span data-ttu-id="5915a-125">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-125">Name of the cluster.</span></span>

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

### <span data-ttu-id="5915a-126">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="5915a-126">-ComputerName</span></span>
<span data-ttu-id="5915a-127">A számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-127">Name of the computer.</span></span>

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

### <span data-ttu-id="5915a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5915a-128">-DefaultProfile</span></span>
<span data-ttu-id="5915a-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5915a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5915a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5915a-130">-Force</span></span>
<span data-ttu-id="5915a-131">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5915a-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5915a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5915a-132">-InputObject</span></span>
<span data-ttu-id="5915a-133">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5915a-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5915a-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="5915a-134">-Location</span></span>
<span data-ttu-id="5915a-135">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5915a-135">Location of the resource.</span></span>

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

### <span data-ttu-id="5915a-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="5915a-136">-MacAddress</span></span>
<span data-ttu-id="5915a-137">A csupasz fém csomópont MAC-címének neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-137">Name of the MAC address of the bare metal node.</span></span>

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

### <span data-ttu-id="5915a-138">– Modell</span><span class="sxs-lookup"><span data-stu-id="5915a-138">-Model</span></span>
<span data-ttu-id="5915a-139">A fizikai gép mintája.</span><span class="sxs-lookup"><span data-stu-id="5915a-139">Model of the physical machine.</span></span>

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

### <span data-ttu-id="5915a-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5915a-140">-Name</span></span>
<span data-ttu-id="5915a-141">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="5915a-141">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="5915a-142">-Várva</span><span class="sxs-lookup"><span data-stu-id="5915a-142">-NoWait</span></span>
<span data-ttu-id="5915a-143">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5915a-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5915a-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5915a-144">-PassThru</span></span>
<span data-ttu-id="5915a-145">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="5915a-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5915a-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5915a-146">-ResourceGroupName</span></span>
<span data-ttu-id="5915a-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="5915a-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="5915a-148">-SerialNumber</span></span>
<span data-ttu-id="5915a-149">A fizikai gép sorozatszáma.</span><span class="sxs-lookup"><span data-stu-id="5915a-149">Serial number of the physical machine.</span></span>

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

### <span data-ttu-id="5915a-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5915a-150">-SubscriptionId</span></span>
<span data-ttu-id="5915a-151">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5915a-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5915a-152">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5915a-152">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5915a-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="5915a-153">-Vendor</span></span>
<span data-ttu-id="5915a-154">A fizikai gép szállítója.</span><span class="sxs-lookup"><span data-stu-id="5915a-154">Vendor of the physical machine.</span></span>

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

### <span data-ttu-id="5915a-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5915a-155">-Confirm</span></span>
<span data-ttu-id="5915a-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5915a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5915a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5915a-157">-WhatIf</span></span>
<span data-ttu-id="5915a-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5915a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5915a-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5915a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5915a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5915a-160">CommonParameters</span></span>
<span data-ttu-id="5915a-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5915a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5915a-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5915a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5915a-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5915a-163">INPUTS</span></span>

### <span data-ttu-id="5915a-164">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="5915a-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="5915a-165">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5915a-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5915a-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5915a-166">OUTPUTS</span></span>

### <span data-ttu-id="5915a-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5915a-167">System.Boolean</span></span>



## <span data-ttu-id="5915a-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5915a-168">NOTES</span></span>

<span data-ttu-id="5915a-169">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5915a-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5915a-170">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5915a-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5915a-171">BAREMETALNODE <IBareMetalNodeDescription> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5915a-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="5915a-172">`[BiosVersion <String>]`: A fizikai gép BIOS-verziója.</span><span class="sxs-lookup"><span data-stu-id="5915a-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="5915a-173">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="5915a-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="5915a-174">`[ClusterName <String>]`: A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="5915a-175">`[ComputerName <String>]`: A számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="5915a-176">`[MacAddress <String>]`: A csupasz fém csomópont MAC-címének neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="5915a-177">`[Model <String>]`: A fizikai gép mintája.</span><span class="sxs-lookup"><span data-stu-id="5915a-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="5915a-178">`[SerialNumber <String>]`: A fizikai gép sorozatszáma.</span><span class="sxs-lookup"><span data-stu-id="5915a-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="5915a-179">`[Vendor <String>]`: A fizikai gép szállítója.</span><span class="sxs-lookup"><span data-stu-id="5915a-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="5915a-180">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5915a-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5915a-181">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5915a-182">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5915a-183">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5915a-184">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="5915a-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5915a-185">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5915a-186">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5915a-187">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5915a-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5915a-188">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5915a-189">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5915a-190">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5915a-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5915a-191">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5915a-192">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5915a-193">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5915a-194">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="5915a-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5915a-195">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5915a-196">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5915a-197">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5915a-198">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5915a-199">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="5915a-200">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5915a-201">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5915a-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5915a-202">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5915a-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5915a-203">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="5915a-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5915a-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5915a-204">RELATED LINKS</span></span>

