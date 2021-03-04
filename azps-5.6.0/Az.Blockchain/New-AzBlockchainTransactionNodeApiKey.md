---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920050"
---
# <span data-ttu-id="8ba3f-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="8ba3f-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="8ba3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba3f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba3f-103">A blockchain tag API-kulcsait újragenerálhatja.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="8ba3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ba3f-104">SYNTAX</span></span>

### <span data-ttu-id="8ba3f-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ba3f-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ba3f-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8ba3f-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ba3f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ba3f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba3f-108">A blockchain tag API-kulcsait újragenerálhatja.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="8ba3f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ba3f-109">EXAMPLES</span></span>

### <span data-ttu-id="8ba3f-110">1. példa: A tranzakciós csomópont Api-kulcsait névvel újragenerálhatja.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="8ba3f-111">Ez a parancs Api-kulcsokat hoz létre egy tranzakciós csomóponthoz név, erőforráscsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="8ba3f-112">2. példa: Az Api-kulcsok újragenerálása tranzakciós csomóponthoz</span><span class="sxs-lookup"><span data-stu-id="8ba3f-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="8ba3f-113">Ez a parancs api-kulcsokat hoz létre egy tranzakciós csomóponthoz idenity használatával.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="8ba3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ba3f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba3f-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="8ba3f-115">-BlockchainMemberName</span></span>
<span data-ttu-id="8ba3f-116">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba3f-117">-DefaultProfile</span></span>
<span data-ttu-id="8ba3f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba3f-119">-InputObject</span></span>
<span data-ttu-id="8ba3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8ba3f-121">-KeyName</span></span>
<span data-ttu-id="8ba3f-122">Beállítja vagy beállítja az API-kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ba3f-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8ba3f-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ba3f-126">-SubscriptionId</span></span>
<span data-ttu-id="8ba3f-127">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8ba3f-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="8ba3f-129">-TransactionNodeName</span></span>
<span data-ttu-id="8ba3f-130">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-131">-Érték</span><span class="sxs-lookup"><span data-stu-id="8ba3f-131">-Value</span></span>
<span data-ttu-id="8ba3f-132">Beállítja vagy beállítja az API-kulcs értékét.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-132">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ba3f-133">-Confirm</span></span>
<span data-ttu-id="8ba3f-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba3f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba3f-135">-WhatIf</span></span>
<span data-ttu-id="8ba3f-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba3f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba3f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba3f-138">CommonParameters</span></span>
<span data-ttu-id="8ba3f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba3f-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ba3f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba3f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ba3f-141">INPUTS</span></span>

### <span data-ttu-id="8ba3f-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8ba3f-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8ba3f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba3f-143">OUTPUTS</span></span>

### <span data-ttu-id="8ba3f-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="8ba3f-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="8ba3f-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ba3f-145">NOTES</span></span>

<span data-ttu-id="8ba3f-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8ba3f-146">ALIASES</span></span>

<span data-ttu-id="8ba3f-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8ba3f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ba3f-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ba3f-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ba3f-150">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8ba3f-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ba3f-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8ba3f-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8ba3f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ba3f-153">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8ba3f-154">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8ba3f-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8ba3f-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8ba3f-157">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8ba3f-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8ba3f-159">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="8ba3f-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8ba3f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ba3f-160">RELATED LINKS</span></span>

