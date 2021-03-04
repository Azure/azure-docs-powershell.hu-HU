---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925818"
---
# <span data-ttu-id="b2abb-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b2abb-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="b2abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2abb-102">SYNOPSIS</span></span>
<span data-ttu-id="b2abb-103">A megadott Azure dedikált HSM-et kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2abb-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b2abb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2abb-104">SYNTAX</span></span>

### <span data-ttu-id="b2abb-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2abb-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2abb-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b2abb-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2abb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2abb-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2abb-108">Lista</span><span class="sxs-lookup"><span data-stu-id="b2abb-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b2abb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2abb-109">DESCRIPTION</span></span>
<span data-ttu-id="b2abb-110">A megadott Azure dedikált HSM-et kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2abb-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b2abb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2abb-111">EXAMPLES</span></span>

### <span data-ttu-id="b2abb-112">1. példa: Az összes dedikált HSM lekért előfizetése</span><span class="sxs-lookup"><span data-stu-id="b2abb-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b2abb-113">Ez a parancs az összes dedikált HSM-et egy előfizetéshez kapja</span><span class="sxs-lookup"><span data-stu-id="b2abb-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="b2abb-114">2. példa: Az összes dedikált HSM lekérte egy erőforráscsoport alá.</span><span class="sxs-lookup"><span data-stu-id="b2abb-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b2abb-115">Ez a parancs az összes dedikált HSM-et egy erőforráscsoport alá kapja.</span><span class="sxs-lookup"><span data-stu-id="b2abb-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="b2abb-116">3. példa: Dedikált HSM lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="b2abb-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b2abb-117">Ez a parancs név szerint dedikált HSM-et kap.</span><span class="sxs-lookup"><span data-stu-id="b2abb-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="b2abb-118">4. példa: Dedikált HSM-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2abb-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b2abb-119">Ez a parancs objektumról dedikált HSM-et kap.</span><span class="sxs-lookup"><span data-stu-id="b2abb-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="b2abb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2abb-120">PARAMETERS</span></span>

### <span data-ttu-id="b2abb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2abb-121">-DefaultProfile</span></span>
<span data-ttu-id="b2abb-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2abb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2abb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2abb-123">-InputObject</span></span>
<span data-ttu-id="b2abb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b2abb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2abb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b2abb-125">-Name</span></span>
<span data-ttu-id="b2abb-126">A dedikált HSM neve.</span><span class="sxs-lookup"><span data-stu-id="b2abb-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="b2abb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2abb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2abb-128">Annak az erőforráscsoportnak a neve, amelyhez a dedikált hsm tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2abb-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="b2abb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2abb-129">-SubscriptionId</span></span>
<span data-ttu-id="b2abb-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b2abb-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2abb-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b2abb-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2abb-132">-Top</span><span class="sxs-lookup"><span data-stu-id="b2abb-132">-Top</span></span>
<span data-ttu-id="b2abb-133">A vissza nem térhet találatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b2abb-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="b2abb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2abb-134">CommonParameters</span></span>
<span data-ttu-id="b2abb-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2abb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2abb-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2abb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2abb-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2abb-137">INPUTS</span></span>

### <span data-ttu-id="b2abb-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="b2abb-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="b2abb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2abb-139">OUTPUTS</span></span>

### <span data-ttu-id="b2abb-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b2abb-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="b2abb-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2abb-141">NOTES</span></span>

<span data-ttu-id="b2abb-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b2abb-142">ALIASES</span></span>

<span data-ttu-id="b2abb-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b2abb-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2abb-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b2abb-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2abb-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2abb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2abb-146">INPUTOBJECT: <IDedicatedHsmIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b2abb-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2abb-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b2abb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2abb-148">`[Name <String>]`: A dedikált Hsm neve</span><span class="sxs-lookup"><span data-stu-id="b2abb-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="b2abb-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2abb-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="b2abb-150">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b2abb-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b2abb-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b2abb-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b2abb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2abb-152">RELATED LINKS</span></span>

