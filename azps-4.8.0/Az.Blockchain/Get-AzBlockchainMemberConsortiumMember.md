---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024195"
---
# <span data-ttu-id="252a7-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="252a7-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="252a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="252a7-102">SYNOPSIS</span></span>
<span data-ttu-id="252a7-103">A blockchain-tagok konzorcium-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="252a7-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="252a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="252a7-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="252a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="252a7-105">DESCRIPTION</span></span>
<span data-ttu-id="252a7-106">A blockchain-tagok konzorcium-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="252a7-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="252a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="252a7-107">EXAMPLES</span></span>

### <span data-ttu-id="252a7-108">1. példa: a konzorcium tagjainak listája a blockchain tagjai számára.</span><span class="sxs-lookup"><span data-stu-id="252a7-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="252a7-109">Ez a parancs felsorolja a blockchain tagok konzorcium-tagjait.</span><span class="sxs-lookup"><span data-stu-id="252a7-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="252a7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="252a7-110">PARAMETERS</span></span>

### <span data-ttu-id="252a7-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="252a7-111">-BlockchainMemberName</span></span>
<span data-ttu-id="252a7-112">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="252a7-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="252a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252a7-113">-DefaultProfile</span></span>
<span data-ttu-id="252a7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="252a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="252a7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252a7-115">-ResourceGroupName</span></span>
<span data-ttu-id="252a7-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="252a7-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="252a7-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="252a7-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="252a7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="252a7-118">-SubscriptionId</span></span>
<span data-ttu-id="252a7-119">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="252a7-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="252a7-120">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="252a7-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="252a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252a7-121">CommonParameters</span></span>
<span data-ttu-id="252a7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="252a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252a7-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="252a7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252a7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="252a7-124">INPUTS</span></span>

## <span data-ttu-id="252a7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="252a7-125">OUTPUTS</span></span>

### <span data-ttu-id="252a7-126">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="252a7-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="252a7-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="252a7-127">NOTES</span></span>

<span data-ttu-id="252a7-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="252a7-128">ALIASES</span></span>

## <span data-ttu-id="252a7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="252a7-129">RELATED LINKS</span></span>

