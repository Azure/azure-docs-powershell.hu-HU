---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298922"
---
# <span data-ttu-id="8216d-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="8216d-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="8216d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8216d-102">SYNOPSIS</span></span>
<span data-ttu-id="8216d-103">Társítás törlése</span><span class="sxs-lookup"><span data-stu-id="8216d-103">Delete an association.</span></span>

## <span data-ttu-id="8216d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8216d-104">SYNTAX</span></span>

### <span data-ttu-id="8216d-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8216d-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8216d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8216d-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8216d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8216d-107">DESCRIPTION</span></span>
<span data-ttu-id="8216d-108">Társítás törlése</span><span class="sxs-lookup"><span data-stu-id="8216d-108">Delete an association.</span></span>

## <span data-ttu-id="8216d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8216d-109">EXAMPLES</span></span>

### <span data-ttu-id="8216d-110">1. példa: egyéni szolgáltatói társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8216d-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="8216d-111">Egyéni szolgáltatói társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8216d-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="8216d-112">2. példa: egyéni szolgáltatói társítás eltávolítása csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="8216d-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="8216d-113">Az egyéni szolgáltatói társítás eltávolítása a csővezetékek és a PassThru funkció segítségével a siker vagy a kudarc jelzéséhez.</span><span class="sxs-lookup"><span data-stu-id="8216d-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="8216d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8216d-114">PARAMETERS</span></span>

### <span data-ttu-id="8216d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8216d-115">-AsJob</span></span>
<span data-ttu-id="8216d-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="8216d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8216d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8216d-117">-DefaultProfile</span></span>
<span data-ttu-id="8216d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8216d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8216d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8216d-119">-InputObject</span></span>
<span data-ttu-id="8216d-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8216d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8216d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8216d-121">-Name</span></span>
<span data-ttu-id="8216d-122">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="8216d-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8216d-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="8216d-123">-NoWait</span></span>
<span data-ttu-id="8216d-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="8216d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8216d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8216d-125">-PassThru</span></span>
<span data-ttu-id="8216d-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="8216d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8216d-127">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8216d-127">-Scope</span></span>
<span data-ttu-id="8216d-128">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="8216d-128">The scope of the association.</span></span>

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

### <span data-ttu-id="8216d-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8216d-129">-Confirm</span></span>
<span data-ttu-id="8216d-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8216d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8216d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8216d-131">-WhatIf</span></span>
<span data-ttu-id="8216d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8216d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8216d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8216d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8216d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8216d-134">CommonParameters</span></span>
<span data-ttu-id="8216d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8216d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8216d-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8216d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8216d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8216d-137">INPUTS</span></span>

### <span data-ttu-id="8216d-138">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="8216d-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="8216d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8216d-139">OUTPUTS</span></span>

### <span data-ttu-id="8216d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8216d-140">System.Boolean</span></span>

## <span data-ttu-id="8216d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8216d-141">NOTES</span></span>

<span data-ttu-id="8216d-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8216d-142">ALIASES</span></span>

<span data-ttu-id="8216d-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="8216d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8216d-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8216d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8216d-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8216d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8216d-146">INPUTOBJECT <ICustomProvidersIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8216d-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8216d-147">`[AssociationName <String>]`: A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="8216d-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="8216d-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8216d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8216d-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8216d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8216d-150">`[ResourceProviderName <String>]`: Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="8216d-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="8216d-151">`[Scope <String>]`: A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="8216d-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="8216d-152">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8216d-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8216d-153">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8216d-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8216d-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8216d-154">RELATED LINKS</span></span>

