---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015320"
---
# <span data-ttu-id="641a8-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="641a8-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="641a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="641a8-102">SYNOPSIS</span></span>
<span data-ttu-id="641a8-103">A kért anyag fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="641a8-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="641a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="641a8-104">SYNTAX</span></span>

### <span data-ttu-id="641a8-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="641a8-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="641a8-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="641a8-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="641a8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="641a8-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="641a8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="641a8-108">DESCRIPTION</span></span>
<span data-ttu-id="641a8-109">A kért anyag fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="641a8-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="641a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="641a8-110">EXAMPLES</span></span>

### <span data-ttu-id="641a8-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="641a8-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="641a8-112">Az összes fájlmegosztás listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="641a8-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="641a8-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="641a8-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="641a8-114">A név alapján a fájl megosztását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="641a8-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="641a8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="641a8-115">PARAMETERS</span></span>

### <span data-ttu-id="641a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641a8-116">-DefaultProfile</span></span>
<span data-ttu-id="641a8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="641a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="641a8-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="641a8-118">-Filter</span></span>
<span data-ttu-id="641a8-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="641a8-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="641a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="641a8-120">-InputObject</span></span>
<span data-ttu-id="641a8-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="641a8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="641a8-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="641a8-122">-Location</span></span>
<span data-ttu-id="641a8-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="641a8-123">Location of the resource.</span></span>

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

### <span data-ttu-id="641a8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="641a8-124">-Name</span></span>
<span data-ttu-id="641a8-125">A szövet fájl megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="641a8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="641a8-126">-PassThru</span></span>
<span data-ttu-id="641a8-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="641a8-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="641a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="641a8-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="641a8-130">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="641a8-130">-Skip</span></span>
<span data-ttu-id="641a8-131">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="641a8-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="641a8-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="641a8-132">-SubscriptionId</span></span>
<span data-ttu-id="641a8-133">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="641a8-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="641a8-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="641a8-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="641a8-135">-Top</span><span class="sxs-lookup"><span data-stu-id="641a8-135">-Top</span></span>
<span data-ttu-id="641a8-136">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="641a8-136">OData top parameter.</span></span>

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

### <span data-ttu-id="641a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641a8-137">CommonParameters</span></span>
<span data-ttu-id="641a8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="641a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641a8-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="641a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641a8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="641a8-140">INPUTS</span></span>

### <span data-ttu-id="641a8-141">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="641a8-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="641a8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="641a8-142">OUTPUTS</span></span>

### <span data-ttu-id="641a8-143">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="641a8-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="641a8-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="641a8-144">NOTES</span></span>

<span data-ttu-id="641a8-145">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="641a8-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="641a8-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="641a8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="641a8-147">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="641a8-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="641a8-148">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="641a8-149">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="641a8-150">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="641a8-151">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="641a8-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="641a8-152">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="641a8-153">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="641a8-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="641a8-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="641a8-155">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="641a8-156">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="641a8-157">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="641a8-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="641a8-158">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="641a8-159">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="641a8-160">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="641a8-161">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="641a8-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="641a8-162">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="641a8-163">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="641a8-164">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="641a8-165">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="641a8-166">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="641a8-167">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="641a8-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="641a8-168">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="641a8-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="641a8-169">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="641a8-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="641a8-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="641a8-170">RELATED LINKS</span></span>

