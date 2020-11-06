---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503787"
---
# <span data-ttu-id="81ba7-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81ba7-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="81ba7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="81ba7-103">Várakozás a feladatok elvégzésére.</span><span class="sxs-lookup"><span data-stu-id="81ba7-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ba7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81ba7-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ba7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="81ba7-106">A **WAIT-AzureRmDataLakeAnalyticsJob** parancsmag megvárja az Azure Data Lake-tó elemzési feladatát a befejezéshez.</span><span class="sxs-lookup"><span data-stu-id="81ba7-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="81ba7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="81ba7-108">1. példa: várakozás a feladatok elvégzésére</span><span class="sxs-lookup"><span data-stu-id="81ba7-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="81ba7-109">A következő parancs megvárja, hogy a megadott azonosítót végrehajtva végezze el a feladatot.</span><span class="sxs-lookup"><span data-stu-id="81ba7-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="81ba7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="81ba7-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="81ba7-111">-Account</span></span>
<span data-ttu-id="81ba7-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81ba7-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ba7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ba7-113">-DefaultProfile</span></span>
<span data-ttu-id="81ba7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="81ba7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ba7-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="81ba7-115">-JobId</span></span>
<span data-ttu-id="81ba7-116">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre várni szeretne.</span><span class="sxs-lookup"><span data-stu-id="81ba7-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81ba7-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="81ba7-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="81ba7-118">Azt adja meg, hogy hány másodpercig várjon a program a várakozási műveletből való kilépés előtt.</span><span class="sxs-lookup"><span data-stu-id="81ba7-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ba7-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="81ba7-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="81ba7-120">Adja meg, hogy hány másodpercig tartson a program a feladat állapota között.</span><span class="sxs-lookup"><span data-stu-id="81ba7-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ba7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ba7-121">CommonParameters</span></span>
<span data-ttu-id="81ba7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81ba7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ba7-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ba7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ba7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81ba7-124">INPUTS</span></span>

### <span data-ttu-id="81ba7-125">GUID</span><span class="sxs-lookup"><span data-stu-id="81ba7-125">Guid</span></span>
<span data-ttu-id="81ba7-126">A ' JobId ' paraméter a pipeline "GUID" típusú értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81ba7-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="81ba7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81ba7-127">OUTPUTS</span></span>

### <span data-ttu-id="81ba7-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="81ba7-128">JobInformation</span></span>
<span data-ttu-id="81ba7-129">A befejezett munka utolsó munkarészletei.</span><span class="sxs-lookup"><span data-stu-id="81ba7-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="81ba7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81ba7-130">NOTES</span></span>

## <span data-ttu-id="81ba7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81ba7-131">RELATED LINKS</span></span>

[<span data-ttu-id="81ba7-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81ba7-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="81ba7-133">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81ba7-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="81ba7-134">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81ba7-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


