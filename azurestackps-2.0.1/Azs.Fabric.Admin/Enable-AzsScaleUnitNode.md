---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015229"
---
# <span data-ttu-id="8d678-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8d678-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8d678-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d678-102">SYNOPSIS</span></span>


## <span data-ttu-id="8d678-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d678-103">SYNTAX</span></span>

### <span data-ttu-id="8d678-104">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d678-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d678-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d678-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d678-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d678-106">DESCRIPTION</span></span>


## <span data-ttu-id="8d678-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d678-107">EXAMPLES</span></span>

### <span data-ttu-id="8d678-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="8d678-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="8d678-109">A méretarányos csomópont karbantartási módjának leállítása</span><span class="sxs-lookup"><span data-stu-id="8d678-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="8d678-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d678-110">PARAMETERS</span></span>

### <span data-ttu-id="8d678-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d678-111">-AsJob</span></span>


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

### <span data-ttu-id="8d678-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d678-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="8d678-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8d678-113">-Force</span></span>


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

### <span data-ttu-id="8d678-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d678-114">-InputObject</span></span>
<span data-ttu-id="8d678-115">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8d678-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="8d678-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d678-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-118">-Várva</span><span class="sxs-lookup"><span data-stu-id="8d678-118">-NoWait</span></span>


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

### <span data-ttu-id="8d678-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d678-119">-PassThru</span></span>


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

### <span data-ttu-id="8d678-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d678-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d678-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d678-122">-Confirm</span></span>
<span data-ttu-id="8d678-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d678-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d678-124">-WhatIf</span></span>
<span data-ttu-id="8d678-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d678-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d678-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d678-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d678-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d678-127">CommonParameters</span></span>
<span data-ttu-id="8d678-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d678-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d678-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d678-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d678-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d678-130">INPUTS</span></span>

### <span data-ttu-id="8d678-131">Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8d678-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8d678-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d678-132">OUTPUTS</span></span>

### <span data-ttu-id="8d678-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d678-133">System.Boolean</span></span>



## <span data-ttu-id="8d678-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d678-134">NOTES</span></span>

<span data-ttu-id="8d678-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8d678-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d678-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8d678-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8d678-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="8d678-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="8d678-138">`[Drive <String>]`: A tároló meghajtó neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8d678-139">`[EdgeGateway <String>]`: Az Edge-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8d678-140">`[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8d678-141">`[FabricLocation <String>]`: Szövet helye.</span><span class="sxs-lookup"><span data-stu-id="8d678-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8d678-142">`[FileShare <String>]`: A szövet-fájlmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8d678-143">`[IPPool <String>]`: IP-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8d678-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8d678-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d678-145">`[InfraRole <String>]`: Infrastrukturális szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8d678-146">`[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8d678-147">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8d678-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8d678-148">`[LogicalNetwork <String>]`: A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8d678-149">`[LogicalSubnet <String>]`: A logikai alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8d678-150">`[MacAddressPool <String>]`: A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8d678-151">`[Operation <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="8d678-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8d678-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8d678-153">`[ScaleUnit <String>]`: A méretarány neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8d678-154">`[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8d678-155">`[SlbMuxInstance <String>]`: A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8d678-156">`[StorageSubSystem <String>]`: A tárolási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8d678-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8d678-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d678-158">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8d678-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8d678-159">`[Volume <String>]`: A tárolási mennyiség neve.</span><span class="sxs-lookup"><span data-stu-id="8d678-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8d678-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d678-160">RELATED LINKS</span></span>

