---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844793"
---
# <span data-ttu-id="0efb0-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="0efb0-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="0efb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0efb0-102">SYNOPSIS</span></span>
<span data-ttu-id="0efb0-103">A kért logikai alhálózat értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0efb0-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="0efb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0efb0-104">SYNTAX</span></span>

### <span data-ttu-id="0efb0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0efb0-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0efb0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0efb0-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="0efb0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0efb0-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0efb0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0efb0-108">DESCRIPTION</span></span>
<span data-ttu-id="0efb0-109">A kért logikai alhálózat értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0efb0-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="0efb0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0efb0-110">EXAMPLES</span></span>

### <span data-ttu-id="0efb0-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="0efb0-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="0efb0-112">Minden logikai hálózat beolvasása egy helyen.</span><span class="sxs-lookup"><span data-stu-id="0efb0-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="0efb0-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="0efb0-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="0efb0-114">Meghatározott logikai hálózatok beszerzése egy név alapján</span><span class="sxs-lookup"><span data-stu-id="0efb0-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="0efb0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0efb0-115">PARAMETERS</span></span>

### <span data-ttu-id="0efb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efb0-116">-DefaultProfile</span></span>
<span data-ttu-id="0efb0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0efb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efb0-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="0efb0-118">-Filter</span></span>
<span data-ttu-id="0efb0-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="0efb0-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="0efb0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efb0-120">-InputObject</span></span>
<span data-ttu-id="0efb0-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0efb0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0efb0-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="0efb0-122">-Location</span></span>
<span data-ttu-id="0efb0-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0efb0-123">Location of the resource.</span></span>

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

### <span data-ttu-id="0efb0-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="0efb0-124">-LogicalNetwork</span></span>
<span data-ttu-id="0efb0-125">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0efb0-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0efb0-126">-Name</span></span>
<span data-ttu-id="0efb0-127">A logikai alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="0efb0-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="0efb0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0efb0-128">-PassThru</span></span>
<span data-ttu-id="0efb0-129">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="0efb0-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0efb0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efb0-130">-ResourceGroupName</span></span>
<span data-ttu-id="0efb0-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="0efb0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0efb0-132">-SubscriptionId</span></span>
<span data-ttu-id="0efb0-133">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="0efb0-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0efb0-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0efb0-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0efb0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efb0-135">CommonParameters</span></span>
<span data-ttu-id="0efb0-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0efb0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efb0-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0efb0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efb0-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0efb0-138">INPUTS</span></span>

### <span data-ttu-id="0efb0-139">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0efb0-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="0efb0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0efb0-140">OUTPUTS</span></span>

### <span data-ttu-id="0efb0-141">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. ILogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="0efb0-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="0efb0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0efb0-142">NOTES</span></span>

<span data-ttu-id="0efb0-143">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0efb0-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0efb0-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0efb0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0efb0-145">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0efb0-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0efb0-146">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="0efb0-147">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="0efb0-148">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="0efb0-149">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="0efb0-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="0efb0-150">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="0efb0-151">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="0efb0-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0efb0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0efb0-153">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="0efb0-154">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="0efb0-155">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0efb0-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0efb0-156">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="0efb0-157">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="0efb0-158">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="0efb0-159">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="0efb0-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="0efb0-160">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0efb0-161">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="0efb0-162">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="0efb0-163">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="0efb0-164">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="0efb0-165">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="0efb0-166">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="0efb0-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0efb0-167">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0efb0-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0efb0-168">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="0efb0-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="0efb0-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0efb0-169">RELATED LINKS</span></span>

