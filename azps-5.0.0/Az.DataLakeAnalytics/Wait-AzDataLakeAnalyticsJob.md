---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297956"
---
# <span data-ttu-id="d33b6-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d33b6-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d33b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d33b6-102">SYNOPSIS</span></span>
<span data-ttu-id="d33b6-103">Várakozás a feladatok elvégzésére.</span><span class="sxs-lookup"><span data-stu-id="d33b6-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="d33b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d33b6-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d33b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d33b6-105">DESCRIPTION</span></span>
<span data-ttu-id="d33b6-106">A **WAIT-AzDataLakeAnalyticsJob** parancsmag megvárja az Azure Data Lake-tó elemzési feladatát a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="d33b6-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="d33b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d33b6-107">EXAMPLES</span></span>

### <span data-ttu-id="d33b6-108">1. példa: várakozás a feladatok elvégzésére</span><span class="sxs-lookup"><span data-stu-id="d33b6-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="d33b6-109">A következő parancs megvárja, hogy a megadott azonosítót végrehajtva végezze el a feladatot.</span><span class="sxs-lookup"><span data-stu-id="d33b6-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="d33b6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d33b6-110">PARAMETERS</span></span>

### <span data-ttu-id="d33b6-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d33b6-111">-Account</span></span>
<span data-ttu-id="d33b6-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d33b6-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d33b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33b6-113">-DefaultProfile</span></span>
<span data-ttu-id="d33b6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d33b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d33b6-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="d33b6-115">-JobId</span></span>
<span data-ttu-id="d33b6-116">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="d33b6-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="d33b6-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d33b6-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="d33b6-118">Azt adja meg, hogy hány másodpercig várjon a program a várakozási műveletből való kilépés előtt.</span><span class="sxs-lookup"><span data-stu-id="d33b6-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="d33b6-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d33b6-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="d33b6-120">Adja meg, hogy hány másodpercig tartson a program a feladat állapota között.</span><span class="sxs-lookup"><span data-stu-id="d33b6-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="d33b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33b6-121">CommonParameters</span></span>
<span data-ttu-id="d33b6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d33b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33b6-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33b6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33b6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d33b6-124">INPUTS</span></span>

### <span data-ttu-id="d33b6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d33b6-125">System.String</span></span>

### <span data-ttu-id="d33b6-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d33b6-126">System.Guid</span></span>

### <span data-ttu-id="d33b6-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d33b6-127">System.Int32</span></span>

## <span data-ttu-id="d33b6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d33b6-128">OUTPUTS</span></span>

### <span data-ttu-id="d33b6-129">Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="d33b6-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="d33b6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d33b6-130">NOTES</span></span>

## <span data-ttu-id="d33b6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d33b6-131">RELATED LINKS</span></span>

[<span data-ttu-id="d33b6-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d33b6-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d33b6-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d33b6-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d33b6-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d33b6-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


