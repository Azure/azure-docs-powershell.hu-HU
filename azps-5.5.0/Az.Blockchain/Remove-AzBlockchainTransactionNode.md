---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145171"
---
# <span data-ttu-id="8d502-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="8d502-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="8d502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d502-102">SYNOPSIS</span></span>
<span data-ttu-id="8d502-103">Törölje a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d502-103">Delete the transaction node.</span></span>

## <span data-ttu-id="8d502-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d502-104">SYNTAX</span></span>

### <span data-ttu-id="8d502-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d502-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d502-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d502-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d502-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d502-107">DESCRIPTION</span></span>
<span data-ttu-id="8d502-108">Törölje a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d502-108">Delete the transaction node.</span></span>

## <span data-ttu-id="8d502-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d502-109">EXAMPLES</span></span>

### <span data-ttu-id="8d502-110">1. példa: Tranzakciós csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8d502-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="8d502-111">Ez a parancs eltávolít egy tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d502-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="8d502-112">2. példa: Tranzakciós csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8d502-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="8d502-113">Ez a parancs eltávolít egy tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d502-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="8d502-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d502-114">PARAMETERS</span></span>

### <span data-ttu-id="8d502-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d502-115">-AsJob</span></span>
<span data-ttu-id="8d502-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="8d502-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8d502-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="8d502-117">-BlockchainMemberName</span></span>
<span data-ttu-id="8d502-118">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="8d502-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="8d502-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d502-119">-DefaultProfile</span></span>
<span data-ttu-id="8d502-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d502-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d502-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d502-121">-InputObject</span></span>
<span data-ttu-id="8d502-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8d502-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d502-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8d502-123">-Name</span></span>
<span data-ttu-id="8d502-124">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8d502-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d502-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d502-125">-NoWait</span></span>
<span data-ttu-id="8d502-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="8d502-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d502-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d502-127">-PassThru</span></span>
<span data-ttu-id="8d502-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="8d502-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8d502-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d502-129">-ResourceGroupName</span></span>
<span data-ttu-id="8d502-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d502-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8d502-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="8d502-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8d502-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d502-132">-SubscriptionId</span></span>
<span data-ttu-id="8d502-133">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="8d502-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d502-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="8d502-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d502-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d502-135">-Confirm</span></span>
<span data-ttu-id="8d502-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d502-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d502-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d502-137">-WhatIf</span></span>
<span data-ttu-id="8d502-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d502-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d502-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d502-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d502-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d502-140">CommonParameters</span></span>
<span data-ttu-id="8d502-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d502-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d502-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d502-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d502-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d502-143">INPUTS</span></span>

### <span data-ttu-id="8d502-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8d502-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8d502-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d502-145">OUTPUTS</span></span>

### <span data-ttu-id="8d502-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d502-146">System.Boolean</span></span>

## <span data-ttu-id="8d502-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d502-147">NOTES</span></span>

<span data-ttu-id="8d502-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8d502-148">ALIASES</span></span>

<span data-ttu-id="8d502-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8d502-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d502-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8d502-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d502-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d502-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d502-152">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8d502-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d502-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="8d502-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8d502-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8d502-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d502-155">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="8d502-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8d502-156">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="8d502-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8d502-157">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d502-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8d502-158">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="8d502-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8d502-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="8d502-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8d502-160">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="8d502-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8d502-161">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8d502-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8d502-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d502-162">RELATED LINKS</span></span>

