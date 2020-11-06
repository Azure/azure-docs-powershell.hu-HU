---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: d4ec2865f0a0efcc4a306d0614df1c27adddc5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502811"
---
# <span data-ttu-id="12fc1-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="12fc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="12fc1-103">Adatfolyam-elemzési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="12fc1-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12fc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12fc1-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12fc1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="12fc1-106">A **stop-AzureRmStreamAnalyticsJob** parancsmag aszinkron módon állítja le az adatfolyam-elemzési feladatot az Azure-ban, és a használt erőforrásokat felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="12fc1-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="12fc1-107">A feladatdefiníció és a metaadatok az Azure portálon és a Management API-n keresztül is elérhetők maradnak az előfizetésben, így a feladat szerkeszthető és újraindítható.</span><span class="sxs-lookup"><span data-stu-id="12fc1-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="12fc1-108">A leállított állapotban nem terheli meg a munkát.</span><span class="sxs-lookup"><span data-stu-id="12fc1-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="12fc1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="12fc1-109">EXAMPLES</span></span>

### <span data-ttu-id="12fc1-110">Példa 1: futó feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="12fc1-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="12fc1-111">Ez a parancs leállítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="12fc1-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="12fc1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12fc1-112">PARAMETERS</span></span>

### <span data-ttu-id="12fc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fc1-113">-DefaultProfile</span></span>
<span data-ttu-id="12fc1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12fc1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12fc1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12fc1-115">-Name</span></span>
<span data-ttu-id="12fc1-116">A leállításhoz az Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12fc1-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fc1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fc1-117">-ResourceGroupName</span></span>
<span data-ttu-id="12fc1-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="12fc1-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fc1-119">CommonParameters</span></span>
<span data-ttu-id="12fc1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12fc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fc1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fc1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fc1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12fc1-122">INPUTS</span></span>

### <span data-ttu-id="12fc1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="12fc1-123">System.String</span></span>

## <span data-ttu-id="12fc1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12fc1-124">OUTPUTS</span></span>

### <span data-ttu-id="12fc1-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12fc1-125">System.Boolean</span></span>

## <span data-ttu-id="12fc1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12fc1-126">NOTES</span></span>

## <span data-ttu-id="12fc1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12fc1-127">RELATED LINKS</span></span>

[<span data-ttu-id="12fc1-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12fc1-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12fc1-130">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-130">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12fc1-131">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-131">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="12fc1-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="12fc1-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


