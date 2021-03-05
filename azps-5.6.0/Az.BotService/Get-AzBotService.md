---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 305e65e95b876e3093f4a14590e8b2e111e44aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009317"
---
# <span data-ttu-id="678c7-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="678c7-101">Get-AzBotService</span></span>

## <span data-ttu-id="678c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678c7-102">SYNOPSIS</span></span>
<span data-ttu-id="678c7-103">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="678c7-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="678c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="678c7-104">SYNTAX</span></span>

### <span data-ttu-id="678c7-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="678c7-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="678c7-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="678c7-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="678c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="678c7-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="678c7-108">Lista</span><span class="sxs-lookup"><span data-stu-id="678c7-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="678c7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="678c7-109">DESCRIPTION</span></span>
<span data-ttu-id="678c7-110">A paraméterek által megadott BotService értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="678c7-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="678c7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="678c7-111">EXAMPLES</span></span>

### <span data-ttu-id="678c7-112">1. példa: Az összes BotServices lekérte</span><span class="sxs-lookup"><span data-stu-id="678c7-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="678c7-113">Az összes botszolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="678c7-113">Get all BotServices</span></span>

### <span data-ttu-id="678c7-114">2. példa: A BotService lekérte a ResourceGroupName és a Name nevet</span><span class="sxs-lookup"><span data-stu-id="678c7-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="678c7-115">A BotService lekérte: ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="678c7-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="678c7-116">3. példa: Az összes BotServices lekérte a ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="678c7-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="678c7-117">Az összes BotServices lekérte a ResourceGroupName szerint</span><span class="sxs-lookup"><span data-stu-id="678c7-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="678c7-118">4. példa: A BotService lekérte az inputObject által</span><span class="sxs-lookup"><span data-stu-id="678c7-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="678c7-119">A BotService lekérte: inputObject</span><span class="sxs-lookup"><span data-stu-id="678c7-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="678c7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="678c7-120">PARAMETERS</span></span>

### <span data-ttu-id="678c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678c7-121">-DefaultProfile</span></span>
<span data-ttu-id="678c7-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="678c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678c7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678c7-123">-InputObject</span></span>
<span data-ttu-id="678c7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="678c7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678c7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="678c7-125">-Name</span></span>
<span data-ttu-id="678c7-126">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="678c7-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="678c7-128">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="678c7-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="678c7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="678c7-129">-SubscriptionId</span></span>
<span data-ttu-id="678c7-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="678c7-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="678c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678c7-131">CommonParameters</span></span>
<span data-ttu-id="678c7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678c7-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="678c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678c7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="678c7-134">INPUTS</span></span>

### <span data-ttu-id="678c7-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="678c7-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="678c7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="678c7-136">OUTPUTS</span></span>

### <span data-ttu-id="678c7-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="678c7-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="678c7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="678c7-138">NOTES</span></span>

<span data-ttu-id="678c7-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="678c7-139">ALIASES</span></span>

<span data-ttu-id="678c7-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="678c7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="678c7-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="678c7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="678c7-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="678c7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="678c7-143">INPUTOBJECT: <IBotServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="678c7-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="678c7-144">`[ChannelName <ChannelName?>]`: A Csatorna típusú erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="678c7-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="678c7-145">`[ConnectionName <String>]`: A robotszolgáltatás kapcsolatbeállítási erőforrásának neve</span><span class="sxs-lookup"><span data-stu-id="678c7-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="678c7-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="678c7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="678c7-147">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="678c7-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="678c7-148">`[ResourceName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="678c7-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="678c7-149">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="678c7-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="678c7-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="678c7-150">RELATED LINKS</span></span>

