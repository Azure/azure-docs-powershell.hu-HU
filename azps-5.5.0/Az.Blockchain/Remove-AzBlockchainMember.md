---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205143"
---
# <span data-ttu-id="288de-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="288de-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="288de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="288de-102">SYNOPSIS</span></span>
<span data-ttu-id="288de-103">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="288de-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="288de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="288de-104">SYNTAX</span></span>

### <span data-ttu-id="288de-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="288de-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="288de-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="288de-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="288de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="288de-107">DESCRIPTION</span></span>
<span data-ttu-id="288de-108">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="288de-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="288de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="288de-109">EXAMPLES</span></span>

### <span data-ttu-id="288de-110">1. példa: Blockchain-tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="288de-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="288de-111">Ez a parancs eltávolítja a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="288de-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="288de-112">2. példa: Blockchain-tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="288de-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="288de-113">Ez a parancs eltávolítja a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="288de-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="288de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="288de-114">PARAMETERS</span></span>

### <span data-ttu-id="288de-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="288de-115">-AsJob</span></span>
<span data-ttu-id="288de-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="288de-116">Run the command as a job</span></span>

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

### <span data-ttu-id="288de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288de-117">-DefaultProfile</span></span>
<span data-ttu-id="288de-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="288de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="288de-119">-InputObject</span></span>
<span data-ttu-id="288de-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="288de-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="288de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="288de-121">-Name</span></span>
<span data-ttu-id="288de-122">Blockchain member name</span><span class="sxs-lookup"><span data-stu-id="288de-122">Blockchain member name</span></span>

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

### <span data-ttu-id="288de-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="288de-123">-NoWait</span></span>
<span data-ttu-id="288de-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="288de-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="288de-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="288de-125">-PassThru</span></span>
<span data-ttu-id="288de-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="288de-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="288de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288de-127">-ResourceGroupName</span></span>
<span data-ttu-id="288de-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="288de-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="288de-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="288de-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="288de-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="288de-130">-SubscriptionId</span></span>
<span data-ttu-id="288de-131">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="288de-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="288de-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="288de-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="288de-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="288de-133">-Confirm</span></span>
<span data-ttu-id="288de-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="288de-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288de-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288de-135">-WhatIf</span></span>
<span data-ttu-id="288de-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="288de-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288de-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="288de-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288de-138">CommonParameters</span></span>
<span data-ttu-id="288de-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288de-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="288de-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288de-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="288de-141">INPUTS</span></span>

### <span data-ttu-id="288de-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="288de-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="288de-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="288de-143">OUTPUTS</span></span>

### <span data-ttu-id="288de-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="288de-144">System.Boolean</span></span>

## <span data-ttu-id="288de-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="288de-145">NOTES</span></span>

<span data-ttu-id="288de-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="288de-146">ALIASES</span></span>

<span data-ttu-id="288de-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="288de-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="288de-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="288de-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="288de-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="288de-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="288de-150">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="288de-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="288de-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="288de-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="288de-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="288de-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="288de-153">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="288de-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="288de-154">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="288de-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="288de-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="288de-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="288de-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="288de-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="288de-157">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="288de-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="288de-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="288de-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="288de-159">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="288de-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="288de-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="288de-160">RELATED LINKS</span></span>

