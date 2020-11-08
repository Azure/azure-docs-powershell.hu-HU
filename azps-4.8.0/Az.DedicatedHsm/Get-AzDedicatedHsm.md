---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184558"
---
# <span data-ttu-id="18d43-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="18d43-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="18d43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18d43-102">SYNOPSIS</span></span>
<span data-ttu-id="18d43-103">A megadott Azure dedikált HSM kapja meg.</span><span class="sxs-lookup"><span data-stu-id="18d43-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="18d43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18d43-104">SYNTAX</span></span>

### <span data-ttu-id="18d43-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18d43-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="18d43-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="18d43-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18d43-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18d43-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18d43-108">Lista</span><span class="sxs-lookup"><span data-stu-id="18d43-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="18d43-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="18d43-109">DESCRIPTION</span></span>
<span data-ttu-id="18d43-110">A megadott Azure dedikált HSM kapja meg.</span><span class="sxs-lookup"><span data-stu-id="18d43-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="18d43-111">Példák</span><span class="sxs-lookup"><span data-stu-id="18d43-111">EXAMPLES</span></span>

### <span data-ttu-id="18d43-112">Példa 1: az összes dedikált HSM beszerzése az előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="18d43-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="18d43-113">Ez a parancs egy előfizetéshez tartozó dedikált HSM-t kap</span><span class="sxs-lookup"><span data-stu-id="18d43-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="18d43-114">2. példa: a dedikált HSM beszerzése egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="18d43-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="18d43-115">Ez a parancs egy erőforráscsoport alatt kapja meg az összes dedikált HSM-csoportot.</span><span class="sxs-lookup"><span data-stu-id="18d43-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="18d43-116">3. példa: dedikált HSM-név beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="18d43-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="18d43-117">Ez a parancs név szerint kapja meg a dedikált HSM-t.</span><span class="sxs-lookup"><span data-stu-id="18d43-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="18d43-118">4. példa: dedikált HSM-objektum beszerzése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="18d43-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="18d43-119">Ez a parancs a dedikált HSM objektumot objektum szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="18d43-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="18d43-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18d43-120">PARAMETERS</span></span>

### <span data-ttu-id="18d43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d43-121">-DefaultProfile</span></span>
<span data-ttu-id="18d43-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18d43-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18d43-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18d43-123">-InputObject</span></span>
<span data-ttu-id="18d43-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="18d43-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18d43-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18d43-125">-Name</span></span>
<span data-ttu-id="18d43-126">A dedikált HSM neve.</span><span class="sxs-lookup"><span data-stu-id="18d43-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="18d43-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d43-127">-ResourceGroupName</span></span>
<span data-ttu-id="18d43-128">Annak az Erőforráscsoportnek a neve, amelyhez a kijelölt HSM tartozik.</span><span class="sxs-lookup"><span data-stu-id="18d43-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="18d43-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18d43-129">-SubscriptionId</span></span>
<span data-ttu-id="18d43-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="18d43-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18d43-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="18d43-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18d43-132">-Top</span><span class="sxs-lookup"><span data-stu-id="18d43-132">-Top</span></span>
<span data-ttu-id="18d43-133">Eredményül kapott találatok maximális száma</span><span class="sxs-lookup"><span data-stu-id="18d43-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="18d43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d43-134">CommonParameters</span></span>
<span data-ttu-id="18d43-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18d43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d43-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="18d43-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d43-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d43-137">INPUTS</span></span>

### <span data-ttu-id="18d43-138">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="18d43-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="18d43-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d43-139">OUTPUTS</span></span>

### <span data-ttu-id="18d43-140">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. modellek. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="18d43-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="18d43-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18d43-141">NOTES</span></span>

<span data-ttu-id="18d43-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="18d43-142">ALIASES</span></span>

<span data-ttu-id="18d43-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="18d43-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18d43-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="18d43-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18d43-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="18d43-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18d43-146">INPUTOBJECT <IDedicatedHsmIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="18d43-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18d43-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="18d43-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18d43-148">`[Name <String>]`: A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="18d43-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="18d43-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="18d43-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="18d43-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="18d43-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18d43-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="18d43-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18d43-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18d43-152">RELATED LINKS</span></span>

