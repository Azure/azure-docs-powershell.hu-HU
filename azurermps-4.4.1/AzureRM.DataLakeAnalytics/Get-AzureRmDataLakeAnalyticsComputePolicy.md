---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 59bc611d63d062d06b3b3bdebe9ac8b0f1349179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680577"
---
# <span data-ttu-id="ed9cf-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ed9cf-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ed9cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9cf-103">Adattó-elemzést kap a házirend vagy a számítási házirendek listájának kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed9cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed9cf-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed9cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed9cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9cf-106">A **Get-AzureRmDataLakeAnalyticsComputePolicy** megkapja a megadott Azure Data Lake Analytics számítási házirendjét vagy a házirendek listáját.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="ed9cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed9cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ed9cf-108">Példa 1: meghatározott számítási házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed9cf-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="ed9cf-109">Ez a parancs a megadott számítási házirendet a "myPolicy" névvel a "contosoadla" fiókban kapja.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="ed9cf-110">2. példa: a fiókban található összes számítási házirend listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed9cf-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="ed9cf-111">Ez a parancs a "contosoadla" fiókban a számítási házirendek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="ed9cf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed9cf-112">PARAMETERS</span></span>

### <span data-ttu-id="ed9cf-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="ed9cf-113">-Account</span></span>
<span data-ttu-id="ed9cf-114">Annak a fióknak a neve, amelyből kiszámítja a számítási házirendet vagy a házirendeket.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="ed9cf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed9cf-115">-Name</span></span>
<span data-ttu-id="ed9cf-116">A beszerzéshez használandó számítási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-116">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="ed9cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed9cf-118">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="ed9cf-119">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="ed9cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9cf-120">-DefaultProfile</span></span>
<span data-ttu-id="ed9cf-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed9cf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9cf-122">CommonParameters</span></span>
<span data-ttu-id="ed9cf-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed9cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9cf-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9cf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9cf-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9cf-125">INPUTS</span></span>

### <span data-ttu-id="ed9cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ed9cf-126">System.String</span></span>

## <span data-ttu-id="ed9cf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9cf-127">OUTPUTS</span></span>

### <span data-ttu-id="ed9cf-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ed9cf-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="ed9cf-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ed9cf-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ed9cf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed9cf-130">NOTES</span></span>

## <span data-ttu-id="ed9cf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed9cf-131">RELATED LINKS</span></span>

