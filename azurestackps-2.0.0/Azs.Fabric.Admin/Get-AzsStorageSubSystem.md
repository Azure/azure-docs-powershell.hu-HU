---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842598"
---
# <span data-ttu-id="93f7f-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="93f7f-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="93f7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="93f7f-103">Adja vissza a kért tárolási alrendszert.</span><span class="sxs-lookup"><span data-stu-id="93f7f-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="93f7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93f7f-104">SYNTAX</span></span>

### <span data-ttu-id="93f7f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93f7f-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="93f7f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="93f7f-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="93f7f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93f7f-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="93f7f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="93f7f-108">DESCRIPTION</span></span>
<span data-ttu-id="93f7f-109">Adja vissza a kért tárolási alrendszert.</span><span class="sxs-lookup"><span data-stu-id="93f7f-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="93f7f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="93f7f-110">EXAMPLES</span></span>

### <span data-ttu-id="93f7f-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="93f7f-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="93f7f-112">Az összes tárterület-alrendszert letölthet egy méretarányból.</span><span class="sxs-lookup"><span data-stu-id="93f7f-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="93f7f-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="93f7f-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="93f7f-114">Adja meg a tárterület-alrendszer méretarányát és nevét.</span><span class="sxs-lookup"><span data-stu-id="93f7f-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="93f7f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93f7f-115">PARAMETERS</span></span>

### <span data-ttu-id="93f7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f7f-116">-DefaultProfile</span></span>
<span data-ttu-id="93f7f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93f7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f7f-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="93f7f-118">-Filter</span></span>
<span data-ttu-id="93f7f-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="93f7f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="93f7f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f7f-120">-InputObject</span></span>
<span data-ttu-id="93f7f-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93f7f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93f7f-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="93f7f-122">-Location</span></span>
<span data-ttu-id="93f7f-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="93f7f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="93f7f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93f7f-124">-Name</span></span>
<span data-ttu-id="93f7f-125">A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="93f7f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93f7f-126">-PassThru</span></span>
<span data-ttu-id="93f7f-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="93f7f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93f7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="93f7f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="93f7f-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="93f7f-130">-ScaleUnit</span></span>
<span data-ttu-id="93f7f-131">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="93f7f-132">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="93f7f-132">-Skip</span></span>
<span data-ttu-id="93f7f-133">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="93f7f-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="93f7f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93f7f-134">-SubscriptionId</span></span>
<span data-ttu-id="93f7f-135">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="93f7f-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="93f7f-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="93f7f-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="93f7f-137">-Top</span><span class="sxs-lookup"><span data-stu-id="93f7f-137">-Top</span></span>
<span data-ttu-id="93f7f-138">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="93f7f-138">OData top parameter.</span></span>

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

### <span data-ttu-id="93f7f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f7f-139">CommonParameters</span></span>
<span data-ttu-id="93f7f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93f7f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f7f-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93f7f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f7f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93f7f-142">INPUTS</span></span>

### <span data-ttu-id="93f7f-143">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="93f7f-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="93f7f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93f7f-144">OUTPUTS</span></span>

### <span data-ttu-id="93f7f-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="93f7f-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="93f7f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93f7f-146">NOTES</span></span>

<span data-ttu-id="93f7f-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="93f7f-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93f7f-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="93f7f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93f7f-149">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="93f7f-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93f7f-150">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="93f7f-151">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="93f7f-152">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="93f7f-153">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="93f7f-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="93f7f-154">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="93f7f-155">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="93f7f-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="93f7f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93f7f-157">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="93f7f-158">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="93f7f-159">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="93f7f-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="93f7f-160">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="93f7f-161">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="93f7f-162">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="93f7f-163">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="93f7f-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="93f7f-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="93f7f-165">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="93f7f-166">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="93f7f-167">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="93f7f-168">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="93f7f-169">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="93f7f-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="93f7f-170">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="93f7f-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93f7f-171">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="93f7f-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="93f7f-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93f7f-172">RELATED LINKS</span></span>

