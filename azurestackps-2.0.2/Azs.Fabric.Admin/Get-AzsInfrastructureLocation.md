---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016771"
---
# <span data-ttu-id="1999a-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="1999a-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="1999a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1999a-102">SYNOPSIS</span></span>
<span data-ttu-id="1999a-103">A kért szövet helyének értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1999a-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="1999a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1999a-104">SYNTAX</span></span>

### <span data-ttu-id="1999a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1999a-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1999a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1999a-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1999a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1999a-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="1999a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1999a-108">DESCRIPTION</span></span>
<span data-ttu-id="1999a-109">A kért szövet helyének értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1999a-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="1999a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1999a-110">EXAMPLES</span></span>

### <span data-ttu-id="1999a-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="1999a-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="1999a-112">A teljes anyagból álló helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1999a-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="1999a-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="1999a-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="1999a-114">A név alapján megtudhatja, hogy hol található.</span><span class="sxs-lookup"><span data-stu-id="1999a-114">Get a location based on the name.</span></span>

## <span data-ttu-id="1999a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1999a-115">PARAMETERS</span></span>

### <span data-ttu-id="1999a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1999a-116">-DefaultProfile</span></span>
<span data-ttu-id="1999a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1999a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1999a-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="1999a-118">-FabricLocation</span></span>
<span data-ttu-id="1999a-119">A szövet helye.</span><span class="sxs-lookup"><span data-stu-id="1999a-119">Fabric location.</span></span>

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

### <span data-ttu-id="1999a-120">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="1999a-120">-Filter</span></span>
<span data-ttu-id="1999a-121">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="1999a-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="1999a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1999a-122">-InputObject</span></span>
<span data-ttu-id="1999a-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1999a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1999a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1999a-124">-PassThru</span></span>
<span data-ttu-id="1999a-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="1999a-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1999a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1999a-126">-ResourceGroupName</span></span>
<span data-ttu-id="1999a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="1999a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1999a-128">-SubscriptionId</span></span>
<span data-ttu-id="1999a-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1999a-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1999a-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1999a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1999a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1999a-131">CommonParameters</span></span>
<span data-ttu-id="1999a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1999a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1999a-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1999a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1999a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1999a-134">INPUTS</span></span>

### <span data-ttu-id="1999a-135">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1999a-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="1999a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1999a-136">OUTPUTS</span></span>

### <span data-ttu-id="1999a-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="1999a-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="1999a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1999a-138">NOTES</span></span>

<span data-ttu-id="1999a-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1999a-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1999a-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1999a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1999a-141">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1999a-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1999a-142">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="1999a-143">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="1999a-144">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="1999a-145">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="1999a-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="1999a-146">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="1999a-147">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="1999a-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1999a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1999a-149">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="1999a-150">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="1999a-151">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1999a-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1999a-152">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="1999a-153">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="1999a-154">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="1999a-155">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="1999a-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="1999a-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1999a-157">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="1999a-158">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="1999a-159">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="1999a-160">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="1999a-161">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1999a-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1999a-162">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1999a-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1999a-163">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="1999a-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="1999a-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1999a-164">RELATED LINKS</span></span>

