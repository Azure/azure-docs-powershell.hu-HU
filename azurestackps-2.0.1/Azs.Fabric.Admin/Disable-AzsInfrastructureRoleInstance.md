---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015232"
---
# <span data-ttu-id="74004-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="74004-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="74004-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74004-102">SYNOPSIS</span></span>


## <span data-ttu-id="74004-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74004-103">SYNTAX</span></span>

### <span data-ttu-id="74004-104">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74004-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74004-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74004-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74004-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="74004-106">DESCRIPTION</span></span>
<span data-ttu-id="74004-107">Egy infrastrukturális szerepkör-példány leállítása a karbantartáshoz.</span><span class="sxs-lookup"><span data-stu-id="74004-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="74004-108">Példák</span><span class="sxs-lookup"><span data-stu-id="74004-108">EXAMPLES</span></span>

### <span data-ttu-id="74004-109">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="74004-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="74004-110">Egy infrastrukturális szerepkör-példány leállítása a karbantartáshoz.</span><span class="sxs-lookup"><span data-stu-id="74004-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="74004-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74004-111">PARAMETERS</span></span>

### <span data-ttu-id="74004-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74004-112">-AsJob</span></span>
<span data-ttu-id="74004-113">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="74004-113">Run the command as a job</span></span>

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

### <span data-ttu-id="74004-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74004-114">-DefaultProfile</span></span>
<span data-ttu-id="74004-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74004-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74004-116">-Force</span><span class="sxs-lookup"><span data-stu-id="74004-116">-Force</span></span>
<span data-ttu-id="74004-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74004-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="74004-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74004-118">-InputObject</span></span>
<span data-ttu-id="74004-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74004-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="74004-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="74004-120">-Location</span></span>
<span data-ttu-id="74004-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="74004-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74004-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74004-122">-Name</span></span>
<span data-ttu-id="74004-123">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="74004-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74004-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="74004-124">-NoWait</span></span>
<span data-ttu-id="74004-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="74004-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74004-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74004-126">-PassThru</span></span>
<span data-ttu-id="74004-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="74004-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74004-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74004-128">-ResourceGroupName</span></span>
<span data-ttu-id="74004-129">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="74004-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74004-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74004-130">-SubscriptionId</span></span>
<span data-ttu-id="74004-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="74004-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="74004-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="74004-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="74004-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74004-133">-Confirm</span></span>
<span data-ttu-id="74004-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74004-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74004-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74004-135">-WhatIf</span></span>
<span data-ttu-id="74004-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74004-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74004-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74004-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74004-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74004-138">CommonParameters</span></span>
<span data-ttu-id="74004-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74004-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74004-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74004-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74004-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74004-141">INPUTS</span></span>

### <span data-ttu-id="74004-142">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="74004-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="74004-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74004-143">OUTPUTS</span></span>

### <span data-ttu-id="74004-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74004-144">System.Boolean</span></span>



## <span data-ttu-id="74004-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74004-145">NOTES</span></span>

<span data-ttu-id="74004-146">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="74004-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74004-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="74004-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="74004-148">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="74004-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74004-149">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="74004-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="74004-150">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="74004-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="74004-151">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="74004-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="74004-152">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="74004-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="74004-153">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="74004-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="74004-154">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="74004-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="74004-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="74004-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74004-156">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="74004-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="74004-157">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="74004-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="74004-158">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="74004-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="74004-159">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="74004-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="74004-160">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="74004-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="74004-161">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="74004-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="74004-162">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="74004-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="74004-163">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74004-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="74004-164">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="74004-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="74004-165">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="74004-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="74004-166">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="74004-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="74004-167">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="74004-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="74004-168">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="74004-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="74004-169">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="74004-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="74004-170">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="74004-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="74004-171">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="74004-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="74004-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74004-172">RELATED LINKS</span></span>

