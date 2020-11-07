---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842630"
---
# <span data-ttu-id="4a50e-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="4a50e-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="4a50e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a50e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a50e-103">A kért peremhálózat-átjáró értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4a50e-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="4a50e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a50e-104">SYNTAX</span></span>

### <span data-ttu-id="4a50e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a50e-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4a50e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4a50e-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4a50e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a50e-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4a50e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a50e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a50e-109">A kért peremhálózat-átjáró értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4a50e-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="4a50e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4a50e-110">EXAMPLES</span></span>

### <span data-ttu-id="4a50e-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="4a50e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="4a50e-112">Egy adott helyen található összes peremhálózat-átjáró listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4a50e-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="4a50e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a50e-113">PARAMETERS</span></span>

### <span data-ttu-id="4a50e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a50e-114">-DefaultProfile</span></span>
<span data-ttu-id="4a50e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a50e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a50e-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="4a50e-116">-Filter</span></span>
<span data-ttu-id="4a50e-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="4a50e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="4a50e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a50e-118">-InputObject</span></span>
<span data-ttu-id="4a50e-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a50e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a50e-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="4a50e-120">-Location</span></span>
<span data-ttu-id="4a50e-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4a50e-121">Location of the resource.</span></span>

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

### <span data-ttu-id="4a50e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a50e-122">-Name</span></span>
<span data-ttu-id="4a50e-123">Az Edge átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="4a50e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a50e-124">-PassThru</span></span>
<span data-ttu-id="4a50e-125">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="4a50e-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a50e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a50e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a50e-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="4a50e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a50e-128">-SubscriptionId</span></span>
<span data-ttu-id="4a50e-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4a50e-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a50e-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4a50e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a50e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a50e-131">CommonParameters</span></span>
<span data-ttu-id="4a50e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a50e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a50e-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a50e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a50e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a50e-134">INPUTS</span></span>

### <span data-ttu-id="4a50e-135">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4a50e-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4a50e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a50e-136">OUTPUTS</span></span>

### <span data-ttu-id="4a50e-137">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="4a50e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="4a50e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a50e-138">NOTES</span></span>

<span data-ttu-id="4a50e-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4a50e-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a50e-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4a50e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a50e-141">INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4a50e-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a50e-142">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4a50e-143">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4a50e-144">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4a50e-145">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="4a50e-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4a50e-146">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4a50e-147">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4a50e-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4a50e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a50e-149">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4a50e-150">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4a50e-151">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4a50e-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4a50e-152">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4a50e-153">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4a50e-154">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4a50e-155">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="4a50e-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4a50e-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4a50e-157">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4a50e-158">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4a50e-159">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4a50e-160">`[StoragePool <String>]`: Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="4a50e-161">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4a50e-162">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4a50e-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4a50e-163">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4a50e-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4a50e-164">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="4a50e-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4a50e-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a50e-165">RELATED LINKS</span></span>

