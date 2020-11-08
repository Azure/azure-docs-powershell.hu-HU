---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187373"
---
# <span data-ttu-id="6d239-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="6d239-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="6d239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d239-102">SYNOPSIS</span></span>
<span data-ttu-id="6d239-103">Leletek létrehozása meglévő képsablonból</span><span class="sxs-lookup"><span data-stu-id="6d239-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="6d239-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d239-104">SYNTAX</span></span>

### <span data-ttu-id="6d239-105">Run (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d239-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6d239-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d239-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d239-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d239-107">DESCRIPTION</span></span>
<span data-ttu-id="6d239-108">Leletek létrehozása meglévő képsablonból</span><span class="sxs-lookup"><span data-stu-id="6d239-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="6d239-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6d239-109">EXAMPLES</span></span>

### <span data-ttu-id="6d239-110">1. példa: Képsablon indítása</span><span class="sxs-lookup"><span data-stu-id="6d239-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="6d239-111">Ezzel a paranccsal elindíthatja a képsablont.</span><span class="sxs-lookup"><span data-stu-id="6d239-111">This command starts an image template.</span></span>

### <span data-ttu-id="6d239-112">2. példa: Képsablon indítása</span><span class="sxs-lookup"><span data-stu-id="6d239-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="6d239-113">Ezzel a paranccsal elindíthatja a képsablont.</span><span class="sxs-lookup"><span data-stu-id="6d239-113">This command starts an image template.</span></span>

## <span data-ttu-id="6d239-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d239-114">PARAMETERS</span></span>

### <span data-ttu-id="6d239-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d239-115">-AsJob</span></span>
<span data-ttu-id="6d239-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="6d239-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d239-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d239-117">-DefaultProfile</span></span>
<span data-ttu-id="6d239-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d239-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d239-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="6d239-119">-ImageTemplateName</span></span>
<span data-ttu-id="6d239-120">A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6d239-120">The name of the image Template</span></span>

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

### <span data-ttu-id="6d239-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d239-121">-InputObject</span></span>
<span data-ttu-id="6d239-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d239-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d239-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="6d239-123">-NoWait</span></span>
<span data-ttu-id="6d239-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="6d239-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d239-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d239-125">-PassThru</span></span>
<span data-ttu-id="6d239-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="6d239-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d239-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d239-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d239-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d239-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d239-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d239-129">-SubscriptionId</span></span>
<span data-ttu-id="6d239-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6d239-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d239-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6d239-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d239-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d239-132">-Confirm</span></span>
<span data-ttu-id="6d239-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d239-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d239-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d239-134">-WhatIf</span></span>
<span data-ttu-id="6d239-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d239-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d239-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d239-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d239-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d239-137">CommonParameters</span></span>
<span data-ttu-id="6d239-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d239-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d239-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d239-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d239-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d239-140">INPUTS</span></span>

### <span data-ttu-id="6d239-141">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="6d239-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="6d239-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d239-142">OUTPUTS</span></span>

### <span data-ttu-id="6d239-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d239-143">System.Boolean</span></span>

## <span data-ttu-id="6d239-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d239-144">NOTES</span></span>

<span data-ttu-id="6d239-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6d239-145">ALIASES</span></span>

<span data-ttu-id="6d239-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6d239-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d239-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6d239-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d239-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6d239-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d239-149">INPUTOBJECT <IImageBuilderIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6d239-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d239-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6d239-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d239-151">`[ImageTemplateName <String>]`: A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="6d239-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="6d239-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d239-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6d239-153">`[RunOutputName <String>]`: A futtatott kimenet neve</span><span class="sxs-lookup"><span data-stu-id="6d239-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="6d239-154">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6d239-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6d239-155">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6d239-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d239-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d239-156">RELATED LINKS</span></span>

