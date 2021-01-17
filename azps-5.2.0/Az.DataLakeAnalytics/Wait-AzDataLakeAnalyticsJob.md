---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339581"
---
# <span data-ttu-id="8ade0-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8ade0-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8ade0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ade0-102">SYNOPSIS</span></span>
<span data-ttu-id="8ade0-103">Megvárja, amíg befejeződik egy feladat.</span><span class="sxs-lookup"><span data-stu-id="8ade0-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="8ade0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ade0-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ade0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ade0-105">DESCRIPTION</span></span>
<span data-ttu-id="8ade0-106">A **Wait-AzDataLakeAnalytics Job** parancsmag az Azure Data Lake Analytics-feladat befejezésére vár.</span><span class="sxs-lookup"><span data-stu-id="8ade0-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="8ade0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ade0-107">EXAMPLES</span></span>

### <span data-ttu-id="8ade0-108">1. példa: Várjon, amíg befejeződik egy feladat</span><span class="sxs-lookup"><span data-stu-id="8ade0-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="8ade0-109">Az alábbi parancs megvárja, amíg a megadott azonosítójú feladat befejeződik.</span><span class="sxs-lookup"><span data-stu-id="8ade0-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="8ade0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ade0-110">PARAMETERS</span></span>

### <span data-ttu-id="8ade0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="8ade0-111">-Account</span></span>
<span data-ttu-id="8ade0-112">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ade0-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8ade0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ade0-113">-DefaultProfile</span></span>
<span data-ttu-id="8ade0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ade0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ade0-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="8ade0-115">-JobId</span></span>
<span data-ttu-id="8ade0-116">Annak a feladatnak az azonosítóját adja meg, amelynek várnia kell.</span><span class="sxs-lookup"><span data-stu-id="8ade0-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ade0-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ade0-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="8ade0-118">A várakozási műveletből való kilépésig várakozási másodpercek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ade0-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ade0-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ade0-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="8ade0-120">Adja meg a feladatállapot egyes ellenőrzései között eltelt másodpercek számát.</span><span class="sxs-lookup"><span data-stu-id="8ade0-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ade0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ade0-121">CommonParameters</span></span>
<span data-ttu-id="8ade0-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ade0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ade0-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ade0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ade0-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ade0-124">INPUTS</span></span>

### <span data-ttu-id="8ade0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8ade0-125">System.String</span></span>

### <span data-ttu-id="8ade0-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8ade0-126">System.Guid</span></span>

### <span data-ttu-id="8ade0-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8ade0-127">System.Int32</span></span>

## <span data-ttu-id="8ade0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ade0-128">OUTPUTS</span></span>

### <span data-ttu-id="8ade0-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="8ade0-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="8ade0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ade0-130">NOTES</span></span>

## <span data-ttu-id="8ade0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ade0-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ade0-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8ade0-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8ade0-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8ade0-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8ade0-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8ade0-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


