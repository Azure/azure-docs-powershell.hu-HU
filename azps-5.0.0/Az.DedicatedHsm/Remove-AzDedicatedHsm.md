---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297281"
---
# <span data-ttu-id="76de8-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="76de8-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="76de8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76de8-102">SYNOPSIS</span></span>
<span data-ttu-id="76de8-103">A megadott Azure dedikált HSM törlése</span><span class="sxs-lookup"><span data-stu-id="76de8-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="76de8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76de8-104">SYNTAX</span></span>

### <span data-ttu-id="76de8-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76de8-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76de8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76de8-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76de8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76de8-107">DESCRIPTION</span></span>
<span data-ttu-id="76de8-108">A megadott Azure dedikált HSM törlése</span><span class="sxs-lookup"><span data-stu-id="76de8-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="76de8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76de8-109">EXAMPLES</span></span>

### <span data-ttu-id="76de8-110">Példa 1: dedikált HSM eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="76de8-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="76de8-111">Ez a commnad a hardveres biztonsági modult (HSM) távolítja el név szerint.</span><span class="sxs-lookup"><span data-stu-id="76de8-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="76de8-112">2. példa: dedikált HSM eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="76de8-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="76de8-113">Ez a commnad objektumból távolítja el az dedikált HSM-t.</span><span class="sxs-lookup"><span data-stu-id="76de8-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="76de8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76de8-114">PARAMETERS</span></span>

### <span data-ttu-id="76de8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76de8-115">-AsJob</span></span>
<span data-ttu-id="76de8-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="76de8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="76de8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76de8-117">-DefaultProfile</span></span>
<span data-ttu-id="76de8-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76de8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76de8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76de8-119">-InputObject</span></span>
<span data-ttu-id="76de8-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76de8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76de8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76de8-121">-Name</span></span>
<span data-ttu-id="76de8-122">A törlendő dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="76de8-122">The name of the dedicated HSM to delete</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76de8-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="76de8-123">-NoWait</span></span>
<span data-ttu-id="76de8-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="76de8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76de8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76de8-125">-PassThru</span></span>
<span data-ttu-id="76de8-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="76de8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="76de8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76de8-127">-ResourceGroupName</span></span>
<span data-ttu-id="76de8-128">Annak az Erőforráscsoportnek a neve, amelyhez a kijelölt HSM tartozik.</span><span class="sxs-lookup"><span data-stu-id="76de8-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76de8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76de8-129">-SubscriptionId</span></span>
<span data-ttu-id="76de8-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="76de8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76de8-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="76de8-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76de8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76de8-132">-Confirm</span></span>
<span data-ttu-id="76de8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76de8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76de8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76de8-134">-WhatIf</span></span>
<span data-ttu-id="76de8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76de8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76de8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76de8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76de8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76de8-137">CommonParameters</span></span>
<span data-ttu-id="76de8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76de8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76de8-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76de8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76de8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76de8-140">INPUTS</span></span>

### <span data-ttu-id="76de8-141">Microsoft. Azure. PowerShell. parancsmagok. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="76de8-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="76de8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76de8-142">OUTPUTS</span></span>

### <span data-ttu-id="76de8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76de8-143">System.Boolean</span></span>

## <span data-ttu-id="76de8-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76de8-144">NOTES</span></span>

<span data-ttu-id="76de8-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="76de8-145">ALIASES</span></span>

<span data-ttu-id="76de8-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="76de8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76de8-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="76de8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76de8-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="76de8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76de8-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="76de8-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76de8-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="76de8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76de8-151">`[Name <String>]`: A dedikált HSM neve</span><span class="sxs-lookup"><span data-stu-id="76de8-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="76de8-152">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez az erőforrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="76de8-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="76de8-153">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="76de8-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76de8-154">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="76de8-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76de8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76de8-155">RELATED LINKS</span></span>

