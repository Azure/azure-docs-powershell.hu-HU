---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339065"
---
# <span data-ttu-id="06644-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="06644-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="06644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06644-102">SYNOPSIS</span></span>
<span data-ttu-id="06644-103">Virtuális gép képsablonjának törlése</span><span class="sxs-lookup"><span data-stu-id="06644-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="06644-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06644-104">SYNTAX</span></span>

### <span data-ttu-id="06644-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06644-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="06644-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06644-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06644-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06644-107">DESCRIPTION</span></span>
<span data-ttu-id="06644-108">Virtuális gép képsablonjának törlése</span><span class="sxs-lookup"><span data-stu-id="06644-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="06644-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06644-109">EXAMPLES</span></span>

### <span data-ttu-id="06644-110">1. példa: Képsablon eltávolítása</span><span class="sxs-lookup"><span data-stu-id="06644-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="06644-111">Ez a parancs eltávolít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="06644-111">This command removes a image template.</span></span>

### <span data-ttu-id="06644-112">2. példa: Képsablon eltávolítása</span><span class="sxs-lookup"><span data-stu-id="06644-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="06644-113">Ez a parancs eltávolít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="06644-113">This command removes a image template.</span></span>

## <span data-ttu-id="06644-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06644-114">PARAMETERS</span></span>

### <span data-ttu-id="06644-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06644-115">-AsJob</span></span>
<span data-ttu-id="06644-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="06644-116">Run the command as a job</span></span>

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

### <span data-ttu-id="06644-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06644-117">-DefaultProfile</span></span>
<span data-ttu-id="06644-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06644-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06644-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="06644-119">-ImageTemplateName</span></span>
<span data-ttu-id="06644-120">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="06644-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06644-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06644-121">-InputObject</span></span>
<span data-ttu-id="06644-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="06644-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06644-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06644-123">-NoWait</span></span>
<span data-ttu-id="06644-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="06644-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06644-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06644-125">-PassThru</span></span>
<span data-ttu-id="06644-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="06644-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06644-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06644-127">-ResourceGroupName</span></span>
<span data-ttu-id="06644-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06644-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="06644-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06644-129">-SubscriptionId</span></span>
<span data-ttu-id="06644-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="06644-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06644-131">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="06644-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06644-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06644-132">-Confirm</span></span>
<span data-ttu-id="06644-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06644-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06644-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06644-134">-WhatIf</span></span>
<span data-ttu-id="06644-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06644-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06644-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06644-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06644-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06644-137">CommonParameters</span></span>
<span data-ttu-id="06644-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06644-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06644-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06644-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06644-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06644-140">INPUTS</span></span>

### <span data-ttu-id="06644-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="06644-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="06644-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06644-142">OUTPUTS</span></span>

### <span data-ttu-id="06644-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06644-143">System.Boolean</span></span>

## <span data-ttu-id="06644-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06644-144">NOTES</span></span>

<span data-ttu-id="06644-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="06644-145">ALIASES</span></span>

<span data-ttu-id="06644-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="06644-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06644-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="06644-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06644-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06644-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06644-149">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="06644-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06644-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="06644-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06644-151">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="06644-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="06644-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06644-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="06644-153">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="06644-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="06644-154">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="06644-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06644-155">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="06644-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06644-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06644-156">RELATED LINKS</span></span>

