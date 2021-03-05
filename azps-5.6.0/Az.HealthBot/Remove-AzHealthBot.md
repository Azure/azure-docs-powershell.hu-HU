---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013221"
---
# <span data-ttu-id="4db84-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="4db84-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="4db84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db84-102">SYNOPSIS</span></span>
<span data-ttu-id="4db84-103">HealthBot törlése</span><span class="sxs-lookup"><span data-stu-id="4db84-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="4db84-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4db84-104">SYNTAX</span></span>

### <span data-ttu-id="4db84-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4db84-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4db84-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4db84-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4db84-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4db84-107">DESCRIPTION</span></span>
<span data-ttu-id="4db84-108">HealthBot törlése</span><span class="sxs-lookup"><span data-stu-id="4db84-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="4db84-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4db84-109">EXAMPLES</span></span>

### <span data-ttu-id="4db84-110">1. példa: A HealthBot törlése ResourceGroupName és Name szerint</span><span class="sxs-lookup"><span data-stu-id="4db84-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="4db84-111">Delete HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="4db84-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="4db84-112">2. példa: Az InputObject HealthBot törlése</span><span class="sxs-lookup"><span data-stu-id="4db84-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="4db84-113">Delete HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="4db84-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="4db84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4db84-114">PARAMETERS</span></span>

### <span data-ttu-id="4db84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4db84-115">-AsJob</span></span>
<span data-ttu-id="4db84-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="4db84-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4db84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db84-117">-DefaultProfile</span></span>
<span data-ttu-id="4db84-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4db84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db84-119">-InputObject</span></span>
<span data-ttu-id="4db84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4db84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4db84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4db84-121">-Name</span></span>
<span data-ttu-id="4db84-122">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4db84-122">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db84-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4db84-123">-NoWait</span></span>
<span data-ttu-id="4db84-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="4db84-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4db84-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4db84-125">-PassThru</span></span>
<span data-ttu-id="4db84-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="4db84-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4db84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db84-127">-ResourceGroupName</span></span>
<span data-ttu-id="4db84-128">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4db84-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db84-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4db84-129">-SubscriptionId</span></span>
<span data-ttu-id="4db84-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4db84-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db84-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db84-131">-Confirm</span></span>
<span data-ttu-id="4db84-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4db84-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db84-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db84-133">-WhatIf</span></span>
<span data-ttu-id="4db84-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4db84-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db84-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4db84-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db84-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db84-136">CommonParameters</span></span>
<span data-ttu-id="4db84-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db84-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db84-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4db84-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db84-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4db84-139">INPUTS</span></span>

### <span data-ttu-id="4db84-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="4db84-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="4db84-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4db84-141">OUTPUTS</span></span>

### <span data-ttu-id="4db84-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4db84-142">System.Boolean</span></span>

## <span data-ttu-id="4db84-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4db84-143">NOTES</span></span>

<span data-ttu-id="4db84-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4db84-144">ALIASES</span></span>

<span data-ttu-id="4db84-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4db84-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4db84-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4db84-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4db84-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4db84-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4db84-148">INPUTOBJECT: <IHealthBotIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4db84-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4db84-149">`[BotName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4db84-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="4db84-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4db84-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4db84-151">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4db84-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="4db84-152">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4db84-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4db84-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4db84-153">RELATED LINKS</span></span>

