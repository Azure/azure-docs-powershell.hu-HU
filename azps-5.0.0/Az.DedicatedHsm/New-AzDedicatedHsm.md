---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297287"
---
# <span data-ttu-id="d7567-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="d7567-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="d7567-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7567-102">SYNOPSIS</span></span>
<span data-ttu-id="d7567-103">Dedikált HSM létrehozása vagy frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d7567-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="d7567-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7567-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d7567-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7567-105">DESCRIPTION</span></span>
<span data-ttu-id="d7567-106">Dedikált HSM létrehozása vagy frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d7567-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="d7567-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7567-107">EXAMPLES</span></span>

### <span data-ttu-id="d7567-108">Példa 1: dedikált HSM létrehozása meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="d7567-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="d7567-109">A parancs létrehoz egy dedikált HSM-t egy meglévő virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="d7567-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="d7567-110">**Megjegyzés:** Jelenleg `New-AzDedicatedHsm` olyan korlátozással rendelkezik, amelyet a HSM teljes kiépítése előtt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7567-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="d7567-111">Miután létrehozott egy új HSM-t, kérjük, hogy az állapotának lekérdezése, `Get-AzDedicatedHsm` és győződjön meg róla, hogy az új HSM `Provisioning State` `Succeeded` .</span><span class="sxs-lookup"><span data-stu-id="d7567-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="d7567-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7567-112">PARAMETERS</span></span>

### <span data-ttu-id="d7567-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7567-113">-AsJob</span></span>
<span data-ttu-id="d7567-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d7567-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d7567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7567-115">-DefaultProfile</span></span>
<span data-ttu-id="d7567-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7567-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7567-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="d7567-117">-Location</span></span>
<span data-ttu-id="d7567-118">A támogatott Azure-hely, ahol a dedikált HSM-t létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="d7567-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7567-119">-Name</span></span>
<span data-ttu-id="d7567-120">A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="d7567-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7567-121">-NetworkInterface</span></span>
<span data-ttu-id="d7567-122">A dedikált HSM-hez társított hálózati illesztők erőforrás-azonosítóinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7567-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="d7567-123">A kivitelezéshez tekintse meg a NETWORKINTERFACE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d7567-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="d7567-124">-NoWait</span></span>
<span data-ttu-id="d7567-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d7567-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d7567-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7567-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7567-127">Annak az erőforrás csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="d7567-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="d7567-128">-Sku</span></span>
<span data-ttu-id="d7567-129">A dedikált HSM SKU-je</span><span class="sxs-lookup"><span data-stu-id="d7567-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="d7567-130">-StampId</span></span>
<span data-ttu-id="d7567-131">Ezt a mezőt akkor fogja használni a program, ha az RP nem támogatja az elérhetőségi zónákat.</span><span class="sxs-lookup"><span data-stu-id="d7567-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-132">– NetI</span><span class="sxs-lookup"><span data-stu-id="d7567-132">-SubnetId</span></span>
<span data-ttu-id="d7567-133">A kar erőforrás-azonosítója/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/... formájában</span><span class="sxs-lookup"><span data-stu-id="d7567-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7567-134">-SubscriptionId</span></span>
<span data-ttu-id="d7567-135">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d7567-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7567-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d7567-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7567-137">-Tag</span></span>
<span data-ttu-id="d7567-138">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="d7567-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-139">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="d7567-139">-Zone</span></span>
<span data-ttu-id="d7567-140">A dedikált HSM-zónák.</span><span class="sxs-lookup"><span data-stu-id="d7567-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7567-141">-Confirm</span></span>
<span data-ttu-id="d7567-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7567-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7567-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7567-143">-WhatIf</span></span>
<span data-ttu-id="d7567-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7567-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7567-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7567-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7567-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7567-146">CommonParameters</span></span>
<span data-ttu-id="d7567-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7567-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7567-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7567-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7567-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7567-149">INPUTS</span></span>

## <span data-ttu-id="d7567-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7567-150">OUTPUTS</span></span>

### <span data-ttu-id="d7567-151">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. modellek. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="d7567-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="d7567-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7567-152">NOTES</span></span>

<span data-ttu-id="d7567-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d7567-153">ALIASES</span></span>

<span data-ttu-id="d7567-154">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d7567-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7567-155">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d7567-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7567-156">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d7567-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7567-157">NETWORKINTERFACE <INetworkInterface [] >: a dedikált HSM-hez társított hálózati illesztők erőforrás-azonosítóinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7567-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="d7567-158">`[PrivateIPAddress <String>]`: A felület privát IP-címe</span><span class="sxs-lookup"><span data-stu-id="d7567-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="d7567-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7567-159">RELATED LINKS</span></span>

