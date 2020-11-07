---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842601"
---
# <span data-ttu-id="034cd-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="034cd-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="034cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="034cd-102">SYNOPSIS</span></span>


## <span data-ttu-id="034cd-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="034cd-103">SYNTAX</span></span>

### <span data-ttu-id="034cd-104">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="034cd-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="034cd-105">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="034cd-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="034cd-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="034cd-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="034cd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="034cd-107">DESCRIPTION</span></span>


## <span data-ttu-id="034cd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="034cd-108">EXAMPLES</span></span>

### <span data-ttu-id="034cd-109">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="034cd-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="034cd-110">Az összes méretarányos csomópont lekérése egy helyen.</span><span class="sxs-lookup"><span data-stu-id="034cd-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="034cd-111">2. példa:</span><span class="sxs-lookup"><span data-stu-id="034cd-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="034cd-112">Egy adott méretarányú csomópontot kap egy olyan helyen, ahol nevet kapott.</span><span class="sxs-lookup"><span data-stu-id="034cd-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="034cd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="034cd-113">PARAMETERS</span></span>

### <span data-ttu-id="034cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034cd-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="034cd-115">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="034cd-115">-Filter</span></span>


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

### <span data-ttu-id="034cd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="034cd-116">-InputObject</span></span>
<span data-ttu-id="034cd-117">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="034cd-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="034cd-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="034cd-118">-Location</span></span>


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

### <span data-ttu-id="034cd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="034cd-119">-Name</span></span>


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

### <span data-ttu-id="034cd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="034cd-120">-PassThru</span></span>


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

### <span data-ttu-id="034cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034cd-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="034cd-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="034cd-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="034cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034cd-123">CommonParameters</span></span>
<span data-ttu-id="034cd-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="034cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034cd-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="034cd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034cd-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="034cd-126">INPUTS</span></span>

### <span data-ttu-id="034cd-127">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="034cd-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="034cd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="034cd-128">OUTPUTS</span></span>

### <span data-ttu-id="034cd-129">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="034cd-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="034cd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="034cd-130">NOTES</span></span>

<span data-ttu-id="034cd-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="034cd-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="034cd-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="034cd-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="034cd-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="034cd-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="034cd-134">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="034cd-135">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="034cd-136">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="034cd-137">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="034cd-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="034cd-138">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="034cd-139">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="034cd-140">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="034cd-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="034cd-141">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="034cd-142">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="034cd-143">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="034cd-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="034cd-144">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="034cd-145">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="034cd-146">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="034cd-147">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="034cd-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="034cd-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="034cd-149">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="034cd-150">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="034cd-151">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="034cd-152">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="034cd-153">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="034cd-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="034cd-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="034cd-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="034cd-155">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="034cd-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="034cd-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="034cd-156">RELATED LINKS</span></span>

