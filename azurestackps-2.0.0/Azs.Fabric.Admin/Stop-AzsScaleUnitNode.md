---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844781"
---
# <span data-ttu-id="5e7a1-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5e7a1-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="5e7a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7a1-103">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="5e7a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e7a1-104">SYNTAX</span></span>

### <span data-ttu-id="5e7a1-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e7a1-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e7a1-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e7a1-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e7a1-107">Leáll</span><span class="sxs-lookup"><span data-stu-id="5e7a1-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e7a1-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e7a1-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e7a1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e7a1-109">DESCRIPTION</span></span>
<span data-ttu-id="5e7a1-110">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="5e7a1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5e7a1-111">EXAMPLES</span></span>

### <span data-ttu-id="5e7a1-112">Példa 1: {{cím felvétele ide}}</span><span class="sxs-lookup"><span data-stu-id="5e7a1-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="5e7a1-113">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="5e7a1-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="5e7a1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e7a1-114">PARAMETERS</span></span>

### <span data-ttu-id="5e7a1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e7a1-115">-AsJob</span></span>
<span data-ttu-id="5e7a1-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5e7a1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5e7a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7a1-117">-DefaultProfile</span></span>
<span data-ttu-id="5e7a1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e7a1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5e7a1-119">-Force</span></span>
<span data-ttu-id="5e7a1-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5e7a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e7a1-121">-InputObject</span></span>
<span data-ttu-id="5e7a1-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5e7a1-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="5e7a1-123">-Location</span></span>
<span data-ttu-id="5e7a1-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7a1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e7a1-125">-Name</span></span>
<span data-ttu-id="5e7a1-126">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7a1-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="5e7a1-127">-NoWait</span></span>
<span data-ttu-id="5e7a1-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5e7a1-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e7a1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e7a1-129">-PassThru</span></span>
<span data-ttu-id="5e7a1-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="5e7a1-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e7a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e7a1-132">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="5e7a1-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7a1-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e7a1-133">-SubscriptionId</span></span>
<span data-ttu-id="5e7a1-134">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e7a1-135">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7a1-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e7a1-136">-Confirm</span></span>
<span data-ttu-id="5e7a1-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7a1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7a1-138">-WhatIf</span></span>
<span data-ttu-id="5e7a1-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e7a1-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e7a1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7a1-141">CommonParameters</span></span>
<span data-ttu-id="5e7a1-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e7a1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7a1-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7a1-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e7a1-144">INPUTS</span></span>

### <span data-ttu-id="5e7a1-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5e7a1-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5e7a1-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e7a1-146">OUTPUTS</span></span>

### <span data-ttu-id="5e7a1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e7a1-147">System.Boolean</span></span>



## <span data-ttu-id="5e7a1-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e7a1-148">NOTES</span></span>

<span data-ttu-id="5e7a1-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e7a1-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5e7a1-151">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5e7a1-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e7a1-152">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5e7a1-153">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5e7a1-154">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5e7a1-155">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5e7a1-156">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5e7a1-157">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5e7a1-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5e7a1-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e7a1-159">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5e7a1-160">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5e7a1-161">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5e7a1-162">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5e7a1-163">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5e7a1-164">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5e7a1-165">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5e7a1-166">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5e7a1-167">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5e7a1-168">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5e7a1-169">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5e7a1-170">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="5e7a1-171">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5e7a1-172">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5e7a1-173">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5e7a1-174">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="5e7a1-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5e7a1-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e7a1-175">RELATED LINKS</span></span>

