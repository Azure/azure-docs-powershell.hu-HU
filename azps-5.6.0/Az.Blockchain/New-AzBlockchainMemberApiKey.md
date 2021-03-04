---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 77b4d7800d556fc43aee4e47ebc243d006a0f484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920057"
---
# <span data-ttu-id="d8dd3-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="d8dd3-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="d8dd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dd3-103">A blockchain-tag API-kulcsait újragenerálhatja.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d8dd3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8dd3-104">SYNTAX</span></span>

### <span data-ttu-id="d8dd3-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8dd3-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8dd3-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d8dd3-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8dd3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8dd3-107">DESCRIPTION</span></span>
<span data-ttu-id="d8dd3-108">A blockchain-tag API-kulcsait újragenerálhatja.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d8dd3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="d8dd3-110">1. példa: A blockchain tag API-kulcsának újragenerálása név használatával</span><span class="sxs-lookup"><span data-stu-id="d8dd3-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d8dd3-111">Ez a parancs név, erőforráscsoport használatával újra létrehozza egy blockchain-tag Api-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="d8dd3-112">2. példa: Az Api-kulcsok újragenerálása blokklánctag esetén idenity használatával</span><span class="sxs-lookup"><span data-stu-id="d8dd3-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d8dd3-113">Ez a parancs identitás használatával újra létrehozza egy blockchain-tag API-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="d8dd3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8dd3-114">PARAMETERS</span></span>

### <span data-ttu-id="d8dd3-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d8dd3-115">-BlockchainMemberName</span></span>
<span data-ttu-id="d8dd3-116">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="d8dd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dd3-117">-DefaultProfile</span></span>
<span data-ttu-id="d8dd3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dd3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8dd3-119">-InputObject</span></span>
<span data-ttu-id="d8dd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8dd3-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d8dd3-121">-KeyName</span></span>
<span data-ttu-id="d8dd3-122">Beállítja vagy beállítja az API-kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="d8dd3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dd3-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8dd3-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d8dd3-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d8dd3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8dd3-126">-SubscriptionId</span></span>
<span data-ttu-id="d8dd3-127">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8dd3-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8dd3-129">-Érték</span><span class="sxs-lookup"><span data-stu-id="d8dd3-129">-Value</span></span>
<span data-ttu-id="d8dd3-130">Beállítja vagy beállítja az API-kulcs értékét.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="d8dd3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8dd3-131">-Confirm</span></span>
<span data-ttu-id="d8dd3-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dd3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8dd3-133">-WhatIf</span></span>
<span data-ttu-id="d8dd3-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8dd3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dd3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dd3-136">CommonParameters</span></span>
<span data-ttu-id="d8dd3-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dd3-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8dd3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dd3-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8dd3-139">INPUTS</span></span>

### <span data-ttu-id="d8dd3-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d8dd3-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d8dd3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8dd3-141">OUTPUTS</span></span>

### <span data-ttu-id="d8dd3-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="d8dd3-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="d8dd3-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8dd3-143">NOTES</span></span>

<span data-ttu-id="d8dd3-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d8dd3-144">ALIASES</span></span>

<span data-ttu-id="d8dd3-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d8dd3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8dd3-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8dd3-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8dd3-148">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d8dd3-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8dd3-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d8dd3-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d8dd3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8dd3-151">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d8dd3-152">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d8dd3-153">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8dd3-154">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8dd3-155">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d8dd3-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d8dd3-157">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="d8dd3-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d8dd3-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8dd3-158">RELATED LINKS</span></span>

