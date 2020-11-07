---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: dcd4f9da702425808e3e2565a7b668930ff7aa32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842605"
---
# <span data-ttu-id="b1289-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="b1289-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="b1289-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1289-102">SYNOPSIS</span></span>
<span data-ttu-id="b1289-103">A kért infrastrukturális szerepkör leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1289-103">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="b1289-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1289-104">SYNTAX</span></span>

### <span data-ttu-id="b1289-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1289-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b1289-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1289-106">Get</span></span>
```
Get-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b1289-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1289-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b1289-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1289-108">DESCRIPTION</span></span>
<span data-ttu-id="b1289-109">A kért infrastrukturális szerepkör leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1289-109">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="b1289-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b1289-110">EXAMPLES</span></span>

### <span data-ttu-id="b1289-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="b1289-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole

A list of all infrastructure roles.
```

<span data-ttu-id="b1289-112">A teljes infrastruktúra-szerepkörök listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1289-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="b1289-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="b1289-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole -Name "Active Directory Federation Services"

An infrastructure role based on the name.
```

<span data-ttu-id="b1289-114">A név alapján Ismerje meg az infrastruktúra szerepkört.</span><span class="sxs-lookup"><span data-stu-id="b1289-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="b1289-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1289-115">PARAMETERS</span></span>

### <span data-ttu-id="b1289-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1289-116">-DefaultProfile</span></span>
<span data-ttu-id="b1289-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1289-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1289-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b1289-118">-Filter</span></span>
<span data-ttu-id="b1289-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b1289-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="b1289-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1289-120">-InputObject</span></span>
<span data-ttu-id="b1289-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1289-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1289-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="b1289-122">-Location</span></span>
<span data-ttu-id="b1289-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b1289-123">Location of the resource.</span></span>

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

### <span data-ttu-id="b1289-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1289-124">-Name</span></span>
<span data-ttu-id="b1289-125">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-125">Infrastructure role name.</span></span>

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

### <span data-ttu-id="b1289-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1289-126">-PassThru</span></span>
<span data-ttu-id="b1289-127">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="b1289-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1289-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1289-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1289-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="b1289-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1289-130">-SubscriptionId</span></span>
<span data-ttu-id="b1289-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b1289-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1289-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b1289-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1289-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1289-133">CommonParameters</span></span>
<span data-ttu-id="b1289-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1289-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1289-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1289-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1289-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1289-136">INPUTS</span></span>

### <span data-ttu-id="b1289-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b1289-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b1289-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1289-138">OUTPUTS</span></span>

### <span data-ttu-id="b1289-139">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IInfraRole</span><span class="sxs-lookup"><span data-stu-id="b1289-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRole</span></span>



## <span data-ttu-id="b1289-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1289-140">NOTES</span></span>

<span data-ttu-id="b1289-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b1289-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1289-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b1289-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b1289-143">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b1289-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1289-144">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b1289-145">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b1289-146">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b1289-147">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="b1289-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b1289-148">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b1289-149">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b1289-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b1289-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1289-151">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b1289-152">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b1289-153">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b1289-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b1289-154">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b1289-155">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b1289-156">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b1289-157">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="b1289-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b1289-158">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b1289-159">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b1289-160">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b1289-161">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b1289-162">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="b1289-163">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b1289-164">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b1289-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b1289-165">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b1289-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b1289-166">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="b1289-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b1289-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1289-167">RELATED LINKS</span></span>

