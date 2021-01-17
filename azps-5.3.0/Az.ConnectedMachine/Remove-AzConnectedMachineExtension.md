---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480652"
---
# <span data-ttu-id="6ab65-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6ab65-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="6ab65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab65-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab65-103">A bővítmény törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="6ab65-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="6ab65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ab65-104">SYNTAX</span></span>

### <span data-ttu-id="6ab65-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ab65-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab65-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab65-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ab65-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ab65-107">DESCRIPTION</span></span>
<span data-ttu-id="6ab65-108">A bővítmény törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="6ab65-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="6ab65-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ab65-109">EXAMPLES</span></span>

### <span data-ttu-id="6ab65-110">1. példa: Számítógépbővítmény eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6ab65-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="6ab65-111">Törli a bővítményt a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="6ab65-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="6ab65-112">2. példa: Bővítmény eltávolítása a folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="6ab65-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="6ab65-113">A megadott gép összes bővítményének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6ab65-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="6ab65-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ab65-114">PARAMETERS</span></span>

### <span data-ttu-id="6ab65-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab65-115">-AsJob</span></span>
<span data-ttu-id="6ab65-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="6ab65-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6ab65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab65-117">-DefaultProfile</span></span>
<span data-ttu-id="6ab65-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ab65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab65-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab65-119">-InputObject</span></span>
<span data-ttu-id="6ab65-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6ab65-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ab65-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="6ab65-121">-MachineName</span></span>
<span data-ttu-id="6ab65-122">Annak a gépnek a neve, amelyből törölni kell a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="6ab65-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="6ab65-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6ab65-123">-Name</span></span>
<span data-ttu-id="6ab65-124">A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="6ab65-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6ab65-125">-NoWait</span></span>
<span data-ttu-id="6ab65-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="6ab65-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ab65-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ab65-127">-PassThru</span></span>
<span data-ttu-id="6ab65-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="6ab65-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6ab65-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab65-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ab65-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ab65-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ab65-131">-SubscriptionId</span></span>
<span data-ttu-id="6ab65-132">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6ab65-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ab65-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ab65-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6ab65-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ab65-134">-Confirm</span></span>
<span data-ttu-id="6ab65-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6ab65-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab65-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab65-136">-WhatIf</span></span>
<span data-ttu-id="6ab65-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6ab65-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab65-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ab65-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab65-139">CommonParameters</span></span>
<span data-ttu-id="6ab65-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab65-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ab65-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab65-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab65-142">INPUTS</span></span>

### <span data-ttu-id="6ab65-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab65-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="6ab65-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ab65-144">OUTPUTS</span></span>

### <span data-ttu-id="6ab65-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ab65-145">System.Boolean</span></span>

## <span data-ttu-id="6ab65-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ab65-146">NOTES</span></span>

<span data-ttu-id="6ab65-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6ab65-147">ALIASES</span></span>

<span data-ttu-id="6ab65-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6ab65-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ab65-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6ab65-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ab65-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ab65-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ab65-151">INPUTOBJECT: <IConnectedMachineIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6ab65-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ab65-152">`[ExtensionName <String>]`: A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="6ab65-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6ab65-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ab65-154">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="6ab65-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6ab65-156">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6ab65-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6ab65-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ab65-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ab65-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ab65-158">RELATED LINKS</span></span>

