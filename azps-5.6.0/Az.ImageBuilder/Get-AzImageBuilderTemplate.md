---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: 82730525f6330336be72e922881d743345515926
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013062"
---
# <span data-ttu-id="6c7fd-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="6c7fd-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="6c7fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7fd-103">Virtuális gép képsablonjának információi</span><span class="sxs-lookup"><span data-stu-id="6c7fd-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="6c7fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c7fd-104">SYNTAX</span></span>

### <span data-ttu-id="6c7fd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c7fd-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c7fd-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="6c7fd-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c7fd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6c7fd-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c7fd-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="6c7fd-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6c7fd-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c7fd-109">DESCRIPTION</span></span>
<span data-ttu-id="6c7fd-110">Virtuális gép képsablonjának információi</span><span class="sxs-lookup"><span data-stu-id="6c7fd-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="6c7fd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c7fd-111">EXAMPLES</span></span>

### <span data-ttu-id="6c7fd-112">1. példa: Az előfizetés összes sablonjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="6c7fd-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6c7fd-113">Ez a parancs felsorolja az előfizetés alatt található összes sablont.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="6c7fd-114">2. példa: Az erőforráscsoport összes sablonjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="6c7fd-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6c7fd-115">Ez a parancs felsorolja az erőforráscsoportok alatt található összes sablont.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="6c7fd-116">3. példa: Sablon létrehozása erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="6c7fd-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6c7fd-117">Ez a parancs egy erőforráscsoport alatt kap egy sablont.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="6c7fd-118">4. példa: Sablon lekérte egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="6c7fd-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="6c7fd-119">Ez a parancs egy erőforráscsoport alatt kap egy sablont.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="6c7fd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c7fd-120">PARAMETERS</span></span>

### <span data-ttu-id="6c7fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7fd-121">-DefaultProfile</span></span>
<span data-ttu-id="6c7fd-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c7fd-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="6c7fd-123">-ImageTemplateName</span></span>
<span data-ttu-id="6c7fd-124">A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6c7fd-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7fd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c7fd-125">-InputObject</span></span>
<span data-ttu-id="6c7fd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c7fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c7fd-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c7fd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c7fd-129">-SubscriptionId</span></span>
<span data-ttu-id="6c7fd-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6c7fd-131">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6c7fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7fd-132">CommonParameters</span></span>
<span data-ttu-id="6c7fd-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7fd-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c7fd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7fd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c7fd-135">INPUTS</span></span>

### <span data-ttu-id="6c7fd-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="6c7fd-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="6c7fd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c7fd-137">OUTPUTS</span></span>

### <span data-ttu-id="6c7fd-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="6c7fd-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="6c7fd-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c7fd-139">NOTES</span></span>

<span data-ttu-id="6c7fd-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6c7fd-140">ALIASES</span></span>

<span data-ttu-id="6c7fd-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6c7fd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c7fd-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c7fd-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c7fd-144">INPUTOBJECT: <IImageBuilderIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6c7fd-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c7fd-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6c7fd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c7fd-146">`[ImageTemplateName <String>]`: A képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6c7fd-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="6c7fd-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6c7fd-148">`[RunOutputName <String>]`: A futtatás kimenetének neve</span><span class="sxs-lookup"><span data-stu-id="6c7fd-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="6c7fd-149">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6c7fd-150">Az előfizetés azonosítója minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6c7fd-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6c7fd-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c7fd-151">RELATED LINKS</span></span>

