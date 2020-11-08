---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016713"
---
# <span data-ttu-id="301d2-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="301d2-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="301d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="301d2-102">SYNOPSIS</span></span>
<span data-ttu-id="301d2-103">Méretarány mértékegysége</span><span class="sxs-lookup"><span data-stu-id="301d2-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="301d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="301d2-104">SYNTAX</span></span>

### <span data-ttu-id="301d2-105">ScaleExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="301d2-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="301d2-106">Méretarány</span><span class="sxs-lookup"><span data-stu-id="301d2-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="301d2-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="301d2-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="301d2-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="301d2-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="301d2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="301d2-109">DESCRIPTION</span></span>
<span data-ttu-id="301d2-110">Méretarány mértékegysége</span><span class="sxs-lookup"><span data-stu-id="301d2-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="301d2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="301d2-111">EXAMPLES</span></span>

### <span data-ttu-id="301d2-112">Példa 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="301d2-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="301d2-113">Adjon hozzá egy új méretarányos csomópontot a méretarányos fürthöz.</span><span class="sxs-lookup"><span data-stu-id="301d2-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="301d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="301d2-114">PARAMETERS</span></span>

### <span data-ttu-id="301d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="301d2-115">-AsJob</span></span>
<span data-ttu-id="301d2-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="301d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="301d2-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="301d2-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="301d2-118">A jelölő jelzi, ha a műveletnek a tárterületre várnia kell, hogy ne térjen vissza az eredményre.</span><span class="sxs-lookup"><span data-stu-id="301d2-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="301d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301d2-119">-DefaultProfile</span></span>
<span data-ttu-id="301d2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="301d2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301d2-121">-InputObject</span></span>
<span data-ttu-id="301d2-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="301d2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="301d2-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="301d2-123">-Location</span></span>
<span data-ttu-id="301d2-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="301d2-124">Location of the resource.</span></span>

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

### <span data-ttu-id="301d2-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="301d2-125">-BmciPv4Address</span></span> 
<span data-ttu-id="301d2-126">A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="301d2-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="301d2-127">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="301d2-127">-ComputerName</span></span> 
<span data-ttu-id="301d2-128">A fizikai gép számítógépnevét.</span><span class="sxs-lookup"><span data-stu-id="301d2-128">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="301d2-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="301d2-129">-NoWait</span></span>
<span data-ttu-id="301d2-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="301d2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="301d2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="301d2-131">-PassThru</span></span>
<span data-ttu-id="301d2-132">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="301d2-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="301d2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301d2-133">-ResourceGroupName</span></span>
<span data-ttu-id="301d2-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-134">Name of the resource group.</span></span>

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

### <span data-ttu-id="301d2-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="301d2-135">-ScaleUnit</span></span>
<span data-ttu-id="301d2-136">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-136">Name of the scale units.</span></span>

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

### <span data-ttu-id="301d2-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="301d2-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="301d2-138">A méretarány-csomópontok készletének hozzáadását lehetővé tevő bemeneti adatok listája.</span><span class="sxs-lookup"><span data-stu-id="301d2-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="301d2-139">A kivitelezéshez tekintse meg a SCALEUNITNODEPARAMETER tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="301d2-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="301d2-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="301d2-140">-SubscriptionId</span></span>
<span data-ttu-id="301d2-141">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="301d2-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="301d2-142">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="301d2-142">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="301d2-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="301d2-143">-Confirm</span></span>
<span data-ttu-id="301d2-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="301d2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301d2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301d2-145">-WhatIf</span></span>
<span data-ttu-id="301d2-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="301d2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301d2-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="301d2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301d2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301d2-148">CommonParameters</span></span>
<span data-ttu-id="301d2-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="301d2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301d2-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="301d2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301d2-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="301d2-151">INPUTS</span></span>

### <span data-ttu-id="301d2-152">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="301d2-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="301d2-153">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="301d2-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="301d2-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="301d2-154">OUTPUTS</span></span>

### <span data-ttu-id="301d2-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="301d2-155">System.Boolean</span></span>

## <span data-ttu-id="301d2-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="301d2-156">NOTES</span></span>

<span data-ttu-id="301d2-157">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="301d2-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="301d2-158">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="301d2-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="301d2-159">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="301d2-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="301d2-160">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="301d2-161">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="301d2-162">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="301d2-163">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="301d2-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="301d2-164">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="301d2-165">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="301d2-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="301d2-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="301d2-167">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="301d2-168">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="301d2-169">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="301d2-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="301d2-170">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="301d2-171">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="301d2-172">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="301d2-173">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="301d2-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="301d2-174">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="301d2-175">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="301d2-176">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="301d2-177">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="301d2-178">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="301d2-179">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="301d2-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="301d2-180">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="301d2-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="301d2-181">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="301d2-182">NODELIST <IScaleOutScaleUnitParameters [] >: csomópontok listája a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="301d2-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="301d2-183">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="301d2-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="301d2-184">`[ComputerName <String>]`: A fizikai gép számítógépének neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="301d2-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : a méretarányos csomópontok halmazának hozzáadását lehetővé tevő bemeneti adatok listája.</span><span class="sxs-lookup"><span data-stu-id="301d2-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="301d2-186">`[AwaitStorageConvergence <Boolean?>]`: A megjelölés azt jelzi, hogy a művelet csak a tárolás előtt közelíti meg a tárterületet.</span><span class="sxs-lookup"><span data-stu-id="301d2-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="301d2-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: A méretarányban lévő csomópontok listája.</span><span class="sxs-lookup"><span data-stu-id="301d2-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="301d2-188">`[BmciPv4Address <String>]`: A fizikai gép BMC-címe.</span><span class="sxs-lookup"><span data-stu-id="301d2-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="301d2-189">`[ComputerName <String>]`: A fizikai gép számítógépének neve.</span><span class="sxs-lookup"><span data-stu-id="301d2-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="301d2-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="301d2-190">RELATED LINKS</span></span>
