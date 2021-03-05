---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012598"
---
# <span data-ttu-id="97684-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="97684-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="97684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97684-102">SYNOPSIS</span></span>
<span data-ttu-id="97684-103">List Confluent marketplace agreements in the subscription.</span><span class="sxs-lookup"><span data-stu-id="97684-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="97684-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97684-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="97684-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97684-105">DESCRIPTION</span></span>
<span data-ttu-id="97684-106">List Confluent marketplace agreements in the subscription.</span><span class="sxs-lookup"><span data-stu-id="97684-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="97684-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97684-107">EXAMPLES</span></span>

### <span data-ttu-id="97684-108">1. példa: Az előfizetéshez kötött összes összefolyásos piac-szerződés felsorolása</span><span class="sxs-lookup"><span data-stu-id="97684-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="97684-109">Ez a parancs felsorolja az előfizetéshez kötött összes, összefolyásos piactéri szerződést.</span><span class="sxs-lookup"><span data-stu-id="97684-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="97684-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97684-110">PARAMETERS</span></span>

### <span data-ttu-id="97684-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97684-111">-DefaultProfile</span></span>
<span data-ttu-id="97684-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97684-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97684-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97684-113">-SubscriptionId</span></span>
<span data-ttu-id="97684-114">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="97684-114">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="97684-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97684-115">CommonParameters</span></span>
<span data-ttu-id="97684-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97684-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97684-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97684-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97684-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97684-118">INPUTS</span></span>

## <span data-ttu-id="97684-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97684-119">OUTPUTS</span></span>

### <span data-ttu-id="97684-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="97684-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="97684-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97684-121">NOTES</span></span>

<span data-ttu-id="97684-122">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="97684-122">ALIASES</span></span>

## <span data-ttu-id="97684-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97684-123">RELATED LINKS</span></span>

