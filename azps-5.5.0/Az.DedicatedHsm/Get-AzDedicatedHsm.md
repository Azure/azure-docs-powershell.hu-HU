---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165259"
---
# <span data-ttu-id="0505e-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="0505e-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="0505e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0505e-102">SYNOPSIS</span></span>
<span data-ttu-id="0505e-103">A megadott Azure dedikált HSM-et kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0505e-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="0505e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0505e-104">SYNTAX</span></span>

### <span data-ttu-id="0505e-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0505e-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0505e-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0505e-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0505e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0505e-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0505e-108">Lista</span><span class="sxs-lookup"><span data-stu-id="0505e-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0505e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0505e-109">DESCRIPTION</span></span>
<span data-ttu-id="0505e-110">A megadott Azure dedikált HSM-et kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0505e-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="0505e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0505e-111">EXAMPLES</span></span>

### <span data-ttu-id="0505e-112">1. példa: Az összes dedikált HSM lekért előfizetése</span><span class="sxs-lookup"><span data-stu-id="0505e-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="0505e-113">Ez a parancs az összes dedikált HSM-et egy előfizetéshez kapja</span><span class="sxs-lookup"><span data-stu-id="0505e-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="0505e-114">2. példa: Az összes dedikált HSM lekérte egy erőforráscsoport alá.</span><span class="sxs-lookup"><span data-stu-id="0505e-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="0505e-115">Ez a parancs az összes dedikált HSM-et egy erőforráscsoport alá kapja.</span><span class="sxs-lookup"><span data-stu-id="0505e-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="0505e-116">3. példa: Dedikált HSM lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="0505e-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="0505e-117">Ez a parancs név szerint dedikált HSM-et kap.</span><span class="sxs-lookup"><span data-stu-id="0505e-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="0505e-118">4. példa: Dedikált HSM-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="0505e-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="0505e-119">Ez a parancs objektumról dedikált HSM-et kap.</span><span class="sxs-lookup"><span data-stu-id="0505e-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="0505e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0505e-120">PARAMETERS</span></span>

### <span data-ttu-id="0505e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0505e-121">-DefaultProfile</span></span>
<span data-ttu-id="0505e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0505e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0505e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0505e-123">-InputObject</span></span>
<span data-ttu-id="0505e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0505e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0505e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0505e-125">-Name</span></span>
<span data-ttu-id="0505e-126">A dedikált HSM neve.</span><span class="sxs-lookup"><span data-stu-id="0505e-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="0505e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0505e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0505e-128">Annak az erőforráscsoportnak a neve, amelyhez a dedikált hsm tartozik.</span><span class="sxs-lookup"><span data-stu-id="0505e-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="0505e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0505e-129">-SubscriptionId</span></span>
<span data-ttu-id="0505e-130">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0505e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0505e-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0505e-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0505e-132">-Top</span><span class="sxs-lookup"><span data-stu-id="0505e-132">-Top</span></span>
<span data-ttu-id="0505e-133">A vissza nem térhet találatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="0505e-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0505e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0505e-134">CommonParameters</span></span>
<span data-ttu-id="0505e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0505e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0505e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0505e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0505e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0505e-137">INPUTS</span></span>

### <span data-ttu-id="0505e-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="0505e-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="0505e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0505e-139">OUTPUTS</span></span>

### <span data-ttu-id="0505e-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="0505e-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="0505e-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0505e-141">NOTES</span></span>

<span data-ttu-id="0505e-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0505e-142">ALIASES</span></span>

<span data-ttu-id="0505e-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0505e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0505e-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0505e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0505e-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0505e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0505e-146">INPUTOBJECT: <IDedicatedHsmIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0505e-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0505e-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0505e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0505e-148">`[Name <String>]`: A dedikált Hsm neve</span><span class="sxs-lookup"><span data-stu-id="0505e-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="0505e-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="0505e-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="0505e-150">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0505e-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0505e-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0505e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0505e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0505e-152">RELATED LINKS</span></span>

