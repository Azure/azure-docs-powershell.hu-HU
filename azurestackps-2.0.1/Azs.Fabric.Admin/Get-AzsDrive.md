---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015228"
---
# <span data-ttu-id="c4fe5-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="c4fe5-101">Get-AzsDrive</span></span>

## <span data-ttu-id="c4fe5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fe5-103">Adja vissza a kért tárterület-meghajtót.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="c4fe5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4fe5-104">SYNTAX</span></span>

### <span data-ttu-id="c4fe5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4fe5-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c4fe5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4fe5-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="c4fe5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4fe5-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="c4fe5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4fe5-108">DESCRIPTION</span></span>
<span data-ttu-id="c4fe5-109">Adja vissza a kért tárterület-meghajtót.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="c4fe5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="c4fe5-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="c4fe5-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="c4fe5-112">Megtudhatja, hogy az adott fürtökhöz milyen tárterület-meghajtók használhatók.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="c4fe5-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="c4fe5-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="c4fe5-114">Tárterület-meghajtó beszerzése egy adott fürt nevében</span><span class="sxs-lookup"><span data-stu-id="c4fe5-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="c4fe5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4fe5-115">PARAMETERS</span></span>

### <span data-ttu-id="c4fe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fe5-116">-DefaultProfile</span></span>
<span data-ttu-id="c4fe5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fe5-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c4fe5-118">-Filter</span></span>
<span data-ttu-id="c4fe5-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="c4fe5-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="c4fe5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4fe5-120">-InputObject</span></span>
<span data-ttu-id="c4fe5-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4fe5-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="c4fe5-122">-Location</span></span>
<span data-ttu-id="c4fe5-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-123">Location of the resource.</span></span>

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

### <span data-ttu-id="c4fe5-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4fe5-124">-Name</span></span>
<span data-ttu-id="c4fe5-125">A tárterület-meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="c4fe5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4fe5-126">-PassThru</span></span>
<span data-ttu-id="c4fe5-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="c4fe5-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4fe5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fe5-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4fe5-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="c4fe5-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c4fe5-130">-ScaleUnit</span></span>
<span data-ttu-id="c4fe5-131">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="c4fe5-132">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="c4fe5-132">-Skip</span></span>
<span data-ttu-id="c4fe5-133">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="c4fe5-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="c4fe5-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c4fe5-134">-StorageSubSystem</span></span>
<span data-ttu-id="c4fe5-135">A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="c4fe5-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4fe5-136">-SubscriptionId</span></span>
<span data-ttu-id="c4fe5-137">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4fe5-138">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4fe5-139">-Top</span><span class="sxs-lookup"><span data-stu-id="c4fe5-139">-Top</span></span>
<span data-ttu-id="c4fe5-140">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="c4fe5-140">OData top parameter.</span></span>

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

### <span data-ttu-id="c4fe5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fe5-141">CommonParameters</span></span>
<span data-ttu-id="c4fe5-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4fe5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fe5-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fe5-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4fe5-144">INPUTS</span></span>

### <span data-ttu-id="c4fe5-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c4fe5-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c4fe5-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4fe5-146">OUTPUTS</span></span>

### <span data-ttu-id="c4fe5-147">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="c4fe5-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="c4fe5-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4fe5-148">NOTES</span></span>

<span data-ttu-id="c4fe5-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4fe5-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c4fe5-151">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c4fe5-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4fe5-152">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c4fe5-153">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c4fe5-154">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c4fe5-155">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c4fe5-156">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c4fe5-157">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c4fe5-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c4fe5-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4fe5-159">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c4fe5-160">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c4fe5-161">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c4fe5-162">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c4fe5-163">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c4fe5-164">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c4fe5-165">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c4fe5-166">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c4fe5-167">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c4fe5-168">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c4fe5-169">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c4fe5-170">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c4fe5-171">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4fe5-172">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c4fe5-173">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c4fe5-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4fe5-174">RELATED LINKS</span></span>

