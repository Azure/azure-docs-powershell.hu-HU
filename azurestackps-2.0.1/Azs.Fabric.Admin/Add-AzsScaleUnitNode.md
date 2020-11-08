---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015379"
---
# <span data-ttu-id="9029e-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9029e-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9029e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9029e-102">SYNOPSIS</span></span>
<span data-ttu-id="9029e-103">Méretarány mértékegysége</span><span class="sxs-lookup"><span data-stu-id="9029e-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="9029e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9029e-104">SYNTAX</span></span>

### <span data-ttu-id="9029e-105">ScaleExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9029e-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9029e-106">Méretarány</span><span class="sxs-lookup"><span data-stu-id="9029e-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9029e-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9029e-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9029e-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9029e-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9029e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9029e-109">DESCRIPTION</span></span>
<span data-ttu-id="9029e-110">Méretarány mértékegysége</span><span class="sxs-lookup"><span data-stu-id="9029e-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="9029e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9029e-111">EXAMPLES</span></span>

### <span data-ttu-id="9029e-112">Példa 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9029e-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="9029e-113">Adjon hozzá egy új méretarányos csomópontot a méretarányos fürthöz.</span><span class="sxs-lookup"><span data-stu-id="9029e-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="9029e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9029e-114">PARAMETERS</span></span>

### <span data-ttu-id="9029e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9029e-115">-AsJob</span></span>
<span data-ttu-id="9029e-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9029e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9029e-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="9029e-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="9029e-118">A jelölő jelzi, ha a műveletnek a tárterületre várnia kell, hogy ne térjen vissza az eredményre.</span><span class="sxs-lookup"><span data-stu-id="9029e-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9029e-119">-DefaultProfile</span></span>
<span data-ttu-id="9029e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9029e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9029e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9029e-121">-InputObject</span></span>
<span data-ttu-id="9029e-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9029e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="9029e-123">-Location</span></span>
<span data-ttu-id="9029e-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="9029e-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="9029e-125">-NodeList</span></span>
<span data-ttu-id="9029e-126">Csomópontok listája a méretarányt tartalmazó egységben.</span><span class="sxs-lookup"><span data-stu-id="9029e-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="9029e-127">A kivitelezéshez tekintse meg a NODELIST tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9029e-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="9029e-128">-NoWait</span></span>
<span data-ttu-id="9029e-129">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9029e-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9029e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9029e-130">-PassThru</span></span>
<span data-ttu-id="9029e-131">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="9029e-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9029e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9029e-132">-ResourceGroupName</span></span>
<span data-ttu-id="9029e-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="9029e-134">-ScaleUnit</span></span>
<span data-ttu-id="9029e-135">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="9029e-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="9029e-137">A méretarány-csomópontok készletének hozzáadását lehetővé tevő bemeneti adatok listája.</span><span class="sxs-lookup"><span data-stu-id="9029e-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="9029e-138">A kivitelezéshez tekintse meg a SCALEUNITNODEPARAMETER tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9029e-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9029e-139">-SubscriptionId</span></span>
<span data-ttu-id="9029e-140">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="9029e-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9029e-141">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9029e-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9029e-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9029e-142">-Confirm</span></span>
<span data-ttu-id="9029e-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9029e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9029e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9029e-144">-WhatIf</span></span>
<span data-ttu-id="9029e-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9029e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9029e-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9029e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9029e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9029e-147">CommonParameters</span></span>
<span data-ttu-id="9029e-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9029e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9029e-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9029e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9029e-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9029e-150">INPUTS</span></span>

### <span data-ttu-id="9029e-151">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="9029e-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="9029e-152">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9029e-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9029e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9029e-153">OUTPUTS</span></span>

### <span data-ttu-id="9029e-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9029e-154">System.Boolean</span></span>



## <span data-ttu-id="9029e-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9029e-155">NOTES</span></span>

<span data-ttu-id="9029e-156">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9029e-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9029e-157">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9029e-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9029e-158">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9029e-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9029e-159">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9029e-160">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9029e-161">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9029e-162">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="9029e-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9029e-163">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9029e-164">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9029e-165">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9029e-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9029e-166">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9029e-167">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9029e-168">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="9029e-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9029e-169">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9029e-170">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9029e-171">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9029e-172">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="9029e-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9029e-173">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9029e-174">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9029e-175">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9029e-176">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9029e-177">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9029e-178">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="9029e-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9029e-179">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9029e-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9029e-180">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="9029e-181">NODELIST <IScaleOutScaleUnitParameters [] >: csomópontok listája a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="9029e-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="9029e-182">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="9029e-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="9029e-183">`[ComputerName <String>]`: A fizikai gép számítógépének neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="9029e-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : a méretarányos csomópontok halmazának hozzáadását lehetővé tevő bemeneti adatok listája.</span><span class="sxs-lookup"><span data-stu-id="9029e-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="9029e-185">`[AwaitStorageConvergence <Boolean?>]`: A megjelölés azt jelzi, hogy a művelet csak a tárolás előtt közelíti meg a tárterületet.</span><span class="sxs-lookup"><span data-stu-id="9029e-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="9029e-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: A méretarányban lévő csomópontok listája.</span><span class="sxs-lookup"><span data-stu-id="9029e-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="9029e-187">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="9029e-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="9029e-188">`[ComputerName <String>]`: A fizikai gép számítógépének neve.</span><span class="sxs-lookup"><span data-stu-id="9029e-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="9029e-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9029e-189">RELATED LINKS</span></span>

