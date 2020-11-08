---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015227"
---
# <span data-ttu-id="15f6a-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="15f6a-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="15f6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="15f6a-103">Adja vissza a kért infrastruktúra szerepkör-példányt.</span><span class="sxs-lookup"><span data-stu-id="15f6a-103">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="15f6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15f6a-104">SYNTAX</span></span>

### <span data-ttu-id="15f6a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15f6a-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="15f6a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="15f6a-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="15f6a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15f6a-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="15f6a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15f6a-108">DESCRIPTION</span></span>
<span data-ttu-id="15f6a-109">Adja vissza a kért infrastruktúra szerepkör-példányt.</span><span class="sxs-lookup"><span data-stu-id="15f6a-109">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="15f6a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="15f6a-110">EXAMPLES</span></span>

### <span data-ttu-id="15f6a-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="15f6a-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

<span data-ttu-id="15f6a-112">Visszaadja az összes infrastruktúra-szerepkör-példány listáját.</span><span class="sxs-lookup"><span data-stu-id="15f6a-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="15f6a-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="15f6a-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

<span data-ttu-id="15f6a-114">A név alapján egyetlen infrastrukturális szerepkört ad vissza.</span><span class="sxs-lookup"><span data-stu-id="15f6a-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="15f6a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15f6a-115">PARAMETERS</span></span>

### <span data-ttu-id="15f6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f6a-116">-DefaultProfile</span></span>
<span data-ttu-id="15f6a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15f6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f6a-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="15f6a-118">-Filter</span></span>
<span data-ttu-id="15f6a-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="15f6a-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="15f6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15f6a-120">-InputObject</span></span>
<span data-ttu-id="15f6a-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="15f6a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15f6a-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="15f6a-122">-Location</span></span>
<span data-ttu-id="15f6a-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="15f6a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="15f6a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15f6a-124">-Name</span></span>
<span data-ttu-id="15f6a-125">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-125">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="15f6a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15f6a-126">-PassThru</span></span>
<span data-ttu-id="15f6a-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="15f6a-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15f6a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f6a-128">-ResourceGroupName</span></span>
<span data-ttu-id="15f6a-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="15f6a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15f6a-130">-SubscriptionId</span></span>
<span data-ttu-id="15f6a-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="15f6a-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="15f6a-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="15f6a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15f6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f6a-133">CommonParameters</span></span>
<span data-ttu-id="15f6a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15f6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f6a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="15f6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f6a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15f6a-136">INPUTS</span></span>

### <span data-ttu-id="15f6a-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="15f6a-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="15f6a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15f6a-138">OUTPUTS</span></span>

### <span data-ttu-id="15f6a-139">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IInfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="15f6a-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRoleInstance</span></span>



## <span data-ttu-id="15f6a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15f6a-140">NOTES</span></span>

<span data-ttu-id="15f6a-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="15f6a-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15f6a-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="15f6a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="15f6a-143">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="15f6a-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15f6a-144">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="15f6a-145">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="15f6a-146">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="15f6a-147">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="15f6a-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="15f6a-148">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="15f6a-149">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="15f6a-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="15f6a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15f6a-151">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="15f6a-152">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="15f6a-153">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="15f6a-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="15f6a-154">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="15f6a-155">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="15f6a-156">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="15f6a-157">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="15f6a-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="15f6a-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="15f6a-159">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="15f6a-160">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="15f6a-161">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="15f6a-162">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="15f6a-163">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="15f6a-164">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="15f6a-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="15f6a-165">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="15f6a-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="15f6a-166">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="15f6a-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="15f6a-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15f6a-167">RELATED LINKS</span></span>

