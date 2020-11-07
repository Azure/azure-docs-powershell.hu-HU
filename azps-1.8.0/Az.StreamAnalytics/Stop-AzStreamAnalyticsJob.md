---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 050bfccef2b6286ef45a96a9feedc99ef4745115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668431"
---
# <span data-ttu-id="6b057-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="6b057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b057-102">SYNOPSIS</span></span>
<span data-ttu-id="6b057-103">Adatfolyam-elemzési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="6b057-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="6b057-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b057-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b057-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b057-105">DESCRIPTION</span></span>
<span data-ttu-id="6b057-106">A **stop-AzStreamAnalyticsJob** parancsmag aszinkron módon állítja le az adatfolyam-elemzési feladatot az Azure-ban, és a használt erőforrásokat felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="6b057-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="6b057-107">A feladatdefiníció és a metaadatok az Azure portálon és a Management API-n keresztül is elérhetők maradnak az előfizetésben, így a feladat szerkeszthető és újraindítható.</span><span class="sxs-lookup"><span data-stu-id="6b057-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="6b057-108">A leállított állapotban nem terheli meg a munkát.</span><span class="sxs-lookup"><span data-stu-id="6b057-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="6b057-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b057-109">EXAMPLES</span></span>

### <span data-ttu-id="6b057-110">Példa 1: futó feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="6b057-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="6b057-111">Ez a parancs leállítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6b057-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="6b057-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b057-112">PARAMETERS</span></span>

### <span data-ttu-id="6b057-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b057-113">-DefaultProfile</span></span>
<span data-ttu-id="6b057-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b057-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b057-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b057-115">-Name</span></span>
<span data-ttu-id="6b057-116">A leállításhoz az Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b057-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="6b057-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b057-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b057-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="6b057-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="6b057-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b057-119">CommonParameters</span></span>
<span data-ttu-id="6b057-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b057-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b057-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b057-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b057-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b057-122">INPUTS</span></span>

### <span data-ttu-id="6b057-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6b057-123">System.String</span></span>

## <span data-ttu-id="6b057-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b057-124">OUTPUTS</span></span>

### <span data-ttu-id="6b057-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b057-125">System.Boolean</span></span>

## <span data-ttu-id="6b057-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b057-126">NOTES</span></span>

## <span data-ttu-id="6b057-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b057-127">RELATED LINKS</span></span>

[<span data-ttu-id="6b057-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6b057-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6b057-130">Új – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6b057-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6b057-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b057-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


