---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296285"
---
# <span data-ttu-id="1fe42-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="1fe42-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="1fe42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fe42-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe42-103">A megadott sablonfájl-erőforrás meghatározott futtatási kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="1fe42-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="1fe42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fe42-104">SYNTAX</span></span>

### <span data-ttu-id="1fe42-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fe42-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1fe42-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1fe42-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1fe42-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fe42-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe42-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fe42-108">DESCRIPTION</span></span>
<span data-ttu-id="1fe42-109">A megadott sablonfájl-erőforrás meghatározott futtatási kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="1fe42-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="1fe42-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1fe42-110">EXAMPLES</span></span>

### <span data-ttu-id="1fe42-111">Példa 1: a minden futási eredmény listázása egy sablon alatt</span><span class="sxs-lookup"><span data-stu-id="1fe42-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1fe42-112">Ez a parancs felsorolja a minden futási eredményt egy sablon alatt.</span><span class="sxs-lookup"><span data-stu-id="1fe42-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="1fe42-113">2. példa: futtatási eredmény megszerzése sablon alatt</span><span class="sxs-lookup"><span data-stu-id="1fe42-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1fe42-114">Ez a parancs a futási eredményt egy sablon alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="1fe42-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="1fe42-115">3. példa: futtatási eredmény megszerzése sablon alatt</span><span class="sxs-lookup"><span data-stu-id="1fe42-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1fe42-116">Ez a parancs a futási eredményt egy sablon alatt kapja.</span><span class="sxs-lookup"><span data-stu-id="1fe42-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="1fe42-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fe42-117">PARAMETERS</span></span>

### <span data-ttu-id="1fe42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe42-118">-DefaultProfile</span></span>
<span data-ttu-id="1fe42-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fe42-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe42-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="1fe42-120">-ImageTemplateName</span></span>
<span data-ttu-id="1fe42-121">A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="1fe42-121">The name of the image Template</span></span>

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

### <span data-ttu-id="1fe42-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe42-122">-InputObject</span></span>
<span data-ttu-id="1fe42-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1fe42-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fe42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe42-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fe42-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe42-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fe42-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="1fe42-126">-RunOutputName</span></span>
<span data-ttu-id="1fe42-127">A futtatási kimenet neve</span><span class="sxs-lookup"><span data-stu-id="1fe42-127">The name of the run output</span></span>

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

### <span data-ttu-id="1fe42-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fe42-128">-SubscriptionId</span></span>
<span data-ttu-id="1fe42-129">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1fe42-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fe42-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1fe42-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1fe42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe42-131">CommonParameters</span></span>
<span data-ttu-id="1fe42-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fe42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe42-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1fe42-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe42-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe42-134">INPUTS</span></span>

### <span data-ttu-id="1fe42-135">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="1fe42-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="1fe42-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe42-136">OUTPUTS</span></span>

### <span data-ttu-id="1fe42-137">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="1fe42-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="1fe42-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fe42-138">NOTES</span></span>

<span data-ttu-id="1fe42-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1fe42-139">ALIASES</span></span>

<span data-ttu-id="1fe42-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1fe42-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fe42-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1fe42-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fe42-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1fe42-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fe42-143">INPUTOBJECT <IImageBuilderIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1fe42-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fe42-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1fe42-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fe42-145">`[ImageTemplateName <String>]`: A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="1fe42-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="1fe42-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fe42-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1fe42-147">`[RunOutputName <String>]`: A futtatott kimenet neve</span><span class="sxs-lookup"><span data-stu-id="1fe42-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="1fe42-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1fe42-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fe42-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1fe42-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1fe42-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fe42-150">RELATED LINKS</span></span>

