---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297263"
---
# <span data-ttu-id="3cd1d-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3cd1d-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="3cd1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd1d-103">Dedikált HSM frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3cd1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cd1d-104">SYNTAX</span></span>

### <span data-ttu-id="3cd1d-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3cd1d-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3cd1d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3cd1d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3cd1d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cd1d-107">DESCRIPTION</span></span>
<span data-ttu-id="3cd1d-108">Dedikált HSM frissítése a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3cd1d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3cd1d-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd1d-110">1. példa: a dedikált HSM paraméter címkéjének frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="3cd1d-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="3cd1d-111">Ez a parancs frissíti a dedikált HSM paraméteres címkéjét név szerint.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="3cd1d-112">2. példa: a dedikált HSM által objektumhoz tartozó paraméter címkéjének frissítése</span><span class="sxs-lookup"><span data-stu-id="3cd1d-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="3cd1d-113">Ez a parancs frissíti a dedikált HSM objektum által létrehozott paraméter címkéjét.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="3cd1d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cd1d-114">PARAMETERS</span></span>

### <span data-ttu-id="3cd1d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cd1d-115">-AsJob</span></span>
<span data-ttu-id="3cd1d-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3cd1d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3cd1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd1d-117">-DefaultProfile</span></span>
<span data-ttu-id="3cd1d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cd1d-119">-InputObject</span></span>
<span data-ttu-id="3cd1d-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd1d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cd1d-121">-Name</span></span>
<span data-ttu-id="3cd1d-122">A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="3cd1d-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd1d-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="3cd1d-123">-NoWait</span></span>
<span data-ttu-id="3cd1d-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3cd1d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3cd1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cd1d-126">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd1d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cd1d-127">-SubscriptionId</span></span>
<span data-ttu-id="3cd1d-128">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3cd1d-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd1d-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="3cd1d-130">-Tag</span></span>
<span data-ttu-id="3cd1d-131">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="3cd1d-131">Resource tags</span></span>

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

### <span data-ttu-id="3cd1d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3cd1d-132">-Confirm</span></span>
<span data-ttu-id="3cd1d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd1d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd1d-134">-WhatIf</span></span>
<span data-ttu-id="3cd1d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd1d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd1d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd1d-137">CommonParameters</span></span>
<span data-ttu-id="3cd1d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cd1d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd1d-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd1d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cd1d-140">INPUTS</span></span>

### <span data-ttu-id="3cd1d-141">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="3cd1d-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="3cd1d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cd1d-142">OUTPUTS</span></span>

### <span data-ttu-id="3cd1d-143">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. modellek. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3cd1d-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="3cd1d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-144">NOTES</span></span>

<span data-ttu-id="3cd1d-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3cd1d-145">ALIASES</span></span>

<span data-ttu-id="3cd1d-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3cd1d-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3cd1d-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3cd1d-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3cd1d-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3cd1d-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3cd1d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3cd1d-151">`[Name <String>]`: A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="3cd1d-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="3cd1d-152">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="3cd1d-153">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3cd1d-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3cd1d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cd1d-155">RELATED LINKS</span></span>

