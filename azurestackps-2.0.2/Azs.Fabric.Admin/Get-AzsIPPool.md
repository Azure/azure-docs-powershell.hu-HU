---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016969"
---
# <span data-ttu-id="a08d0-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="a08d0-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="a08d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a08d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a08d0-103">Adja vissza a kért IP-készletet.</span><span class="sxs-lookup"><span data-stu-id="a08d0-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="a08d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a08d0-104">SYNTAX</span></span>

### <span data-ttu-id="a08d0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a08d0-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a08d0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a08d0-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a08d0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a08d0-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a08d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a08d0-108">DESCRIPTION</span></span>
<span data-ttu-id="a08d0-109">Adja vissza a kért IP-készletet.</span><span class="sxs-lookup"><span data-stu-id="a08d0-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="a08d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a08d0-110">EXAMPLES</span></span>

### <span data-ttu-id="a08d0-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="a08d0-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="a08d0-112">Az összes infrastruktúra IP-készletének beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a08d0-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="a08d0-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="a08d0-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="a08d0-114">Infrastruktúra IP-készletének beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="a08d0-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="a08d0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a08d0-115">PARAMETERS</span></span>

### <span data-ttu-id="a08d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08d0-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="a08d0-117">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a08d0-117">-Filter</span></span>
<span data-ttu-id="a08d0-118">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="a08d0-118">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a08d0-119">-InputObject</span></span>
<span data-ttu-id="a08d0-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a08d0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="a08d0-121">-Location</span></span>
<span data-ttu-id="a08d0-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a08d0-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a08d0-123">-Name</span></span>
<span data-ttu-id="a08d0-124">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="a08d0-124">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a08d0-125">-PassThru</span></span>
<span data-ttu-id="a08d0-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a08d0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a08d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a08d0-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a08d0-129">-SubscriptionId</span></span>
<span data-ttu-id="a08d0-130">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="a08d0-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a08d0-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a08d0-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a08d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08d0-132">CommonParameters</span></span>
<span data-ttu-id="a08d0-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a08d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08d0-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a08d0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08d0-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a08d0-135">INPUTS</span></span>

### <span data-ttu-id="a08d0-136">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a08d0-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a08d0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a08d0-137">OUTPUTS</span></span>

### <span data-ttu-id="a08d0-138">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="a08d0-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="a08d0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a08d0-139">NOTES</span></span>

<span data-ttu-id="a08d0-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a08d0-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a08d0-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a08d0-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a08d0-142">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a08d0-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a08d0-143">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a08d0-144">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a08d0-145">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a08d0-146">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="a08d0-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a08d0-147">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a08d0-148">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a08d0-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a08d0-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a08d0-150">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a08d0-151">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a08d0-152">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a08d0-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a08d0-153">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a08d0-154">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a08d0-155">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a08d0-156">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="a08d0-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a08d0-157">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a08d0-158">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a08d0-159">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a08d0-160">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a08d0-161">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a08d0-162">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a08d0-163">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="a08d0-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a08d0-164">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a08d0-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a08d0-165">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="a08d0-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a08d0-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a08d0-166">RELATED LINKS</span></span>

