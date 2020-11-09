---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301583"
---
# <span data-ttu-id="96e4f-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="96e4f-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="96e4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="96e4f-103">A blockchain-tagok API-kulcsainak újragenerálása</span><span class="sxs-lookup"><span data-stu-id="96e4f-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="96e4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96e4f-104">SYNTAX</span></span>

### <span data-ttu-id="96e4f-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96e4f-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96e4f-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="96e4f-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96e4f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="96e4f-108">A blockchain-tagok API-kulcsainak újragenerálása</span><span class="sxs-lookup"><span data-stu-id="96e4f-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="96e4f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="96e4f-110">Példa 1: az API-kulcsok újragenerálása a blockchain-tagok nevével</span><span class="sxs-lookup"><span data-stu-id="96e4f-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="96e4f-111">Ez a parancs a blockchain-tagok API-kulcsait a név, az erőforráscsoport segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="96e4f-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="96e4f-112">2. példa: az API-kulcsok újragenerálása a blockchain-tagok idenity használatával</span><span class="sxs-lookup"><span data-stu-id="96e4f-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="96e4f-113">Ez a parancs a blockchain-tagok API-kulcsait az identitás segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="96e4f-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="96e4f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96e4f-114">PARAMETERS</span></span>

### <span data-ttu-id="96e4f-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="96e4f-115">-BlockchainMemberName</span></span>
<span data-ttu-id="96e4f-116">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="96e4f-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="96e4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e4f-117">-DefaultProfile</span></span>
<span data-ttu-id="96e4f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96e4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96e4f-119">-InputObject</span></span>
<span data-ttu-id="96e4f-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96e4f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96e4f-121">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="96e4f-121">-KeyName</span></span>
<span data-ttu-id="96e4f-122">Az API-kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="96e4f-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="96e4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="96e4f-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96e4f-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="96e4f-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="96e4f-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="96e4f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96e4f-126">-SubscriptionId</span></span>
<span data-ttu-id="96e4f-127">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="96e4f-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96e4f-128">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="96e4f-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96e4f-129">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="96e4f-129">-Value</span></span>
<span data-ttu-id="96e4f-130">Az API-kulcs értékét kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="96e4f-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="96e4f-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96e4f-131">-Confirm</span></span>
<span data-ttu-id="96e4f-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96e4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e4f-133">-WhatIf</span></span>
<span data-ttu-id="96e4f-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96e4f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e4f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96e4f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e4f-136">CommonParameters</span></span>
<span data-ttu-id="96e4f-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96e4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e4f-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96e4f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e4f-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e4f-139">INPUTS</span></span>

### <span data-ttu-id="96e4f-140">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="96e4f-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="96e4f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e4f-141">OUTPUTS</span></span>

### <span data-ttu-id="96e4f-142">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="96e4f-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="96e4f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96e4f-143">NOTES</span></span>

<span data-ttu-id="96e4f-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="96e4f-144">ALIASES</span></span>

<span data-ttu-id="96e4f-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="96e4f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96e4f-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96e4f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96e4f-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="96e4f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96e4f-148">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="96e4f-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96e4f-149">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="96e4f-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="96e4f-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="96e4f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96e4f-151">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="96e4f-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="96e4f-152">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="96e4f-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="96e4f-153">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96e4f-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="96e4f-154">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="96e4f-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="96e4f-155">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="96e4f-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="96e4f-156">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="96e4f-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="96e4f-157">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="96e4f-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="96e4f-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96e4f-158">RELATED LINKS</span></span>

