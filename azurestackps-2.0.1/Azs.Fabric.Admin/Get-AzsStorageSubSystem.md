---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015305"
---
# <span data-ttu-id="8fae1-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="8fae1-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="8fae1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fae1-102">SYNOPSIS</span></span>
<span data-ttu-id="8fae1-103">Adja vissza a kért tárolási alrendszert.</span><span class="sxs-lookup"><span data-stu-id="8fae1-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="8fae1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fae1-104">SYNTAX</span></span>

### <span data-ttu-id="8fae1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fae1-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8fae1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="8fae1-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8fae1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8fae1-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8fae1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fae1-108">DESCRIPTION</span></span>
<span data-ttu-id="8fae1-109">Adja vissza a kért tárolási alrendszert.</span><span class="sxs-lookup"><span data-stu-id="8fae1-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="8fae1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8fae1-110">EXAMPLES</span></span>

### <span data-ttu-id="8fae1-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="8fae1-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="8fae1-112">Az összes tárterület-alrendszert letölthet egy méretarányból.</span><span class="sxs-lookup"><span data-stu-id="8fae1-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="8fae1-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="8fae1-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="8fae1-114">Adja meg a tárterület-alrendszer méretarányát és nevét.</span><span class="sxs-lookup"><span data-stu-id="8fae1-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="8fae1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fae1-115">PARAMETERS</span></span>

### <span data-ttu-id="8fae1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fae1-116">-DefaultProfile</span></span>
<span data-ttu-id="8fae1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fae1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fae1-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="8fae1-118">-Filter</span></span>
<span data-ttu-id="8fae1-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="8fae1-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="8fae1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fae1-120">-InputObject</span></span>
<span data-ttu-id="8fae1-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fae1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8fae1-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="8fae1-122">-Location</span></span>
<span data-ttu-id="8fae1-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8fae1-123">Location of the resource.</span></span>

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

### <span data-ttu-id="8fae1-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fae1-124">-Name</span></span>
<span data-ttu-id="8fae1-125">A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="8fae1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fae1-126">-PassThru</span></span>
<span data-ttu-id="8fae1-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="8fae1-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8fae1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fae1-128">-ResourceGroupName</span></span>
<span data-ttu-id="8fae1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="8fae1-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8fae1-130">-ScaleUnit</span></span>
<span data-ttu-id="8fae1-131">A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="8fae1-132">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="8fae1-132">-Skip</span></span>
<span data-ttu-id="8fae1-133">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="8fae1-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="8fae1-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fae1-134">-SubscriptionId</span></span>
<span data-ttu-id="8fae1-135">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8fae1-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8fae1-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8fae1-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8fae1-137">-Top</span><span class="sxs-lookup"><span data-stu-id="8fae1-137">-Top</span></span>
<span data-ttu-id="8fae1-138">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="8fae1-138">OData top parameter.</span></span>

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

### <span data-ttu-id="8fae1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fae1-139">CommonParameters</span></span>
<span data-ttu-id="8fae1-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fae1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fae1-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fae1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fae1-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fae1-142">INPUTS</span></span>

### <span data-ttu-id="8fae1-143">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8fae1-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8fae1-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fae1-144">OUTPUTS</span></span>

### <span data-ttu-id="8fae1-145">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="8fae1-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="8fae1-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fae1-146">NOTES</span></span>

<span data-ttu-id="8fae1-147">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8fae1-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8fae1-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8fae1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8fae1-149">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8fae1-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8fae1-150">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8fae1-151">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8fae1-152">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8fae1-153">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="8fae1-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8fae1-154">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8fae1-155">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8fae1-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8fae1-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8fae1-157">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8fae1-158">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8fae1-159">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8fae1-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8fae1-160">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8fae1-161">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8fae1-162">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8fae1-163">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="8fae1-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8fae1-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8fae1-165">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8fae1-166">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8fae1-167">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8fae1-168">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8fae1-169">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8fae1-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8fae1-170">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8fae1-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8fae1-171">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="8fae1-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8fae1-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fae1-172">RELATED LINKS</span></span>

