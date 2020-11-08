---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182754"
---
# <span data-ttu-id="8fc35-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="8fc35-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="8fc35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fc35-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc35-103">A képsablonon alapuló hosszú futási kép megszüntetése</span><span class="sxs-lookup"><span data-stu-id="8fc35-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="8fc35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fc35-104">SYNTAX</span></span>

### <span data-ttu-id="8fc35-105">Mégse (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fc35-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8fc35-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8fc35-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8fc35-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fc35-107">DESCRIPTION</span></span>
<span data-ttu-id="8fc35-108">A képsablonon alapuló hosszú futási kép megszüntetése</span><span class="sxs-lookup"><span data-stu-id="8fc35-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="8fc35-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8fc35-109">EXAMPLES</span></span>

### <span data-ttu-id="8fc35-110">Példa 1: a Képsablon létrehozásának leállítása</span><span class="sxs-lookup"><span data-stu-id="8fc35-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="8fc35-111">Ez a parancs a Képsablon létrehozását nem állítja be.</span><span class="sxs-lookup"><span data-stu-id="8fc35-111">This command stops image template creation.</span></span>

### <span data-ttu-id="8fc35-112">2. példa: a Képsablon létrehozásának leállítása</span><span class="sxs-lookup"><span data-stu-id="8fc35-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="8fc35-113">Ez a parancs a Képsablon létrehozását nem állítja be.</span><span class="sxs-lookup"><span data-stu-id="8fc35-113">This command stops image template creation.</span></span>

## <span data-ttu-id="8fc35-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fc35-114">PARAMETERS</span></span>

### <span data-ttu-id="8fc35-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fc35-115">-AsJob</span></span>
<span data-ttu-id="8fc35-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="8fc35-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8fc35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc35-117">-DefaultProfile</span></span>
<span data-ttu-id="8fc35-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fc35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc35-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="8fc35-119">-ImageTemplateName</span></span>
<span data-ttu-id="8fc35-120">A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="8fc35-120">The name of the image Template</span></span>

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

### <span data-ttu-id="8fc35-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fc35-121">-InputObject</span></span>
<span data-ttu-id="8fc35-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fc35-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8fc35-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="8fc35-123">-NoWait</span></span>
<span data-ttu-id="8fc35-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="8fc35-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8fc35-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fc35-125">-PassThru</span></span>
<span data-ttu-id="8fc35-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="8fc35-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8fc35-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc35-127">-ResourceGroupName</span></span>
<span data-ttu-id="8fc35-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fc35-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8fc35-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fc35-129">-SubscriptionId</span></span>
<span data-ttu-id="8fc35-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8fc35-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8fc35-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8fc35-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8fc35-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8fc35-132">-Confirm</span></span>
<span data-ttu-id="8fc35-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8fc35-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc35-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc35-134">-WhatIf</span></span>
<span data-ttu-id="8fc35-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8fc35-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc35-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fc35-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc35-137">CommonParameters</span></span>
<span data-ttu-id="8fc35-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fc35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc35-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fc35-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc35-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc35-140">INPUTS</span></span>

### <span data-ttu-id="8fc35-141">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="8fc35-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="8fc35-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc35-142">OUTPUTS</span></span>

### <span data-ttu-id="8fc35-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8fc35-143">System.Boolean</span></span>

## <span data-ttu-id="8fc35-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fc35-144">NOTES</span></span>

<span data-ttu-id="8fc35-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8fc35-145">ALIASES</span></span>

<span data-ttu-id="8fc35-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="8fc35-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8fc35-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8fc35-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8fc35-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8fc35-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8fc35-149">INPUTOBJECT <IImageBuilderIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8fc35-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8fc35-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8fc35-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8fc35-151">`[ImageTemplateName <String>]`: A Képsablon neve</span><span class="sxs-lookup"><span data-stu-id="8fc35-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="8fc35-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fc35-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8fc35-153">`[RunOutputName <String>]`: A futtatott kimenet neve</span><span class="sxs-lookup"><span data-stu-id="8fc35-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="8fc35-154">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8fc35-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8fc35-155">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8fc35-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8fc35-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fc35-156">RELATED LINKS</span></span>

