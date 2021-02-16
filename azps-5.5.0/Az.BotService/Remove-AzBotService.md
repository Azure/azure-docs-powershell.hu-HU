---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162426"
---
# <span data-ttu-id="a4c59-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="a4c59-101">Remove-AzBotService</span></span>

## <span data-ttu-id="a4c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c59-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c59-103">Robotszolgáltatás törlése az erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="a4c59-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="a4c59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4c59-104">SYNTAX</span></span>

### <span data-ttu-id="a4c59-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4c59-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4c59-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4c59-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4c59-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4c59-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c59-108">Robotszolgáltatás törlése az erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="a4c59-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="a4c59-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4c59-109">EXAMPLES</span></span>

### <span data-ttu-id="a4c59-110">1. példa: A BotService By Name és az ResourceGroupName törlése</span><span class="sxs-lookup"><span data-stu-id="a4c59-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="a4c59-111">A BotService By Name és az ResourceGroupName törlése</span><span class="sxs-lookup"><span data-stu-id="a4c59-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="a4c59-112">2. példa: A BotService By InputObject törlése</span><span class="sxs-lookup"><span data-stu-id="a4c59-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="a4c59-113">A BotService By InputObject törlése</span><span class="sxs-lookup"><span data-stu-id="a4c59-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="a4c59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c59-114">PARAMETERS</span></span>

### <span data-ttu-id="a4c59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c59-115">-DefaultProfile</span></span>
<span data-ttu-id="a4c59-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4c59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c59-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c59-117">-InputObject</span></span>
<span data-ttu-id="a4c59-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a4c59-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4c59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4c59-119">-Name</span></span>
<span data-ttu-id="a4c59-120">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a4c59-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="a4c59-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4c59-121">-PassThru</span></span>
<span data-ttu-id="a4c59-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a4c59-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4c59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c59-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4c59-124">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a4c59-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="a4c59-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4c59-125">-SubscriptionId</span></span>
<span data-ttu-id="a4c59-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4c59-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a4c59-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4c59-127">-Confirm</span></span>
<span data-ttu-id="a4c59-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a4c59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c59-129">-WhatIf</span></span>
<span data-ttu-id="a4c59-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a4c59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c59-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4c59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c59-132">CommonParameters</span></span>
<span data-ttu-id="a4c59-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c59-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4c59-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c59-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4c59-135">INPUTS</span></span>

### <span data-ttu-id="a4c59-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a4c59-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="a4c59-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c59-137">OUTPUTS</span></span>

### <span data-ttu-id="a4c59-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4c59-138">System.Boolean</span></span>

## <span data-ttu-id="a4c59-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4c59-139">NOTES</span></span>

<span data-ttu-id="a4c59-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a4c59-140">ALIASES</span></span>

<span data-ttu-id="a4c59-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a4c59-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4c59-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a4c59-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4c59-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4c59-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4c59-144">INPUTOBJECT: <IBotServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c59-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4c59-145">`[ChannelName <ChannelName?>]`: A Csatorna típusú erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a4c59-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="a4c59-146">`[ConnectionName <String>]`: A robotszolgáltatás kapcsolatbeállítási erőforrásának neve</span><span class="sxs-lookup"><span data-stu-id="a4c59-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="a4c59-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a4c59-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4c59-148">`[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a4c59-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="a4c59-149">`[ResourceName <String>]`: A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a4c59-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="a4c59-150">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4c59-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a4c59-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4c59-151">RELATED LINKS</span></span>

