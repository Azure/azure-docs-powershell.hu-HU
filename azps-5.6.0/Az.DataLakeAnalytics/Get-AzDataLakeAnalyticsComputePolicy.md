---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 6867e57e5465ddab8fc7f0adbfdb3197d8ac1245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942810"
---
# <span data-ttu-id="cca95-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="cca95-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="cca95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca95-102">SYNOPSIS</span></span>
<span data-ttu-id="cca95-103">A Data Lake Analytics számítási házirendet vagy a számítási házirendek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cca95-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="cca95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cca95-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca95-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cca95-105">DESCRIPTION</span></span>
<span data-ttu-id="cca95-106">A **Get-AzDataLakeAnalyticsComputePolicy** megkapja a megadott Azure Data Lake Analytics számítási házirendet vagy házirendek listáját.</span><span class="sxs-lookup"><span data-stu-id="cca95-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="cca95-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cca95-107">EXAMPLES</span></span>

### <span data-ttu-id="cca95-108">1. példa: Meghatározott számítási házirend lekérte</span><span class="sxs-lookup"><span data-stu-id="cca95-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="cca95-109">Ez a parancs a megadott számítási házirendet kapja meg a "contosoadla" fiókban a "myPolicy" névvel.</span><span class="sxs-lookup"><span data-stu-id="cca95-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="cca95-110">2. példa: A fiókban található összes számítási házirend listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="cca95-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="cca95-111">Ez a parancs a "contosoadla" fiókban található összes számítási házirend listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="cca95-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="cca95-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cca95-112">PARAMETERS</span></span>

### <span data-ttu-id="cca95-113">-Account</span><span class="sxs-lookup"><span data-stu-id="cca95-113">-Account</span></span>
<span data-ttu-id="cca95-114">Annak a fióknak a neve, amelyből be szeretné szerezni a számítási házirendet vagy házirendeket.</span><span class="sxs-lookup"><span data-stu-id="cca95-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="cca95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca95-115">-DefaultProfile</span></span>
<span data-ttu-id="cca95-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cca95-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cca95-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cca95-117">-Name</span></span>
<span data-ttu-id="cca95-118">A lekért számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="cca95-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="cca95-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca95-119">-ResourceGroupName</span></span>
<span data-ttu-id="cca95-120">Annak az erőforráscsoportnak a neve, amely alatt a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="cca95-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="cca95-121">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="cca95-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="cca95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca95-122">CommonParameters</span></span>
<span data-ttu-id="cca95-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca95-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca95-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca95-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cca95-125">INPUTS</span></span>

### <span data-ttu-id="cca95-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cca95-126">System.String</span></span>

## <span data-ttu-id="cca95-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cca95-127">OUTPUTS</span></span>

### <span data-ttu-id="cca95-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="cca95-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="cca95-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cca95-129">NOTES</span></span>

## <span data-ttu-id="cca95-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cca95-130">RELATED LINKS</span></span>
