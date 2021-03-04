---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 75065d50b8176b256c5cf91c136f4f4588232e55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924946"
---
# <span data-ttu-id="d9774-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="d9774-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="d9774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9774-102">SYNOPSIS</span></span>
<span data-ttu-id="d9774-103">Create artifacts from a existing image template</span><span class="sxs-lookup"><span data-stu-id="d9774-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="d9774-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9774-104">SYNTAX</span></span>

### <span data-ttu-id="d9774-105">Futtatás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9774-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d9774-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9774-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9774-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9774-107">DESCRIPTION</span></span>
<span data-ttu-id="d9774-108">Create artifacts from a existing image template</span><span class="sxs-lookup"><span data-stu-id="d9774-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="d9774-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9774-109">EXAMPLES</span></span>

### <span data-ttu-id="d9774-110">1. példa: Képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="d9774-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="d9774-111">Ez a parancs elindít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="d9774-111">This command starts an image template.</span></span>

### <span data-ttu-id="d9774-112">2. példa: Képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="d9774-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="d9774-113">Ez a parancs elindít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="d9774-113">This command starts an image template.</span></span>

## <span data-ttu-id="d9774-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9774-114">PARAMETERS</span></span>

### <span data-ttu-id="d9774-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9774-115">-AsJob</span></span>
<span data-ttu-id="d9774-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d9774-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d9774-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9774-117">-DefaultProfile</span></span>
<span data-ttu-id="d9774-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9774-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9774-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="d9774-119">-ImageTemplateName</span></span>
<span data-ttu-id="d9774-120">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="d9774-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9774-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9774-121">-InputObject</span></span>
<span data-ttu-id="d9774-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d9774-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9774-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9774-123">-NoWait</span></span>
<span data-ttu-id="d9774-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d9774-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9774-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9774-125">-PassThru</span></span>
<span data-ttu-id="d9774-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="d9774-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d9774-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9774-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9774-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d9774-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9774-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9774-129">-SubscriptionId</span></span>
<span data-ttu-id="d9774-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d9774-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9774-131">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d9774-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9774-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9774-132">-Confirm</span></span>
<span data-ttu-id="d9774-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d9774-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9774-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9774-134">-WhatIf</span></span>
<span data-ttu-id="d9774-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d9774-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9774-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9774-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9774-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9774-137">CommonParameters</span></span>
<span data-ttu-id="d9774-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9774-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9774-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9774-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9774-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9774-140">INPUTS</span></span>

### <span data-ttu-id="d9774-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="d9774-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="d9774-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9774-142">OUTPUTS</span></span>

### <span data-ttu-id="d9774-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9774-143">System.Boolean</span></span>

## <span data-ttu-id="d9774-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9774-144">NOTES</span></span>

<span data-ttu-id="d9774-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d9774-145">ALIASES</span></span>

<span data-ttu-id="d9774-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d9774-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9774-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d9774-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9774-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9774-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9774-149">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d9774-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9774-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d9774-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9774-151">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="d9774-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="d9774-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d9774-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d9774-153">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="d9774-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="d9774-154">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d9774-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9774-155">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d9774-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d9774-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9774-156">RELATED LINKS</span></span>

