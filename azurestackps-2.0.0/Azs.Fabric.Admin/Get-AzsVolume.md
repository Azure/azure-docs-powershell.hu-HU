---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842594"
---
# <span data-ttu-id="4a41a-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="4a41a-101">Get-AzsVolume</span></span>

## <span data-ttu-id="4a41a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a41a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a41a-103">Adja vissza a kért tárterület-mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="4a41a-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="4a41a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a41a-104">SYNTAX</span></span>

### <span data-ttu-id="4a41a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a41a-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4a41a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4a41a-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="4a41a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a41a-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4a41a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a41a-108">DESCRIPTION</span></span>
<span data-ttu-id="4a41a-109">Adja vissza a kért tárterület-mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="4a41a-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="4a41a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4a41a-110">EXAMPLES</span></span>

### <span data-ttu-id="4a41a-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="4a41a-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="4a41a-112">A tárterület minden tárolási kötetének listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="4a41a-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="4a41a-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="4a41a-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="4a41a-114">A tárterületet a megadott helyen, név szerint érheti el.</span><span class="sxs-lookup"><span data-stu-id="4a41a-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="4a41a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a41a-115">PARAMETERS</span></span>

### <span data-ttu-id="4a41a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a41a-116">-DefaultProfile</span></span>
<span data-ttu-id="4a41a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a41a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a41a-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="4a41a-118">-Filter</span></span>
<span data-ttu-id="4a41a-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="4a41a-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="4a41a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a41a-120">-InputObject</span></span>
<span data-ttu-id="4a41a-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a41a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a41a-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="4a41a-122">-Location</span></span>
<span data-ttu-id="4a41a-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4a41a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="4a41a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a41a-124">-Name</span></span>
<span data-ttu-id="4a41a-125">A tárterület neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="4a41a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a41a-126">-PassThru</span></span>
<span data-ttu-id="4a41a-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="4a41a-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a41a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a41a-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a41a-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="4a41a-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4a41a-130">-ScaleUnit</span></span>
<span data-ttu-id="4a41a-131">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="4a41a-132">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="4a41a-132">-Skip</span></span>
<span data-ttu-id="4a41a-133">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="4a41a-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="4a41a-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4a41a-134">-StorageSubSystem</span></span>
<span data-ttu-id="4a41a-135">A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="4a41a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a41a-136">-SubscriptionId</span></span>
<span data-ttu-id="4a41a-137">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4a41a-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a41a-138">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4a41a-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a41a-139">-Top</span><span class="sxs-lookup"><span data-stu-id="4a41a-139">-Top</span></span>
<span data-ttu-id="4a41a-140">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="4a41a-140">OData top parameter.</span></span>

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

### <span data-ttu-id="4a41a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a41a-141">CommonParameters</span></span>
<span data-ttu-id="4a41a-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a41a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a41a-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a41a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a41a-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a41a-144">INPUTS</span></span>

### <span data-ttu-id="4a41a-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4a41a-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4a41a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a41a-146">OUTPUTS</span></span>

### <span data-ttu-id="4a41a-147">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20190501. IVolume</span><span class="sxs-lookup"><span data-stu-id="4a41a-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="4a41a-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a41a-148">NOTES</span></span>

<span data-ttu-id="4a41a-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4a41a-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a41a-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4a41a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a41a-151">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4a41a-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a41a-152">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4a41a-153">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4a41a-154">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4a41a-155">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="4a41a-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4a41a-156">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4a41a-157">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4a41a-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4a41a-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a41a-159">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4a41a-160">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4a41a-161">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4a41a-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4a41a-162">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4a41a-163">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4a41a-164">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4a41a-165">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="4a41a-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4a41a-166">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4a41a-167">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4a41a-168">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4a41a-169">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4a41a-170">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4a41a-171">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4a41a-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4a41a-172">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4a41a-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4a41a-173">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="4a41a-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4a41a-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a41a-174">RELATED LINKS</span></span>

