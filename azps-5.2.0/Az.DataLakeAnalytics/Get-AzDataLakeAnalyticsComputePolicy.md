---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338693"
---
# <span data-ttu-id="7dbf1-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7dbf1-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7dbf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbf1-103">A Data Lake Analytics számítási házirendet vagy a számítási házirendek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="7dbf1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7dbf1-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dbf1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7dbf1-105">DESCRIPTION</span></span>
<span data-ttu-id="7dbf1-106">A **Get-AzDataLakeAnalyticsComputePolicy** megkapja a megadott Azure Data Lake Analytics számítási házirendet vagy házirendek listáját.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="7dbf1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7dbf1-107">EXAMPLES</span></span>

### <span data-ttu-id="7dbf1-108">1. példa: Meghatározott számítási házirend lekérte</span><span class="sxs-lookup"><span data-stu-id="7dbf1-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="7dbf1-109">Ez a parancs a megadott számítási házirendet kapja meg a "contosoadla" fiókban a "myPolicy" névvel.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="7dbf1-110">2. példa: A fiókban található összes számítási házirend listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="7dbf1-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="7dbf1-111">Ez a parancs a "contosoadla" fiókban található összes számítási házirend listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="7dbf1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dbf1-112">PARAMETERS</span></span>

### <span data-ttu-id="7dbf1-113">-Account</span><span class="sxs-lookup"><span data-stu-id="7dbf1-113">-Account</span></span>
<span data-ttu-id="7dbf1-114">Annak a fióknak a neve, amelyből be szeretné szerezni a számítási házirendet vagy házirendeket.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="7dbf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbf1-115">-DefaultProfile</span></span>
<span data-ttu-id="7dbf1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7dbf1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dbf1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7dbf1-117">-Name</span></span>
<span data-ttu-id="7dbf1-118">A lekért számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="7dbf1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbf1-119">-ResourceGroupName</span></span>
<span data-ttu-id="7dbf1-120">Annak az erőforráscsoportnak a neve, amely alatt a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="7dbf1-121">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="7dbf1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbf1-122">CommonParameters</span></span>
<span data-ttu-id="7dbf1-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dbf1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbf1-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dbf1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbf1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dbf1-125">INPUTS</span></span>

### <span data-ttu-id="7dbf1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7dbf1-126">System.String</span></span>

## <span data-ttu-id="7dbf1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dbf1-127">OUTPUTS</span></span>

### <span data-ttu-id="7dbf1-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="7dbf1-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="7dbf1-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7dbf1-129">NOTES</span></span>

## <span data-ttu-id="7dbf1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dbf1-130">RELATED LINKS</span></span>
