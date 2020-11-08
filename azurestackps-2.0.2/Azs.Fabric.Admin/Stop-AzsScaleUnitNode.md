---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016809"
---
# <span data-ttu-id="298ca-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="298ca-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="298ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="298ca-102">SYNOPSIS</span></span>
<span data-ttu-id="298ca-103">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="298ca-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="298ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="298ca-104">SYNTAX</span></span>

### <span data-ttu-id="298ca-105">Erő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="298ca-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="298ca-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="298ca-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="298ca-107">Leáll</span><span class="sxs-lookup"><span data-stu-id="298ca-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="298ca-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="298ca-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="298ca-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="298ca-109">DESCRIPTION</span></span>
<span data-ttu-id="298ca-110">A Scale-Unit csomópont kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="298ca-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="298ca-111">Példák</span><span class="sxs-lookup"><span data-stu-id="298ca-111">EXAMPLES</span></span>

### <span data-ttu-id="298ca-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="298ca-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="298ca-113">A Scale-egység csomópontjának kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="298ca-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="298ca-114">2. példa:</span><span class="sxs-lookup"><span data-stu-id="298ca-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="298ca-115">A Scale-egység csomópontjának kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="298ca-115">Power down a scale unit node.</span></span> <span data-ttu-id="298ca-116">Munkahelyként.</span><span class="sxs-lookup"><span data-stu-id="298ca-116">As a job.</span></span>

## <span data-ttu-id="298ca-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="298ca-117">PARAMETERS</span></span>

### <span data-ttu-id="298ca-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="298ca-118">-AsJob</span></span>
<span data-ttu-id="298ca-119">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="298ca-119">Run the command as a job</span></span>

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

### <span data-ttu-id="298ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298ca-120">-DefaultProfile</span></span>
<span data-ttu-id="298ca-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="298ca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="298ca-122">-Force</span><span class="sxs-lookup"><span data-stu-id="298ca-122">-Force</span></span>
<span data-ttu-id="298ca-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="298ca-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="298ca-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="298ca-124">-InputObject</span></span>
<span data-ttu-id="298ca-125">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="298ca-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="298ca-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="298ca-126">-Location</span></span>
<span data-ttu-id="298ca-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="298ca-127">Location of the resource.</span></span>

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

### <span data-ttu-id="298ca-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="298ca-128">-Name</span></span>
<span data-ttu-id="298ca-129">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="298ca-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="298ca-130">-NoWait</span></span>
<span data-ttu-id="298ca-131">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="298ca-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="298ca-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="298ca-132">-PassThru</span></span>
<span data-ttu-id="298ca-133">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="298ca-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="298ca-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298ca-134">-ResourceGroupName</span></span>
<span data-ttu-id="298ca-135">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="298ca-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="298ca-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="298ca-136">-SubscriptionId</span></span>
<span data-ttu-id="298ca-137">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="298ca-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="298ca-138">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="298ca-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="298ca-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="298ca-139">-Confirm</span></span>
<span data-ttu-id="298ca-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="298ca-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298ca-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298ca-141">-WhatIf</span></span>
<span data-ttu-id="298ca-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="298ca-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298ca-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="298ca-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298ca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298ca-144">CommonParameters</span></span>
<span data-ttu-id="298ca-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="298ca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298ca-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="298ca-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298ca-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="298ca-147">INPUTS</span></span>

### <span data-ttu-id="298ca-148">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="298ca-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="298ca-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="298ca-149">OUTPUTS</span></span>

### <span data-ttu-id="298ca-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="298ca-150">System.Boolean</span></span>

## <span data-ttu-id="298ca-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="298ca-151">NOTES</span></span>

<span data-ttu-id="298ca-152">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="298ca-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="298ca-153">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="298ca-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="298ca-154">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="298ca-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="298ca-155">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="298ca-156">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="298ca-157">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="298ca-158">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="298ca-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="298ca-159">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="298ca-160">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="298ca-161">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="298ca-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="298ca-162">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="298ca-163">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="298ca-164">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="298ca-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="298ca-165">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="298ca-166">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="298ca-167">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="298ca-168">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="298ca-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="298ca-169">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="298ca-170">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="298ca-171">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="298ca-172">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="298ca-173">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="298ca-174">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="298ca-175">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="298ca-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="298ca-176">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="298ca-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="298ca-177">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="298ca-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="298ca-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="298ca-178">RELATED LINKS</span></span>
