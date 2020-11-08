---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016698"
---
# <span data-ttu-id="bc679-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bc679-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="bc679-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc679-102">SYNOPSIS</span></span>
<span data-ttu-id="bc679-103">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="bc679-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="bc679-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc679-104">SYNTAX</span></span>

### <span data-ttu-id="bc679-105">PowerOn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc679-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc679-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc679-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc679-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc679-107">DESCRIPTION</span></span>
<span data-ttu-id="bc679-108">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="bc679-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="bc679-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bc679-109">EXAMPLES</span></span>

### <span data-ttu-id="bc679-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="bc679-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="bc679-111">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="bc679-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="bc679-112">2. példa:</span><span class="sxs-lookup"><span data-stu-id="bc679-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="bc679-113">Power egy méretarányos csomóponton</span><span class="sxs-lookup"><span data-stu-id="bc679-113">Power on a scale unit node.</span></span> <span data-ttu-id="bc679-114">Munkahelyként.</span><span class="sxs-lookup"><span data-stu-id="bc679-114">As a job.</span></span>

## <span data-ttu-id="bc679-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc679-115">PARAMETERS</span></span>

### <span data-ttu-id="bc679-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc679-116">-AsJob</span></span>
<span data-ttu-id="bc679-117">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="bc679-117">Run the command as a job</span></span>

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

### <span data-ttu-id="bc679-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc679-118">-DefaultProfile</span></span>
<span data-ttu-id="bc679-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc679-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc679-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bc679-120">-Force</span></span>
<span data-ttu-id="bc679-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc679-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bc679-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc679-122">-InputObject</span></span>
<span data-ttu-id="bc679-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc679-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc679-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="bc679-124">-Location</span></span>
<span data-ttu-id="bc679-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bc679-125">Location of the resource.</span></span>

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

### <span data-ttu-id="bc679-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc679-126">-Name</span></span>
<span data-ttu-id="bc679-127">A Scale Unit csomópont neve</span><span class="sxs-lookup"><span data-stu-id="bc679-127">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="bc679-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="bc679-128">-NoWait</span></span>
<span data-ttu-id="bc679-129">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="bc679-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc679-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc679-130">-PassThru</span></span>
<span data-ttu-id="bc679-131">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="bc679-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bc679-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc679-132">-ResourceGroupName</span></span>
<span data-ttu-id="bc679-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="bc679-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc679-134">-SubscriptionId</span></span>
<span data-ttu-id="bc679-135">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="bc679-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc679-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bc679-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bc679-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc679-137">-Confirm</span></span>
<span data-ttu-id="bc679-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc679-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc679-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc679-139">-WhatIf</span></span>
<span data-ttu-id="bc679-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc679-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc679-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc679-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc679-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc679-142">CommonParameters</span></span>
<span data-ttu-id="bc679-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc679-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc679-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc679-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc679-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc679-145">INPUTS</span></span>

### <span data-ttu-id="bc679-146">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="bc679-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="bc679-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc679-147">OUTPUTS</span></span>

### <span data-ttu-id="bc679-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc679-148">System.Boolean</span></span>

## <span data-ttu-id="bc679-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc679-149">NOTES</span></span>

<span data-ttu-id="bc679-150">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bc679-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc679-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="bc679-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bc679-152">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="bc679-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc679-153">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="bc679-154">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="bc679-155">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="bc679-156">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="bc679-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="bc679-157">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="bc679-158">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="bc679-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bc679-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc679-160">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="bc679-161">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="bc679-162">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bc679-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="bc679-163">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="bc679-164">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="bc679-165">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="bc679-166">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="bc679-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="bc679-167">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="bc679-168">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="bc679-169">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="bc679-170">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="bc679-171">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="bc679-172">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="bc679-173">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="bc679-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bc679-174">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bc679-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bc679-175">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="bc679-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="bc679-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc679-176">RELATED LINKS</span></span>
