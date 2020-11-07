---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: 6e8b5f2dbfde62613a521fd7a49fba27c54ab498
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842586"
---
# <span data-ttu-id="94640-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="94640-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="94640-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94640-102">SYNOPSIS</span></span>
<span data-ttu-id="94640-103">A kért infrastrukturális szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="94640-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="94640-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94640-104">SYNTAX</span></span>

### <span data-ttu-id="94640-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94640-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94640-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94640-106">RestartViaIdentity</span></span>
```
Restart-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94640-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94640-107">DESCRIPTION</span></span>
<span data-ttu-id="94640-108">A kért infrastrukturális szerepkör újraindítása.</span><span class="sxs-lookup"><span data-stu-id="94640-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="94640-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94640-109">EXAMPLES</span></span>

### <span data-ttu-id="94640-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="94640-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRole -Name "Compute Controller"

```

<span data-ttu-id="94640-111">Indítsa újra az infrastrukturális szerepkört, amely összeomlott.</span><span class="sxs-lookup"><span data-stu-id="94640-111">Restart an infrastructure role which has crashed.</span></span>



## <span data-ttu-id="94640-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94640-112">PARAMETERS</span></span>

### <span data-ttu-id="94640-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94640-113">-AsJob</span></span>
<span data-ttu-id="94640-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="94640-114">Run the command as a job</span></span>

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

### <span data-ttu-id="94640-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94640-115">-DefaultProfile</span></span>
<span data-ttu-id="94640-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94640-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94640-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94640-117">-Force</span></span>
<span data-ttu-id="94640-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94640-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="94640-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94640-119">-InputObject</span></span>
<span data-ttu-id="94640-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94640-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="94640-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="94640-121">-Location</span></span>
<span data-ttu-id="94640-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="94640-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94640-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94640-123">-Name</span></span>
<span data-ttu-id="94640-124">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="94640-124">Infrastructure role name.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94640-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="94640-125">-NoWait</span></span>
<span data-ttu-id="94640-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="94640-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94640-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94640-127">-PassThru</span></span>
<span data-ttu-id="94640-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="94640-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94640-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94640-129">-ResourceGroupName</span></span>
<span data-ttu-id="94640-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94640-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94640-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94640-131">-SubscriptionId</span></span>
<span data-ttu-id="94640-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="94640-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94640-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94640-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94640-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94640-134">-Confirm</span></span>
<span data-ttu-id="94640-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94640-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94640-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94640-136">-WhatIf</span></span>
<span data-ttu-id="94640-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94640-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94640-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94640-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94640-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94640-139">CommonParameters</span></span>
<span data-ttu-id="94640-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94640-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94640-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94640-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94640-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94640-142">INPUTS</span></span>

### <span data-ttu-id="94640-143">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="94640-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="94640-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94640-144">OUTPUTS</span></span>

### <span data-ttu-id="94640-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94640-145">System.Boolean</span></span>



## <span data-ttu-id="94640-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94640-146">NOTES</span></span>

<span data-ttu-id="94640-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="94640-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94640-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="94640-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="94640-149">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="94640-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94640-150">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="94640-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="94640-151">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="94640-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="94640-152">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="94640-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="94640-153">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="94640-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="94640-154">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="94640-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="94640-155">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="94640-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="94640-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="94640-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94640-157">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="94640-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="94640-158">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="94640-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="94640-159">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="94640-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="94640-160">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="94640-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="94640-161">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="94640-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="94640-162">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="94640-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="94640-163">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="94640-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="94640-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94640-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="94640-165">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="94640-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="94640-166">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="94640-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="94640-167">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="94640-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="94640-168">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="94640-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="94640-169">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="94640-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="94640-170">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="94640-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94640-171">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94640-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="94640-172">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="94640-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="94640-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94640-173">RELATED LINKS</span></span>

