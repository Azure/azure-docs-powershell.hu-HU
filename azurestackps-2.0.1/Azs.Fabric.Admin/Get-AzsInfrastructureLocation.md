---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015285"
---
# <span data-ttu-id="67603-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="67603-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="67603-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67603-102">SYNOPSIS</span></span>
<span data-ttu-id="67603-103">A kért szövet helyének értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="67603-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="67603-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67603-104">SYNTAX</span></span>

### <span data-ttu-id="67603-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67603-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67603-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="67603-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="67603-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67603-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="67603-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="67603-108">DESCRIPTION</span></span>
<span data-ttu-id="67603-109">A kért szövet helyének értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="67603-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="67603-110">Példák</span><span class="sxs-lookup"><span data-stu-id="67603-110">EXAMPLES</span></span>

### <span data-ttu-id="67603-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="67603-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="67603-112">A teljes anyagból álló helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="67603-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="67603-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="67603-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="67603-114">A név alapján megtudhatja, hogy hol található.</span><span class="sxs-lookup"><span data-stu-id="67603-114">Get a location based on the name.</span></span>

## <span data-ttu-id="67603-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67603-115">PARAMETERS</span></span>

### <span data-ttu-id="67603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67603-116">-DefaultProfile</span></span>
<span data-ttu-id="67603-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67603-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67603-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="67603-118">-FabricLocation</span></span>
<span data-ttu-id="67603-119">A szövet helye.</span><span class="sxs-lookup"><span data-stu-id="67603-119">Fabric location.</span></span>

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

### <span data-ttu-id="67603-120">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="67603-120">-Filter</span></span>
<span data-ttu-id="67603-121">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="67603-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="67603-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67603-122">-InputObject</span></span>
<span data-ttu-id="67603-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67603-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67603-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67603-124">-PassThru</span></span>
<span data-ttu-id="67603-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="67603-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="67603-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67603-126">-ResourceGroupName</span></span>
<span data-ttu-id="67603-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67603-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="67603-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67603-128">-SubscriptionId</span></span>
<span data-ttu-id="67603-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="67603-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67603-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="67603-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67603-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67603-131">CommonParameters</span></span>
<span data-ttu-id="67603-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67603-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67603-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="67603-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67603-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67603-134">INPUTS</span></span>

### <span data-ttu-id="67603-135">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="67603-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="67603-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67603-136">OUTPUTS</span></span>

### <span data-ttu-id="67603-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="67603-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="67603-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67603-138">NOTES</span></span>

<span data-ttu-id="67603-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="67603-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67603-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="67603-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="67603-141">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="67603-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67603-142">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="67603-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="67603-143">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="67603-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="67603-144">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="67603-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="67603-145">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="67603-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="67603-146">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="67603-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="67603-147">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="67603-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="67603-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="67603-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67603-149">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="67603-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="67603-150">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="67603-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="67603-151">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="67603-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="67603-152">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="67603-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="67603-153">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="67603-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="67603-154">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="67603-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="67603-155">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="67603-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="67603-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67603-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="67603-157">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="67603-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="67603-158">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="67603-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="67603-159">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="67603-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="67603-160">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="67603-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="67603-161">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="67603-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="67603-162">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="67603-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="67603-163">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="67603-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="67603-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67603-164">RELATED LINKS</span></span>

