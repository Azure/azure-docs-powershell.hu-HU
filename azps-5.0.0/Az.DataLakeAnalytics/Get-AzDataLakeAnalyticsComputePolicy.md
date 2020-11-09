---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298115"
---
# <span data-ttu-id="05afa-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="05afa-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="05afa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05afa-102">SYNOPSIS</span></span>
<span data-ttu-id="05afa-103">Adattó-elemzést kap a házirend vagy a számítási házirendek listájának kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="05afa-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="05afa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05afa-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05afa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05afa-105">DESCRIPTION</span></span>
<span data-ttu-id="05afa-106">A **Get-AzDataLakeAnalyticsComputePolicy** megkapja a megadott Azure Data Lake Analytics számítási házirendjét vagy a házirendek listáját.</span><span class="sxs-lookup"><span data-stu-id="05afa-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="05afa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05afa-107">EXAMPLES</span></span>

### <span data-ttu-id="05afa-108">Példa 1: meghatározott számítási házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="05afa-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="05afa-109">Ez a parancs a megadott számítási házirendet a "myPolicy" névvel a "contosoadla" fiókban kapja.</span><span class="sxs-lookup"><span data-stu-id="05afa-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="05afa-110">2. példa: a fiókban található összes számítási házirend listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="05afa-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="05afa-111">Ez a parancs a "contosoadla" fiókban a számítási házirendek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="05afa-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="05afa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05afa-112">PARAMETERS</span></span>

### <span data-ttu-id="05afa-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="05afa-113">-Account</span></span>
<span data-ttu-id="05afa-114">Annak a fióknak a neve, amelyből kiszámítja a számítási házirendet vagy a házirendeket.</span><span class="sxs-lookup"><span data-stu-id="05afa-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05afa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05afa-115">-DefaultProfile</span></span>
<span data-ttu-id="05afa-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="05afa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05afa-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05afa-117">-Name</span></span>
<span data-ttu-id="05afa-118">A beszerzéshez használandó számítási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="05afa-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05afa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05afa-119">-ResourceGroupName</span></span>
<span data-ttu-id="05afa-120">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="05afa-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="05afa-121">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="05afa-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05afa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05afa-122">CommonParameters</span></span>
<span data-ttu-id="05afa-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05afa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05afa-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05afa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05afa-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05afa-125">INPUTS</span></span>

### <span data-ttu-id="05afa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="05afa-126">System.String</span></span>

## <span data-ttu-id="05afa-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05afa-127">OUTPUTS</span></span>

### <span data-ttu-id="05afa-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="05afa-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="05afa-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05afa-129">NOTES</span></span>

## <span data-ttu-id="05afa-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05afa-130">RELATED LINKS</span></span>
