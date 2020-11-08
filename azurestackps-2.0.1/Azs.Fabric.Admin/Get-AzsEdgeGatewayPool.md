---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015321"
---
# <span data-ttu-id="4e3bd-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="4e3bd-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="4e3bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e3bd-102">SYNOPSIS</span></span>


## <span data-ttu-id="4e3bd-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e3bd-103">SYNTAX</span></span>

### <span data-ttu-id="4e3bd-104">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e3bd-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4e3bd-105">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4e3bd-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4e3bd-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e3bd-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4e3bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e3bd-107">DESCRIPTION</span></span>


## <span data-ttu-id="4e3bd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4e3bd-108">EXAMPLES</span></span>

### <span data-ttu-id="4e3bd-109">Példa 1: az összes Edge átjáró-készlet listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="4e3bd-110">A teljes peremhálózat-átjárók listájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4e3bd-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="4e3bd-111">2. példa: speciális szegélyű átjárót tartalmazó alkalmazáskészlet beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="4e3bd-112">Egy adott Edge-átjárót tartalmazó alkalmazáskészlet beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="4e3bd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e3bd-113">PARAMETERS</span></span>

### <span data-ttu-id="4e3bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3bd-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="4e3bd-115">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="4e3bd-115">-Filter</span></span>


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

### <span data-ttu-id="4e3bd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e3bd-116">-InputObject</span></span>
<span data-ttu-id="4e3bd-117">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e3bd-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="4e3bd-118">-Location</span></span>


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

### <span data-ttu-id="4e3bd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e3bd-119">-Name</span></span>


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

### <span data-ttu-id="4e3bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e3bd-120">-PassThru</span></span>


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

### <span data-ttu-id="4e3bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3bd-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="4e3bd-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e3bd-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="4e3bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3bd-123">CommonParameters</span></span>
<span data-ttu-id="4e3bd-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e3bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3bd-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3bd-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3bd-126">INPUTS</span></span>

### <span data-ttu-id="4e3bd-127">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4e3bd-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4e3bd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3bd-128">OUTPUTS</span></span>

### <span data-ttu-id="4e3bd-129">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="4e3bd-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="4e3bd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e3bd-130">NOTES</span></span>

<span data-ttu-id="4e3bd-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e3bd-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4e3bd-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="4e3bd-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="4e3bd-134">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4e3bd-135">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4e3bd-136">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4e3bd-137">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4e3bd-138">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4e3bd-139">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4e3bd-140">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4e3bd-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e3bd-141">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4e3bd-142">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4e3bd-143">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4e3bd-144">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4e3bd-145">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4e3bd-146">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4e3bd-147">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4e3bd-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4e3bd-149">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4e3bd-150">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4e3bd-151">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4e3bd-152">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4e3bd-153">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e3bd-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4e3bd-155">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="4e3bd-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4e3bd-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e3bd-156">RELATED LINKS</span></span>

