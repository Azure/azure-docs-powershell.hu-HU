---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007286"
---
# <span data-ttu-id="7cbac-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="7cbac-101">Update-AzBotService</span></span>

## <span data-ttu-id="7cbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cbac-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbac-103">Robotszolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="7cbac-103">Updates a Bot Service</span></span>

## <span data-ttu-id="7cbac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cbac-104">SYNTAX</span></span>

### <span data-ttu-id="7cbac-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cbac-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cbac-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7cbac-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cbac-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cbac-107">DESCRIPTION</span></span>
<span data-ttu-id="7cbac-108">Robotszolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="7cbac-108">Updates a Bot Service</span></span>

## <span data-ttu-id="7cbac-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cbac-109">EXAMPLES</span></span>

### <span data-ttu-id="7cbac-110">1. példa: A robot frissítése név és ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="7cbac-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="7cbac-111">A robot frissítése név és ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="7cbac-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="7cbac-112">2. példa: A robot frissítése inputObject szerint</span><span class="sxs-lookup"><span data-stu-id="7cbac-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="7cbac-113">A robot frissítése InputObject szerint</span><span class="sxs-lookup"><span data-stu-id="7cbac-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="7cbac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cbac-114">PARAMETERS</span></span>

### <span data-ttu-id="7cbac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbac-115">-DefaultProfile</span></span>
<span data-ttu-id="7cbac-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cbac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cbac-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7cbac-117">-Description</span></span>
<span data-ttu-id="7cbac-118">A robot leírása</span><span class="sxs-lookup"><span data-stu-id="7cbac-118">The description of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="7cbac-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="7cbac-120">Az Application Insights kulcs</span><span class="sxs-lookup"><span data-stu-id="7cbac-120">The Application Insights key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7cbac-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="7cbac-122">Az Application Insights API-kulcs</span><span class="sxs-lookup"><span data-stu-id="7cbac-122">The Application Insights Api Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="7cbac-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="7cbac-124">Az Application Insights appazonosítója</span><span class="sxs-lookup"><span data-stu-id="7cbac-124">The Application Insights App Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7cbac-125">-DisplayName</span></span>
<span data-ttu-id="7cbac-126">A robot neve</span><span class="sxs-lookup"><span data-stu-id="7cbac-126">The Name of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7cbac-127">-Endpoint</span></span>
<span data-ttu-id="7cbac-128">A robot végpontja</span><span class="sxs-lookup"><span data-stu-id="7cbac-128">The bot's endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="7cbac-129">-Etag</span></span>
<span data-ttu-id="7cbac-130">Entity Tag</span><span class="sxs-lookup"><span data-stu-id="7cbac-130">Entity Tag</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="7cbac-131">-IconUrl</span></span>
<span data-ttu-id="7cbac-132">A robot ikon URL-címe</span><span class="sxs-lookup"><span data-stu-id="7cbac-132">The Icon Url of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cbac-133">-InputObject</span></span>
<span data-ttu-id="7cbac-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7cbac-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="7cbac-135">-Kind</span></span>
<span data-ttu-id="7cbac-136">Kötelező.</span><span class="sxs-lookup"><span data-stu-id="7cbac-136">Required.</span></span>
<span data-ttu-id="7cbac-137">Beállítja vagy beállítja az erőforrás fajtáját.</span><span class="sxs-lookup"><span data-stu-id="7cbac-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-138">-Location</span><span class="sxs-lookup"><span data-stu-id="7cbac-138">-Location</span></span>
<span data-ttu-id="7cbac-139">Az erőforrás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbac-139">Specifies the location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="7cbac-140">-LuisAppId</span></span>
<span data-ttu-id="7cbac-141">A LUIS-appazonosítók gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="7cbac-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-142">–LuisKey</span><span class="sxs-lookup"><span data-stu-id="7cbac-142">-LuisKey</span></span>
<span data-ttu-id="7cbac-143">A LUIS-kulcs</span><span class="sxs-lookup"><span data-stu-id="7cbac-143">The LUIS Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="7cbac-144">-MsaAppId</span></span>
<span data-ttu-id="7cbac-145">A robot Microsoft-appazonosítója</span><span class="sxs-lookup"><span data-stu-id="7cbac-145">Microsoft App Id for the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-146">-Name</span><span class="sxs-lookup"><span data-stu-id="7cbac-146">-Name</span></span>
<span data-ttu-id="7cbac-147">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7cbac-147">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbac-148">-ResourceGroupName</span></span>
<span data-ttu-id="7cbac-149">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7cbac-149">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7cbac-150">-SkuName</span></span>
<span data-ttu-id="7cbac-151">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="7cbac-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cbac-152">-SubscriptionId</span></span>
<span data-ttu-id="7cbac-153">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cbac-153">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cbac-154">-Tag</span></span>
<span data-ttu-id="7cbac-155">Kulcs-érték párként definiált erőforráscímkéket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7cbac-155">Contains resource tags defined as key/value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbac-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cbac-156">-Confirm</span></span>
<span data-ttu-id="7cbac-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7cbac-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbac-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbac-158">-WhatIf</span></span>
<span data-ttu-id="7cbac-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7cbac-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbac-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cbac-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbac-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbac-161">CommonParameters</span></span>
<span data-ttu-id="7cbac-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbac-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbac-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cbac-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbac-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cbac-164">INPUTS</span></span>

### <span data-ttu-id="7cbac-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7cbac-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="7cbac-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbac-166">OUTPUTS</span></span>

### <span data-ttu-id="7cbac-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="7cbac-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="7cbac-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cbac-168">NOTES</span></span>

<span data-ttu-id="7cbac-169">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7cbac-169">ALIASES</span></span>

<span data-ttu-id="7cbac-170">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7cbac-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cbac-171">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7cbac-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cbac-172">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cbac-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cbac-173">INPUTOBJECT: <IBotServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7cbac-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cbac-174">`[ChannelName <ChannelName?>]`: A Csatorna típusú erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7cbac-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="7cbac-175">`[ConnectionName <String>]`: A robotszolgáltatás kapcsolatbeállítási erőforrásának neve</span><span class="sxs-lookup"><span data-stu-id="7cbac-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="7cbac-176">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7cbac-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cbac-177">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7cbac-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="7cbac-178">`[ResourceName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7cbac-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="7cbac-179">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cbac-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7cbac-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cbac-180">RELATED LINKS</span></span>

