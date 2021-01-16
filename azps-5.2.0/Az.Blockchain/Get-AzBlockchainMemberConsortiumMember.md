---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341910"
---
# <span data-ttu-id="443fe-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="443fe-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="443fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="443fe-102">SYNOPSIS</span></span>
<span data-ttu-id="443fe-103">Egy blockchain-tagnak a consortium tagjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="443fe-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="443fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="443fe-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="443fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="443fe-105">DESCRIPTION</span></span>
<span data-ttu-id="443fe-106">Egy blockchain-tagnak a consortium tagjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="443fe-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="443fe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="443fe-107">EXAMPLES</span></span>

### <span data-ttu-id="443fe-108">1. példa: Egy blockchain-tag consortium-tagjainak felsorolása.</span><span class="sxs-lookup"><span data-stu-id="443fe-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="443fe-109">Ez a parancs felsorolja egy blockchain-tag consortium tagjait.</span><span class="sxs-lookup"><span data-stu-id="443fe-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="443fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="443fe-110">PARAMETERS</span></span>

### <span data-ttu-id="443fe-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="443fe-111">-BlockchainMemberName</span></span>
<span data-ttu-id="443fe-112">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="443fe-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="443fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443fe-113">-DefaultProfile</span></span>
<span data-ttu-id="443fe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="443fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="443fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="443fe-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="443fe-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="443fe-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="443fe-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="443fe-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="443fe-118">-SubscriptionId</span></span>
<span data-ttu-id="443fe-119">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="443fe-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="443fe-120">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="443fe-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="443fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443fe-121">CommonParameters</span></span>
<span data-ttu-id="443fe-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="443fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443fe-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="443fe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443fe-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="443fe-124">INPUTS</span></span>

## <span data-ttu-id="443fe-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="443fe-125">OUTPUTS</span></span>

### <span data-ttu-id="443fe-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="443fe-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="443fe-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="443fe-127">NOTES</span></span>

<span data-ttu-id="443fe-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="443fe-128">ALIASES</span></span>

## <span data-ttu-id="443fe-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="443fe-129">RELATED LINKS</span></span>

