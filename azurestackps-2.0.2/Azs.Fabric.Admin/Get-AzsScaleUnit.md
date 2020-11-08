---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunit
schema: 2.0.0
ms.openlocfilehash: cef23066fe1bfcd0b428302aab6c8077a8f676b6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016658"
---
# <span data-ttu-id="1fe5c-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1fe5c-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="1fe5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fe5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe5c-103">A kért méretarányt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-103">Returns the requested scale unit.</span></span>

## <span data-ttu-id="1fe5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fe5c-104">SYNTAX</span></span>

### <span data-ttu-id="1fe5c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fe5c-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1fe5c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1fe5c-106">Get</span></span>
```
Get-AzsScaleUnit -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1fe5c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fe5c-107">GetViaIdentity</span></span>
```
Get-AzsScaleUnit -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fe5c-108">DESCRIPTION</span></span>
<span data-ttu-id="1fe5c-109">A kért méretarányt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-109">Returns the requested scale unit.</span></span>

## <span data-ttu-id="1fe5c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1fe5c-110">EXAMPLES</span></span>

### <span data-ttu-id="1fe5c-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="1fe5c-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit

A list of information about scale units.
```

<span data-ttu-id="1fe5c-112">A méretarányokat tartalmazó adatok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="1fe5c-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="1fe5c-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit -Name "S-Cluster"

The information about a specific scale unit.
```

<span data-ttu-id="1fe5c-114">Adott méretarányú egység adatainak visszaadása.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="1fe5c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fe5c-115">PARAMETERS</span></span>

### <span data-ttu-id="1fe5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe5c-116">-DefaultProfile</span></span>
<span data-ttu-id="1fe5c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe5c-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="1fe5c-118">-Filter</span></span>
<span data-ttu-id="1fe5c-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="1fe5c-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="1fe5c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe5c-120">-InputObject</span></span>
<span data-ttu-id="1fe5c-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fe5c-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="1fe5c-122">-Location</span></span>
<span data-ttu-id="1fe5c-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-123">Location of the resource.</span></span>

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

### <span data-ttu-id="1fe5c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1fe5c-124">-Name</span></span>
<span data-ttu-id="1fe5c-125">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-125">Name of the scale units.</span></span>

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

### <span data-ttu-id="1fe5c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe5c-126">-PassThru</span></span>
<span data-ttu-id="1fe5c-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="1fe5c-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1fe5c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe5c-128">-ResourceGroupName</span></span>
<span data-ttu-id="1fe5c-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="1fe5c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fe5c-130">-SubscriptionId</span></span>
<span data-ttu-id="1fe5c-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fe5c-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-132">The subscription ID forms part of the URI for every service call.</span></span>


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

### <span data-ttu-id="1fe5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe5c-133">CommonParameters</span></span>
<span data-ttu-id="1fe5c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fe5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe5c-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe5c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe5c-136">INPUTS</span></span>

### <span data-ttu-id="1fe5c-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1fe5c-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="1fe5c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe5c-138">OUTPUTS</span></span>

### <span data-ttu-id="1fe5c-139">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1fe5c-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnit</span></span>



## <span data-ttu-id="1fe5c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fe5c-140">NOTES</span></span>

<span data-ttu-id="1fe5c-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fe5c-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1fe5c-143">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1fe5c-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fe5c-144">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="1fe5c-145">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="1fe5c-146">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="1fe5c-147">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="1fe5c-148">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="1fe5c-149">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="1fe5c-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1fe5c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fe5c-151">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="1fe5c-152">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="1fe5c-153">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1fe5c-154">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="1fe5c-155">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="1fe5c-156">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="1fe5c-157">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="1fe5c-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1fe5c-159">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="1fe5c-160">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="1fe5c-161">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="1fe5c-162">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="1fe5c-163">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="1fe5c-164">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fe5c-165">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1fe5c-166">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="1fe5c-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="1fe5c-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fe5c-167">RELATED LINKS</span></span>

