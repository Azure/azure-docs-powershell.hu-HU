---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209911"
---
# <span data-ttu-id="2cea2-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="2cea2-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="2cea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cea2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cea2-103">Hibrid gépi identitás eltávolítása az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2cea2-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="2cea2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cea2-104">SYNTAX</span></span>

### <span data-ttu-id="2cea2-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2cea2-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cea2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2cea2-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2cea2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cea2-107">DESCRIPTION</span></span>
<span data-ttu-id="2cea2-108">Hibrid gépi identitás eltávolítása az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2cea2-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="2cea2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cea2-109">EXAMPLES</span></span>

### <span data-ttu-id="2cea2-110">1. példa: Csatlakoztatott számítógép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2cea2-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="2cea2-111">Törli a csatlakoztatott gépet.</span><span class="sxs-lookup"><span data-stu-id="2cea2-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="2cea2-112">2. példa: Csatlakoztatott gépek eltávolítása a folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="2cea2-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="2cea2-113">Eltávolítja az erőforráscsoport összes `contoso-connected-machines` gépét.</span><span class="sxs-lookup"><span data-stu-id="2cea2-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="2cea2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cea2-114">PARAMETERS</span></span>

### <span data-ttu-id="2cea2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cea2-115">-DefaultProfile</span></span>
<span data-ttu-id="2cea2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cea2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cea2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cea2-117">-InputObject</span></span>
<span data-ttu-id="2cea2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2cea2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cea2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2cea2-119">-Name</span></span>
<span data-ttu-id="2cea2-120">A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="2cea2-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="2cea2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cea2-121">-PassThru</span></span>
<span data-ttu-id="2cea2-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="2cea2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2cea2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cea2-123">-ResourceGroupName</span></span>
<span data-ttu-id="2cea2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2cea2-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2cea2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2cea2-125">-SubscriptionId</span></span>
<span data-ttu-id="2cea2-126">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2cea2-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2cea2-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2cea2-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2cea2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cea2-128">-Confirm</span></span>
<span data-ttu-id="2cea2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2cea2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cea2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cea2-130">-WhatIf</span></span>
<span data-ttu-id="2cea2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2cea2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cea2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2cea2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cea2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cea2-133">CommonParameters</span></span>
<span data-ttu-id="2cea2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cea2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cea2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cea2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cea2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cea2-136">INPUTS</span></span>

### <span data-ttu-id="2cea2-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="2cea2-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="2cea2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cea2-138">OUTPUTS</span></span>

### <span data-ttu-id="2cea2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2cea2-139">System.Boolean</span></span>

## <span data-ttu-id="2cea2-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cea2-140">NOTES</span></span>

<span data-ttu-id="2cea2-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2cea2-141">ALIASES</span></span>

<span data-ttu-id="2cea2-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2cea2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2cea2-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2cea2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2cea2-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2cea2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2cea2-145">INPUTOBJECT: <IConnectedMachineIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2cea2-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2cea2-146">`[ExtensionName <String>]`: A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="2cea2-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="2cea2-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2cea2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2cea2-148">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="2cea2-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="2cea2-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2cea2-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2cea2-150">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2cea2-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2cea2-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2cea2-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2cea2-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cea2-152">RELATED LINKS</span></span>

