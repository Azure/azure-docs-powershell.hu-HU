---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: 486490a3b88025fb97b8790df202c944c05d888e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925153"
---
# <span data-ttu-id="6b0ac-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="6b0ac-101">Remove-AzBotService</span></span>

## <span data-ttu-id="6b0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0ac-103">Robotszolgáltatás törlése az erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="6b0ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b0ac-104">SYNTAX</span></span>

### <span data-ttu-id="6b0ac-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b0ac-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b0ac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b0ac-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b0ac-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b0ac-107">DESCRIPTION</span></span>
<span data-ttu-id="6b0ac-108">Robotszolgáltatás törlése az erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="6b0ac-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b0ac-109">EXAMPLES</span></span>

### <span data-ttu-id="6b0ac-110">1. példa: A BotService By Name és az ResourceGroupName törlése</span><span class="sxs-lookup"><span data-stu-id="6b0ac-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="6b0ac-111">A BotService By Name és az ResourceGroupName törlése</span><span class="sxs-lookup"><span data-stu-id="6b0ac-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="6b0ac-112">2. példa: A BotService By InputObject törlése</span><span class="sxs-lookup"><span data-stu-id="6b0ac-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="6b0ac-113">A BotService By InputObject törlése</span><span class="sxs-lookup"><span data-stu-id="6b0ac-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="6b0ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b0ac-114">PARAMETERS</span></span>

### <span data-ttu-id="6b0ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0ac-115">-DefaultProfile</span></span>
<span data-ttu-id="6b0ac-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b0ac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b0ac-117">-InputObject</span></span>
<span data-ttu-id="6b0ac-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0ac-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6b0ac-119">-Name</span></span>
<span data-ttu-id="6b0ac-120">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="6b0ac-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b0ac-121">-PassThru</span></span>
<span data-ttu-id="6b0ac-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="6b0ac-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b0ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b0ac-124">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="6b0ac-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b0ac-125">-SubscriptionId</span></span>
<span data-ttu-id="6b0ac-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6b0ac-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b0ac-127">-Confirm</span></span>
<span data-ttu-id="6b0ac-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b0ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b0ac-129">-WhatIf</span></span>
<span data-ttu-id="6b0ac-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b0ac-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b0ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0ac-132">CommonParameters</span></span>
<span data-ttu-id="6b0ac-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0ac-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b0ac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0ac-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0ac-135">INPUTS</span></span>

### <span data-ttu-id="6b0ac-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6b0ac-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="6b0ac-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b0ac-137">OUTPUTS</span></span>

### <span data-ttu-id="6b0ac-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b0ac-138">System.Boolean</span></span>

## <span data-ttu-id="6b0ac-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b0ac-139">NOTES</span></span>

<span data-ttu-id="6b0ac-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6b0ac-140">ALIASES</span></span>

<span data-ttu-id="6b0ac-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6b0ac-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b0ac-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b0ac-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b0ac-144">INPUTOBJECT: <IBotServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6b0ac-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b0ac-145">`[ChannelName <ChannelName?>]`: A Csatorna típusú erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="6b0ac-146">`[ConnectionName <String>]`: A robotszolgáltatás kapcsolatbeállítási erőforrásának neve</span><span class="sxs-lookup"><span data-stu-id="6b0ac-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="6b0ac-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6b0ac-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b0ac-148">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="6b0ac-149">`[ResourceName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="6b0ac-150">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b0ac-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6b0ac-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b0ac-151">RELATED LINKS</span></span>

