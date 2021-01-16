---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339030"
---
# <span data-ttu-id="03c0a-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="03c0a-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="03c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="03c0a-103">A hosszú ideig futó kép build megszakítása a képsablon alapján</span><span class="sxs-lookup"><span data-stu-id="03c0a-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="03c0a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03c0a-104">SYNTAX</span></span>

### <span data-ttu-id="03c0a-105">Mégse (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03c0a-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03c0a-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03c0a-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03c0a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="03c0a-108">A hosszú ideig futó kép build megszakítása a képsablon alapján</span><span class="sxs-lookup"><span data-stu-id="03c0a-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="03c0a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03c0a-109">EXAMPLES</span></span>

### <span data-ttu-id="03c0a-110">1. példa: A képsablon létrehozásának vége</span><span class="sxs-lookup"><span data-stu-id="03c0a-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="03c0a-111">Ez a parancs leállítja a képsablon létrehozását.</span><span class="sxs-lookup"><span data-stu-id="03c0a-111">This command stops image template creation.</span></span>

### <span data-ttu-id="03c0a-112">2. példa: A képsablon létrehozásának vége</span><span class="sxs-lookup"><span data-stu-id="03c0a-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="03c0a-113">Ez a parancs leállítja a képsablon létrehozását.</span><span class="sxs-lookup"><span data-stu-id="03c0a-113">This command stops image template creation.</span></span>

## <span data-ttu-id="03c0a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c0a-114">PARAMETERS</span></span>

### <span data-ttu-id="03c0a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c0a-115">-AsJob</span></span>
<span data-ttu-id="03c0a-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="03c0a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="03c0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c0a-117">-DefaultProfile</span></span>
<span data-ttu-id="03c0a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03c0a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c0a-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="03c0a-119">-ImageTemplateName</span></span>
<span data-ttu-id="03c0a-120">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="03c0a-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c0a-121">-InputObject</span></span>
<span data-ttu-id="03c0a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="03c0a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03c0a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03c0a-123">-NoWait</span></span>
<span data-ttu-id="03c0a-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="03c0a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03c0a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c0a-125">-PassThru</span></span>
<span data-ttu-id="03c0a-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="03c0a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03c0a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c0a-127">-ResourceGroupName</span></span>
<span data-ttu-id="03c0a-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03c0a-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c0a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03c0a-129">-SubscriptionId</span></span>
<span data-ttu-id="03c0a-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="03c0a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03c0a-131">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="03c0a-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c0a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c0a-132">-Confirm</span></span>
<span data-ttu-id="03c0a-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03c0a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c0a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c0a-134">-WhatIf</span></span>
<span data-ttu-id="03c0a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03c0a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c0a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03c0a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c0a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c0a-137">CommonParameters</span></span>
<span data-ttu-id="03c0a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c0a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c0a-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c0a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c0a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03c0a-140">INPUTS</span></span>

### <span data-ttu-id="03c0a-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="03c0a-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="03c0a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03c0a-142">OUTPUTS</span></span>

### <span data-ttu-id="03c0a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03c0a-143">System.Boolean</span></span>

## <span data-ttu-id="03c0a-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03c0a-144">NOTES</span></span>

<span data-ttu-id="03c0a-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="03c0a-145">ALIASES</span></span>

<span data-ttu-id="03c0a-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="03c0a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03c0a-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="03c0a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03c0a-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03c0a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03c0a-149">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="03c0a-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03c0a-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="03c0a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03c0a-151">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="03c0a-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="03c0a-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03c0a-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="03c0a-153">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="03c0a-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="03c0a-154">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="03c0a-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="03c0a-155">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="03c0a-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="03c0a-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03c0a-156">RELATED LINKS</span></span>

