---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013078"
---
# <span data-ttu-id="e6244-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="e6244-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="e6244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6244-102">SYNOPSIS</span></span>
<span data-ttu-id="e6244-103">A megadott futtatás kimenete a megadott képsablon-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="e6244-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="e6244-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6244-104">SYNTAX</span></span>

### <span data-ttu-id="e6244-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6244-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6244-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="e6244-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6244-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6244-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6244-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6244-108">DESCRIPTION</span></span>
<span data-ttu-id="e6244-109">A megadott futtatás kimenete a megadott képsablon-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="e6244-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="e6244-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6244-110">EXAMPLES</span></span>

### <span data-ttu-id="e6244-111">1. példa: Az összes futtatás eredményének felsorolása egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="e6244-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="e6244-112">Ez a parancs felsorolja az összes futtatás eredményét egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="e6244-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="e6244-113">2. példa: Futtatás eredményének lekérte egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="e6244-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="e6244-114">Ez a parancs futtatás eredményt kap egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="e6244-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="e6244-115">3. példa: Futtatás eredményének lekérte egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="e6244-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="e6244-116">Ez a parancs futtatás eredményt kap egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="e6244-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="e6244-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6244-117">PARAMETERS</span></span>

### <span data-ttu-id="e6244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6244-118">-DefaultProfile</span></span>
<span data-ttu-id="e6244-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6244-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6244-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="e6244-120">-ImageTemplateName</span></span>
<span data-ttu-id="e6244-121">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="e6244-121">The name of the image Template</span></span>

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

### <span data-ttu-id="e6244-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6244-122">-InputObject</span></span>
<span data-ttu-id="e6244-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e6244-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e6244-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6244-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6244-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6244-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6244-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="e6244-126">-RunOutputName</span></span>
<span data-ttu-id="e6244-127">A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="e6244-127">The name of the run output</span></span>

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

### <span data-ttu-id="e6244-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6244-128">-SubscriptionId</span></span>
<span data-ttu-id="e6244-129">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e6244-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e6244-130">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6244-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e6244-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6244-131">CommonParameters</span></span>
<span data-ttu-id="e6244-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6244-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6244-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6244-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6244-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6244-134">INPUTS</span></span>

### <span data-ttu-id="e6244-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="e6244-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="e6244-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6244-136">OUTPUTS</span></span>

### <span data-ttu-id="e6244-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="e6244-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="e6244-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6244-138">NOTES</span></span>

<span data-ttu-id="e6244-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e6244-139">ALIASES</span></span>

<span data-ttu-id="e6244-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e6244-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6244-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e6244-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6244-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6244-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6244-143">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e6244-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6244-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e6244-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6244-145">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="e6244-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="e6244-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6244-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e6244-147">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="e6244-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="e6244-148">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e6244-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e6244-149">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6244-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e6244-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6244-150">RELATED LINKS</span></span>

