---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386817"
---
# <span data-ttu-id="23cb7-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="23cb7-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="23cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="23cb7-103">A megadott futtatás kimenete a megadott képsablon-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="23cb7-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="23cb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23cb7-104">SYNTAX</span></span>

### <span data-ttu-id="23cb7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23cb7-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23cb7-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="23cb7-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23cb7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23cb7-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23cb7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23cb7-108">DESCRIPTION</span></span>
<span data-ttu-id="23cb7-109">A megadott futtatás kimenete a megadott képsablon-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="23cb7-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="23cb7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23cb7-110">EXAMPLES</span></span>

### <span data-ttu-id="23cb7-111">1. példa: Az összes futtatás eredményének felsorolása egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="23cb7-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="23cb7-112">Ez a parancs felsorolja az összes futtatás eredményét egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="23cb7-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="23cb7-113">2. példa: Futtatás eredményének lekérte egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="23cb7-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="23cb7-114">Ez a parancs futtatás eredményt kap egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="23cb7-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="23cb7-115">3. példa: Futtatás eredményének lekérte egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="23cb7-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="23cb7-116">Ez a parancs futtatás eredményt kap egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="23cb7-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="23cb7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23cb7-117">PARAMETERS</span></span>

### <span data-ttu-id="23cb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cb7-118">-DefaultProfile</span></span>
<span data-ttu-id="23cb7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23cb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cb7-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="23cb7-120">-ImageTemplateName</span></span>
<span data-ttu-id="23cb7-121">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="23cb7-121">The name of the image Template</span></span>

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

### <span data-ttu-id="23cb7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23cb7-122">-InputObject</span></span>
<span data-ttu-id="23cb7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="23cb7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="23cb7-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23cb7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="23cb7-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="23cb7-126">-RunOutputName</span></span>
<span data-ttu-id="23cb7-127">A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="23cb7-127">The name of the run output</span></span>

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

### <span data-ttu-id="23cb7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23cb7-128">-SubscriptionId</span></span>
<span data-ttu-id="23cb7-129">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="23cb7-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="23cb7-130">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="23cb7-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cb7-131">CommonParameters</span></span>
<span data-ttu-id="23cb7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cb7-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23cb7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cb7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23cb7-134">INPUTS</span></span>

### <span data-ttu-id="23cb7-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="23cb7-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="23cb7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23cb7-136">OUTPUTS</span></span>

### <span data-ttu-id="23cb7-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="23cb7-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="23cb7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23cb7-138">NOTES</span></span>

<span data-ttu-id="23cb7-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="23cb7-139">ALIASES</span></span>

<span data-ttu-id="23cb7-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="23cb7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23cb7-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="23cb7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23cb7-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23cb7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23cb7-143">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="23cb7-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23cb7-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="23cb7-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23cb7-145">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="23cb7-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="23cb7-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23cb7-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="23cb7-147">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="23cb7-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="23cb7-148">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="23cb7-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="23cb7-149">Az előfizetés-azonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="23cb7-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="23cb7-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23cb7-150">RELATED LINKS</span></span>

