---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 54678dd00a0edae4af3a90c84e1c930c1c032e84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928681"
---
# <span data-ttu-id="cd2c1-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="cd2c1-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="cd2c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2c1-103">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="cd2c1-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="cd2c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd2c1-104">SYNTAX</span></span>

### <span data-ttu-id="cd2c1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd2c1-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd2c1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd2c1-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd2c1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd2c1-107">DESCRIPTION</span></span>
<span data-ttu-id="cd2c1-108">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="cd2c1-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="cd2c1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd2c1-109">EXAMPLES</span></span>

### <span data-ttu-id="cd2c1-110">1. példa: Blockchain-tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cd2c1-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="cd2c1-111">Ez a parancs eltávolítja a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="cd2c1-112">2. példa: Blockchain-tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cd2c1-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="cd2c1-113">Ez a parancs eltávolítja a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="cd2c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd2c1-114">PARAMETERS</span></span>

### <span data-ttu-id="cd2c1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd2c1-115">-AsJob</span></span>
<span data-ttu-id="cd2c1-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="cd2c1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cd2c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2c1-117">-DefaultProfile</span></span>
<span data-ttu-id="cd2c1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd2c1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd2c1-119">-InputObject</span></span>
<span data-ttu-id="cd2c1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2c1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd2c1-121">-Name</span></span>
<span data-ttu-id="cd2c1-122">Blockchain member name</span><span class="sxs-lookup"><span data-stu-id="cd2c1-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2c1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd2c1-123">-NoWait</span></span>
<span data-ttu-id="cd2c1-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="cd2c1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd2c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd2c1-125">-PassThru</span></span>
<span data-ttu-id="cd2c1-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="cd2c1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd2c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd2c1-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cd2c1-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cd2c1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd2c1-130">-SubscriptionId</span></span>
<span data-ttu-id="cd2c1-131">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd2c1-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd2c1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd2c1-133">-Confirm</span></span>
<span data-ttu-id="cd2c1-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2c1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2c1-135">-WhatIf</span></span>
<span data-ttu-id="cd2c1-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd2c1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2c1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2c1-138">CommonParameters</span></span>
<span data-ttu-id="cd2c1-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2c1-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd2c1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2c1-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd2c1-141">INPUTS</span></span>

### <span data-ttu-id="cd2c1-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="cd2c1-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="cd2c1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd2c1-143">OUTPUTS</span></span>

### <span data-ttu-id="cd2c1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd2c1-144">System.Boolean</span></span>

## <span data-ttu-id="cd2c1-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd2c1-145">NOTES</span></span>

<span data-ttu-id="cd2c1-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cd2c1-146">ALIASES</span></span>

<span data-ttu-id="cd2c1-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="cd2c1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd2c1-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd2c1-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd2c1-150">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cd2c1-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd2c1-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="cd2c1-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cd2c1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd2c1-153">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="cd2c1-154">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="cd2c1-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cd2c1-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cd2c1-157">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="cd2c1-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="cd2c1-159">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="cd2c1-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="cd2c1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd2c1-160">RELATED LINKS</span></span>

