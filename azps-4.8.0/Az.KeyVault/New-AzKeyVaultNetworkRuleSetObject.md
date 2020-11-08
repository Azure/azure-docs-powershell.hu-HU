---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181729"
---
# <span data-ttu-id="729d8-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="729d8-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="729d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="729d8-102">SYNOPSIS</span></span>
<span data-ttu-id="729d8-103">Hozzon létre egy olyan objektumot, amely a hálózati szabály beállításait jelképezi.</span><span class="sxs-lookup"><span data-stu-id="729d8-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="729d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="729d8-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="729d8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="729d8-105">DESCRIPTION</span></span>
<span data-ttu-id="729d8-106">Hozzon létre egy olyan objektumot, amely a boltozat létrehozásakor használatos hálózati szabályok beállításait jelképezi.</span><span class="sxs-lookup"><span data-stu-id="729d8-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="729d8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="729d8-107">EXAMPLES</span></span>

### <span data-ttu-id="729d8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="729d8-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="729d8-109">Új tároló létrehozása és a hálózati szabályok megadása, amelyek lehetővé teszik a megadott IP-cím elérését az $myNetworkResId által azonosított virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="729d8-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="729d8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="729d8-110">PARAMETERS</span></span>

### <span data-ttu-id="729d8-111">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="729d8-111">-Bypass</span></span>
<span data-ttu-id="729d8-112">A hálózati szabály megkerülését adja meg.</span><span class="sxs-lookup"><span data-stu-id="729d8-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="729d8-113">-DefaultAction</span></span>
<span data-ttu-id="729d8-114">A hálózati szabály alapértelmezett működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="729d8-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729d8-115">-DefaultProfile</span></span>
<span data-ttu-id="729d8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="729d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="729d8-117">-IpAddressRange</span></span>
<span data-ttu-id="729d8-118">A hálózati szabály engedélyezett hálózati IP-címének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="729d8-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="729d8-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="729d8-120">A hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="729d8-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729d8-121">CommonParameters</span></span>
<span data-ttu-id="729d8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="729d8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729d8-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="729d8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729d8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="729d8-124">INPUTS</span></span>

### <span data-ttu-id="729d8-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="729d8-125">None</span></span>

## <span data-ttu-id="729d8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="729d8-126">OUTPUTS</span></span>

### <span data-ttu-id="729d8-127">Microsoft. Azure. Command. PSKeyVaultNetworkRuleSet. models.</span><span class="sxs-lookup"><span data-stu-id="729d8-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="729d8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="729d8-128">NOTES</span></span>

## <span data-ttu-id="729d8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="729d8-129">RELATED LINKS</span></span>
