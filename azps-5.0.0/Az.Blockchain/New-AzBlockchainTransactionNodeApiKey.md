---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187652"
---
# <span data-ttu-id="f08ca-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="f08ca-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="f08ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f08ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f08ca-103">Az blockchain-tag API-kulcsainak újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="f08ca-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="f08ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f08ca-104">SYNTAX</span></span>

### <span data-ttu-id="f08ca-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f08ca-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f08ca-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f08ca-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f08ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f08ca-107">DESCRIPTION</span></span>
<span data-ttu-id="f08ca-108">Az blockchain-tag API-kulcsainak újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="f08ca-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="f08ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f08ca-109">EXAMPLES</span></span>

### <span data-ttu-id="f08ca-110">1. példa: a Transaction Node API-kulcsának újragenerálása név használatával.</span><span class="sxs-lookup"><span data-stu-id="f08ca-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="f08ca-111">Ez a parancs API-kulcsokat hoz létre a tranzakciós csomópontokhoz név, erőforráscsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="f08ca-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="f08ca-112">2. példa: a tranzakciós csomópont API-kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f08ca-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="f08ca-113">Ez a parancs API-kulcsokat hoz létre a Transaction Node-hoz a idenity használatával.</span><span class="sxs-lookup"><span data-stu-id="f08ca-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="f08ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f08ca-114">PARAMETERS</span></span>

### <span data-ttu-id="f08ca-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="f08ca-115">-BlockchainMemberName</span></span>
<span data-ttu-id="f08ca-116">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="f08ca-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="f08ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08ca-117">-DefaultProfile</span></span>
<span data-ttu-id="f08ca-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f08ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f08ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f08ca-119">-InputObject</span></span>
<span data-ttu-id="f08ca-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f08ca-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f08ca-121">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f08ca-121">-KeyName</span></span>
<span data-ttu-id="f08ca-122">Az API-kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="f08ca-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="f08ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f08ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="f08ca-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f08ca-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f08ca-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f08ca-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f08ca-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f08ca-126">-SubscriptionId</span></span>
<span data-ttu-id="f08ca-127">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f08ca-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f08ca-128">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="f08ca-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f08ca-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="f08ca-129">-TransactionNodeName</span></span>
<span data-ttu-id="f08ca-130">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="f08ca-130">Transaction node name.</span></span>

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

### <span data-ttu-id="f08ca-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="f08ca-131">-Value</span></span>
<span data-ttu-id="f08ca-132">Az API-kulcs értékét kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="f08ca-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="f08ca-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f08ca-133">-Confirm</span></span>
<span data-ttu-id="f08ca-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f08ca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f08ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f08ca-135">-WhatIf</span></span>
<span data-ttu-id="f08ca-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f08ca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f08ca-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f08ca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f08ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08ca-138">CommonParameters</span></span>
<span data-ttu-id="f08ca-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f08ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08ca-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f08ca-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08ca-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f08ca-141">INPUTS</span></span>

### <span data-ttu-id="f08ca-142">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="f08ca-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="f08ca-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f08ca-143">OUTPUTS</span></span>

### <span data-ttu-id="f08ca-144">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="f08ca-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="f08ca-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f08ca-145">NOTES</span></span>

<span data-ttu-id="f08ca-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f08ca-146">ALIASES</span></span>

<span data-ttu-id="f08ca-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f08ca-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f08ca-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f08ca-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f08ca-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f08ca-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f08ca-150">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f08ca-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f08ca-151">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="f08ca-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="f08ca-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f08ca-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f08ca-153">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="f08ca-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="f08ca-154">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="f08ca-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="f08ca-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f08ca-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f08ca-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f08ca-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f08ca-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="f08ca-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="f08ca-158">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="f08ca-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="f08ca-159">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="f08ca-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="f08ca-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f08ca-160">RELATED LINKS</span></span>

