---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325636"
---
# <span data-ttu-id="b03c4-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="b03c4-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="b03c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b03c4-103">Hibrid gépi identitás eltávolítása az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b03c4-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="b03c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b03c4-104">SYNTAX</span></span>

### <span data-ttu-id="b03c4-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b03c4-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b03c4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b03c4-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b03c4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b03c4-107">DESCRIPTION</span></span>
<span data-ttu-id="b03c4-108">Hibrid gépi identitás eltávolítása az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b03c4-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="b03c4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b03c4-109">EXAMPLES</span></span>

### <span data-ttu-id="b03c4-110">1. példa: Csatlakoztatott számítógép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b03c4-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="b03c4-111">A csatlakoztatott számítógép törlése.</span><span class="sxs-lookup"><span data-stu-id="b03c4-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="b03c4-112">2. példa: Csatlakoztatott gépek eltávolítása a folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="b03c4-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="b03c4-113">Eltávolítja az erőforráscsoport összes `contoso-connected-machines` gépét.</span><span class="sxs-lookup"><span data-stu-id="b03c4-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="b03c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b03c4-114">PARAMETERS</span></span>

### <span data-ttu-id="b03c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03c4-115">-DefaultProfile</span></span>
<span data-ttu-id="b03c4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b03c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03c4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03c4-117">-InputObject</span></span>
<span data-ttu-id="b03c4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b03c4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b03c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b03c4-119">-Name</span></span>
<span data-ttu-id="b03c4-120">A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="b03c4-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="b03c4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b03c4-121">-PassThru</span></span>
<span data-ttu-id="b03c4-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="b03c4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b03c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="b03c4-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b03c4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b03c4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b03c4-125">-SubscriptionId</span></span>
<span data-ttu-id="b03c4-126">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b03c4-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b03c4-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b03c4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b03c4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b03c4-128">-Confirm</span></span>
<span data-ttu-id="b03c4-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b03c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03c4-130">-WhatIf</span></span>
<span data-ttu-id="b03c4-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b03c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03c4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b03c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03c4-133">CommonParameters</span></span>
<span data-ttu-id="b03c4-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03c4-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b03c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03c4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b03c4-136">INPUTS</span></span>

### <span data-ttu-id="b03c4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="b03c4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="b03c4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b03c4-138">OUTPUTS</span></span>

### <span data-ttu-id="b03c4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b03c4-139">System.Boolean</span></span>

## <span data-ttu-id="b03c4-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b03c4-140">NOTES</span></span>

<span data-ttu-id="b03c4-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b03c4-141">ALIASES</span></span>

<span data-ttu-id="b03c4-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b03c4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b03c4-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b03c4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b03c4-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b03c4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b03c4-145">INPUTOBJECT: <IConnectedMachineIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b03c4-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b03c4-146">`[ExtensionName <String>]`: A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="b03c4-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="b03c4-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b03c4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b03c4-148">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="b03c4-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="b03c4-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b03c4-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b03c4-150">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b03c4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b03c4-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b03c4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b03c4-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b03c4-152">RELATED LINKS</span></span>

