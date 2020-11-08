---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 07751ba4228faa578e4181ec481eef6e5b033126
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015196"
---
# <span data-ttu-id="84b51-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="84b51-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="84b51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84b51-102">SYNOPSIS</span></span>
<span data-ttu-id="84b51-103">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="84b51-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="84b51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84b51-104">SYNTAX</span></span>

### <span data-ttu-id="84b51-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84b51-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="84b51-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84b51-106">PowerOffViaIdentity</span></span>
```
Stop-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84b51-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84b51-107">DESCRIPTION</span></span>
<span data-ttu-id="84b51-108">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="84b51-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="84b51-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84b51-109">EXAMPLES</span></span>

### <span data-ttu-id="84b51-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="84b51-110">Example 1:</span></span> 
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="84b51-111">Infrastrukturális szerepkör-példány kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="84b51-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="84b51-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84b51-112">PARAMETERS</span></span>

### <span data-ttu-id="84b51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84b51-113">-AsJob</span></span>
<span data-ttu-id="84b51-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="84b51-114">Run the command as a job</span></span>

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

### <span data-ttu-id="84b51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b51-115">-DefaultProfile</span></span>
<span data-ttu-id="84b51-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84b51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b51-117">-Force</span><span class="sxs-lookup"><span data-stu-id="84b51-117">-Force</span></span>
<span data-ttu-id="84b51-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84b51-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="84b51-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b51-119">-InputObject</span></span>
<span data-ttu-id="84b51-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84b51-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="84b51-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="84b51-121">-Location</span></span>
<span data-ttu-id="84b51-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="84b51-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="84b51-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84b51-123">-Name</span></span>
<span data-ttu-id="84b51-124">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="84b51-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="84b51-125">-NoWait</span></span>
<span data-ttu-id="84b51-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="84b51-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84b51-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b51-127">-PassThru</span></span>
<span data-ttu-id="84b51-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="84b51-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84b51-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b51-129">-ResourceGroupName</span></span>
<span data-ttu-id="84b51-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="84b51-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84b51-131">-SubscriptionId</span></span>
<span data-ttu-id="84b51-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="84b51-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84b51-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="84b51-133">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="84b51-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84b51-134">-Confirm</span></span>
<span data-ttu-id="84b51-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84b51-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b51-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b51-136">-WhatIf</span></span>
<span data-ttu-id="84b51-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84b51-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b51-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84b51-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b51-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b51-139">CommonParameters</span></span>
<span data-ttu-id="84b51-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84b51-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b51-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84b51-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b51-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84b51-142">INPUTS</span></span>

### <span data-ttu-id="84b51-143">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="84b51-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="84b51-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84b51-144">OUTPUTS</span></span>

### <span data-ttu-id="84b51-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84b51-145">System.Boolean</span></span>



## <span data-ttu-id="84b51-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84b51-146">NOTES</span></span>

<span data-ttu-id="84b51-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="84b51-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84b51-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="84b51-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="84b51-149">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="84b51-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84b51-150">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="84b51-151">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="84b51-152">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="84b51-153">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="84b51-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="84b51-154">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="84b51-155">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="84b51-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="84b51-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84b51-157">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="84b51-158">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="84b51-159">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="84b51-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="84b51-160">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="84b51-161">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="84b51-162">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="84b51-163">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="84b51-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="84b51-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="84b51-165">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="84b51-166">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="84b51-167">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="84b51-168">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="84b51-169">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="84b51-170">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="84b51-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="84b51-171">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="84b51-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="84b51-172">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="84b51-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="84b51-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84b51-173">RELATED LINKS</span></span>

