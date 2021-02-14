---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: b14ed0d682a6ba74eb557aae79a4fe151e952a73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167418"
---
# <span data-ttu-id="f5904-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f5904-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="f5904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5904-102">SYNOPSIS</span></span>
<span data-ttu-id="f5904-103">Javítás egy HealthBot-nak.</span><span class="sxs-lookup"><span data-stu-id="f5904-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="f5904-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f5904-104">SYNTAX</span></span>

### <span data-ttu-id="f5904-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5904-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5904-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f5904-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5904-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f5904-107">DESCRIPTION</span></span>
<span data-ttu-id="f5904-108">Javítás egy HealthBot-nak.</span><span class="sxs-lookup"><span data-stu-id="f5904-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="f5904-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f5904-109">EXAMPLES</span></span>

### <span data-ttu-id="f5904-110">1. példa: A HealthBot frissítése erőforráscsoportnév és név szerint</span><span class="sxs-lookup"><span data-stu-id="f5904-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="f5904-111">Update HealthBot by Resourcegroupname and Name</span><span class="sxs-lookup"><span data-stu-id="f5904-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="f5904-112">2. példa: A HealthBot frissítése inputObject szerint</span><span class="sxs-lookup"><span data-stu-id="f5904-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="f5904-113">Update HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="f5904-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="f5904-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5904-114">PARAMETERS</span></span>

### <span data-ttu-id="f5904-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5904-115">-DefaultProfile</span></span>
<span data-ttu-id="f5904-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5904-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5904-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5904-117">-InputObject</span></span>
<span data-ttu-id="f5904-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f5904-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5904-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f5904-119">-Name</span></span>
<span data-ttu-id="f5904-120">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f5904-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f5904-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5904-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5904-122">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="f5904-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f5904-123">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="f5904-123">-Sku</span></span>
<span data-ttu-id="f5904-124">A HealthBot termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="f5904-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5904-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5904-125">-SubscriptionId</span></span>
<span data-ttu-id="f5904-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5904-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f5904-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5904-127">-Tag</span></span>
<span data-ttu-id="f5904-128">A HealthBot címkéi.</span><span class="sxs-lookup"><span data-stu-id="f5904-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="f5904-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5904-129">-Confirm</span></span>
<span data-ttu-id="f5904-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f5904-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5904-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5904-131">-WhatIf</span></span>
<span data-ttu-id="f5904-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f5904-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5904-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5904-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5904-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5904-134">CommonParameters</span></span>
<span data-ttu-id="f5904-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5904-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5904-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5904-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5904-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5904-137">INPUTS</span></span>

### <span data-ttu-id="f5904-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="f5904-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f5904-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5904-139">OUTPUTS</span></span>

### <span data-ttu-id="f5904-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.iHealthBot</span><span class="sxs-lookup"><span data-stu-id="f5904-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f5904-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f5904-141">NOTES</span></span>

<span data-ttu-id="f5904-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f5904-142">ALIASES</span></span>

<span data-ttu-id="f5904-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f5904-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5904-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f5904-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5904-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5904-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5904-146">INPUTOBJECT: <IHealthBotIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f5904-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5904-147">`[BotName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f5904-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f5904-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f5904-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5904-149">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="f5904-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f5904-150">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5904-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f5904-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5904-151">RELATED LINKS</span></span>

