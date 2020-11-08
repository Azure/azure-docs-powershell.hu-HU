---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017099"
---
# <span data-ttu-id="eec75-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="eec75-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="eec75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eec75-102">SYNOPSIS</span></span>
<span data-ttu-id="eec75-103">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="eec75-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="eec75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eec75-104">SYNTAX</span></span>

### <span data-ttu-id="eec75-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eec75-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eec75-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eec75-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eec75-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eec75-107">DESCRIPTION</span></span>
<span data-ttu-id="eec75-108">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="eec75-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="eec75-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eec75-109">EXAMPLES</span></span>

### <span data-ttu-id="eec75-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="eec75-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="eec75-111">Az infrastruktúra szerepkör-példányának a teljesítménye</span><span class="sxs-lookup"><span data-stu-id="eec75-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="eec75-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eec75-112">PARAMETERS</span></span>

### <span data-ttu-id="eec75-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec75-113">-AsJob</span></span>
<span data-ttu-id="eec75-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="eec75-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eec75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec75-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="eec75-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eec75-116">-Force</span></span>
<span data-ttu-id="eec75-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eec75-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eec75-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eec75-118">-InputObject</span></span>
<span data-ttu-id="eec75-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eec75-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eec75-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="eec75-120">-Location</span></span>
<span data-ttu-id="eec75-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eec75-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eec75-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eec75-122">-Name</span></span>
<span data-ttu-id="eec75-123">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eec75-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="eec75-124">-NoWait</span></span>
<span data-ttu-id="eec75-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="eec75-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eec75-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eec75-126">-PassThru</span></span>
<span data-ttu-id="eec75-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="eec75-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eec75-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec75-128">-ResourceGroupName</span></span>
<span data-ttu-id="eec75-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eec75-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eec75-130">-SubscriptionId</span></span>
<span data-ttu-id="eec75-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="eec75-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eec75-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eec75-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eec75-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eec75-133">-Confirm</span></span>
<span data-ttu-id="eec75-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eec75-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec75-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec75-135">-WhatIf</span></span>
<span data-ttu-id="eec75-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eec75-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec75-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eec75-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec75-138">CommonParameters</span></span>
<span data-ttu-id="eec75-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eec75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec75-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eec75-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec75-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eec75-141">INPUTS</span></span>

### <span data-ttu-id="eec75-142">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="eec75-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="eec75-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eec75-143">OUTPUTS</span></span>

### <span data-ttu-id="eec75-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eec75-144">System.Boolean</span></span>



## <span data-ttu-id="eec75-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eec75-145">NOTES</span></span>

<span data-ttu-id="eec75-146">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="eec75-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eec75-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="eec75-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eec75-148">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="eec75-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eec75-149">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="eec75-150">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="eec75-151">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="eec75-152">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="eec75-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="eec75-153">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="eec75-154">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="eec75-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eec75-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eec75-156">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="eec75-157">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="eec75-158">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eec75-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="eec75-159">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="eec75-160">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="eec75-161">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="eec75-162">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="eec75-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="eec75-163">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="eec75-164">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="eec75-165">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="eec75-166">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="eec75-167">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="eec75-168">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="eec75-169">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="eec75-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eec75-170">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eec75-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="eec75-171">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="eec75-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="eec75-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eec75-172">RELATED LINKS</span></span>

