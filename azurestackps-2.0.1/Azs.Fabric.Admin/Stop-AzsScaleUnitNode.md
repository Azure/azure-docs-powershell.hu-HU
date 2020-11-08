---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015209"
---
# <span data-ttu-id="d97a9-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d97a9-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d97a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d97a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d97a9-103">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="d97a9-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="d97a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d97a9-104">SYNTAX</span></span>

### <span data-ttu-id="d97a9-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d97a9-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d97a9-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d97a9-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d97a9-107">Leáll</span><span class="sxs-lookup"><span data-stu-id="d97a9-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d97a9-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d97a9-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d97a9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d97a9-109">DESCRIPTION</span></span>
<span data-ttu-id="d97a9-110">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="d97a9-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="d97a9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d97a9-111">EXAMPLES</span></span>

### <span data-ttu-id="d97a9-112">Példa 1: {{cím felvétele ide}}</span><span class="sxs-lookup"><span data-stu-id="d97a9-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="d97a9-113">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="d97a9-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="d97a9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d97a9-114">PARAMETERS</span></span>

### <span data-ttu-id="d97a9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d97a9-115">-AsJob</span></span>
<span data-ttu-id="d97a9-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d97a9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d97a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97a9-117">-DefaultProfile</span></span>
<span data-ttu-id="d97a9-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d97a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97a9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d97a9-119">-Force</span></span>
<span data-ttu-id="d97a9-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d97a9-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d97a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d97a9-121">-InputObject</span></span>
<span data-ttu-id="d97a9-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d97a9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d97a9-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="d97a9-123">-Location</span></span>
<span data-ttu-id="d97a9-124">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d97a9-124">Location of the resource.</span></span>

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

### <span data-ttu-id="d97a9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d97a9-125">-Name</span></span>
<span data-ttu-id="d97a9-126">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-126">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="d97a9-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="d97a9-127">-NoWait</span></span>
<span data-ttu-id="d97a9-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d97a9-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d97a9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d97a9-129">-PassThru</span></span>
<span data-ttu-id="d97a9-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d97a9-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d97a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="d97a9-132">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="d97a9-132">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="d97a9-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d97a9-133">-SubscriptionId</span></span>
<span data-ttu-id="d97a9-134">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="d97a9-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d97a9-135">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d97a9-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d97a9-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d97a9-136">-Confirm</span></span>
<span data-ttu-id="d97a9-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d97a9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97a9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97a9-138">-WhatIf</span></span>
<span data-ttu-id="d97a9-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d97a9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d97a9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d97a9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97a9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97a9-141">CommonParameters</span></span>
<span data-ttu-id="d97a9-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d97a9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97a9-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d97a9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97a9-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d97a9-144">INPUTS</span></span>

### <span data-ttu-id="d97a9-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d97a9-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d97a9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d97a9-146">OUTPUTS</span></span>

### <span data-ttu-id="d97a9-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d97a9-147">System.Boolean</span></span>



## <span data-ttu-id="d97a9-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d97a9-148">NOTES</span></span>

<span data-ttu-id="d97a9-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d97a9-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d97a9-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d97a9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d97a9-151">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d97a9-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d97a9-152">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d97a9-153">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d97a9-154">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d97a9-155">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="d97a9-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d97a9-156">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d97a9-157">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d97a9-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d97a9-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d97a9-159">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d97a9-160">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d97a9-161">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d97a9-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d97a9-162">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d97a9-163">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d97a9-164">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d97a9-165">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="d97a9-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d97a9-166">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d97a9-167">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d97a9-168">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d97a9-169">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d97a9-170">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="d97a9-171">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d97a9-172">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="d97a9-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d97a9-173">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d97a9-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d97a9-174">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="d97a9-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d97a9-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d97a9-175">RELATED LINKS</span></span>

