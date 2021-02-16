---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167754"
---
# <span data-ttu-id="3fcf0-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3fcf0-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="3fcf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcf0-103">Dedikált HSM létrehozása vagy frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3fcf0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3fcf0-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3fcf0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3fcf0-105">DESCRIPTION</span></span>
<span data-ttu-id="3fcf0-106">Dedikált HSM létrehozása vagy frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3fcf0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3fcf0-107">EXAMPLES</span></span>

### <span data-ttu-id="3fcf0-108">1. példa: Dedikált HSM létrehozása meglévő virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="3fcf0-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="3fcf0-109">Ez a parancs dedikált HSM-et hoz létre egy meglévő virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="3fcf0-110">**MEGJEGYZÉS:** Jelenleg korlátozott az eredmény, mielőtt a HSM teljesen ki lenne építve `New-AzDedicatedHsm` az Azure-on.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="3fcf0-111">Ezért ha létrehoz egy új HSM-et, a használat előtt ellenőrizze az állapotát, és győződjön meg arról, hogy `Get-AzDedicatedHsm` `Provisioning State` az a `Succeeded` megfelelő.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="3fcf0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fcf0-112">PARAMETERS</span></span>

### <span data-ttu-id="3fcf0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fcf0-113">-AsJob</span></span>
<span data-ttu-id="3fcf0-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="3fcf0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3fcf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcf0-115">-DefaultProfile</span></span>
<span data-ttu-id="3fcf0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fcf0-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3fcf0-117">-Location</span></span>
<span data-ttu-id="3fcf0-118">A támogatott Azure-hely, ahol létre kell hoznunk a dedikált HSM-et.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="3fcf0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3fcf0-119">-Name</span></span>
<span data-ttu-id="3fcf0-120">A dedikált Hsm neve</span><span class="sxs-lookup"><span data-stu-id="3fcf0-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="3fcf0-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3fcf0-121">-NetworkInterface</span></span>
<span data-ttu-id="3fcf0-122">A dedikált HSM-hez társított hálózati felületek erőforrás-azonosítójának listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="3fcf0-123">Ennek létrehozásáról az NETWORKINTERFACE tulajdonságokat és egy kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthat.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3fcf0-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3fcf0-124">-NoWait</span></span>
<span data-ttu-id="3fcf0-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="3fcf0-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3fcf0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcf0-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fcf0-127">Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="3fcf0-128">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="3fcf0-128">-Sku</span></span>
<span data-ttu-id="3fcf0-129">A dedikált HSM termékváltozata</span><span class="sxs-lookup"><span data-stu-id="3fcf0-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="3fcf0-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="3fcf0-130">-StampId</span></span>
<span data-ttu-id="3fcf0-131">Ezt a mezőt akkor használja a program, ha a RP nem támogatja az elérhetőségi zónákat.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="3fcf0-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3fcf0-132">-SubnetId</span></span>
<span data-ttu-id="3fcf0-133">A ARM/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="3fcf0-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="3fcf0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fcf0-134">-SubscriptionId</span></span>
<span data-ttu-id="3fcf0-135">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3fcf0-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3fcf0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fcf0-137">-Tag</span></span>
<span data-ttu-id="3fcf0-138">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="3fcf0-138">Resource tags</span></span>

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

### <span data-ttu-id="3fcf0-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="3fcf0-139">-Zone</span></span>
<span data-ttu-id="3fcf0-140">A dedikált Hsm zones.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="3fcf0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fcf0-141">-Confirm</span></span>
<span data-ttu-id="3fcf0-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcf0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcf0-143">-WhatIf</span></span>
<span data-ttu-id="3fcf0-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fcf0-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcf0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcf0-146">CommonParameters</span></span>
<span data-ttu-id="3fcf0-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcf0-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fcf0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcf0-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fcf0-149">INPUTS</span></span>

## <span data-ttu-id="3fcf0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fcf0-150">OUTPUTS</span></span>

### <span data-ttu-id="3fcf0-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3fcf0-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="3fcf0-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3fcf0-152">NOTES</span></span>

<span data-ttu-id="3fcf0-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3fcf0-153">ALIASES</span></span>

<span data-ttu-id="3fcf0-154">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3fcf0-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3fcf0-155">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3fcf0-156">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3fcf0-157">NETWORKINTERFACE <INetworkInterface[]>: A dedikált HSM-hez társított hálózati felületek erőforrás-azonosítóinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3fcf0-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="3fcf0-158">`[PrivateIPAddress <String>]`: A felület privát IP-címe</span><span class="sxs-lookup"><span data-stu-id="3fcf0-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="3fcf0-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fcf0-159">RELATED LINKS</span></span>

