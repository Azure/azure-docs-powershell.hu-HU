---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161570"
---
# <span data-ttu-id="89558-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="89558-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="89558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89558-102">SYNOPSIS</span></span>
<span data-ttu-id="89558-103">Create artifacts from a existing image template</span><span class="sxs-lookup"><span data-stu-id="89558-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="89558-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89558-104">SYNTAX</span></span>

### <span data-ttu-id="89558-105">Futtatás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89558-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="89558-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89558-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89558-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89558-107">DESCRIPTION</span></span>
<span data-ttu-id="89558-108">Create artifacts from a existing image template</span><span class="sxs-lookup"><span data-stu-id="89558-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="89558-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89558-109">EXAMPLES</span></span>

### <span data-ttu-id="89558-110">1. példa: Képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="89558-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="89558-111">Ez a parancs elindít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="89558-111">This command starts an image template.</span></span>

### <span data-ttu-id="89558-112">2. példa: Képsablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="89558-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="89558-113">Ez a parancs elindít egy képsablont.</span><span class="sxs-lookup"><span data-stu-id="89558-113">This command starts an image template.</span></span>

## <span data-ttu-id="89558-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89558-114">PARAMETERS</span></span>

### <span data-ttu-id="89558-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89558-115">-AsJob</span></span>
<span data-ttu-id="89558-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="89558-116">Run the command as a job</span></span>

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

### <span data-ttu-id="89558-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89558-117">-DefaultProfile</span></span>
<span data-ttu-id="89558-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89558-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89558-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="89558-119">-ImageTemplateName</span></span>
<span data-ttu-id="89558-120">A kép sablonjának neve</span><span class="sxs-lookup"><span data-stu-id="89558-120">The name of the image Template</span></span>

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

### <span data-ttu-id="89558-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89558-121">-InputObject</span></span>
<span data-ttu-id="89558-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="89558-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89558-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89558-123">-NoWait</span></span>
<span data-ttu-id="89558-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="89558-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89558-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89558-125">-PassThru</span></span>
<span data-ttu-id="89558-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="89558-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="89558-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89558-127">-ResourceGroupName</span></span>
<span data-ttu-id="89558-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89558-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="89558-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89558-129">-SubscriptionId</span></span>
<span data-ttu-id="89558-130">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="89558-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="89558-131">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="89558-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="89558-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89558-132">-Confirm</span></span>
<span data-ttu-id="89558-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89558-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89558-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89558-134">-WhatIf</span></span>
<span data-ttu-id="89558-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89558-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89558-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89558-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89558-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89558-137">CommonParameters</span></span>
<span data-ttu-id="89558-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89558-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89558-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89558-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89558-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89558-140">INPUTS</span></span>

### <span data-ttu-id="89558-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="89558-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="89558-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89558-142">OUTPUTS</span></span>

### <span data-ttu-id="89558-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89558-143">System.Boolean</span></span>

## <span data-ttu-id="89558-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89558-144">NOTES</span></span>

<span data-ttu-id="89558-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="89558-145">ALIASES</span></span>

<span data-ttu-id="89558-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="89558-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89558-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="89558-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89558-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89558-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89558-149">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="89558-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89558-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="89558-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89558-151">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="89558-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="89558-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89558-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="89558-153">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="89558-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="89558-154">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="89558-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="89558-155">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="89558-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="89558-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89558-156">RELATED LINKS</span></span>

