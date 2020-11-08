---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180738"
---
# <span data-ttu-id="18f51-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="18f51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18f51-102">SYNOPSIS</span></span>
<span data-ttu-id="18f51-103">Adatfolyam-elemzési feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="18f51-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="18f51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18f51-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18f51-105">DESCRIPTION</span></span>
<span data-ttu-id="18f51-106">A **stop-AzStreamAnalyticsJob** parancsmag aszinkron módon állítja le az adatfolyam-elemzési feladatot az Azure-ban, és a használt erőforrásokat felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="18f51-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="18f51-107">A feladatdefiníció és a metaadatok az Azure portálon és a Management API-n keresztül is elérhetők maradnak az előfizetésben, így a feladat szerkeszthető és újraindítható.</span><span class="sxs-lookup"><span data-stu-id="18f51-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="18f51-108">A leállított állapotban nem terheli meg a munkát.</span><span class="sxs-lookup"><span data-stu-id="18f51-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="18f51-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18f51-109">EXAMPLES</span></span>

### <span data-ttu-id="18f51-110">Példa 1: futó feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="18f51-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="18f51-111">Ez a parancs leállítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="18f51-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="18f51-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18f51-112">PARAMETERS</span></span>

### <span data-ttu-id="18f51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f51-113">-DefaultProfile</span></span>
<span data-ttu-id="18f51-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18f51-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18f51-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18f51-115">-Name</span></span>
<span data-ttu-id="18f51-116">A leállításhoz az Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18f51-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="18f51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f51-117">-ResourceGroupName</span></span>
<span data-ttu-id="18f51-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="18f51-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="18f51-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f51-119">CommonParameters</span></span>
<span data-ttu-id="18f51-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18f51-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f51-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f51-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f51-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f51-122">INPUTS</span></span>

### <span data-ttu-id="18f51-123">System. String</span><span class="sxs-lookup"><span data-stu-id="18f51-123">System.String</span></span>

## <span data-ttu-id="18f51-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f51-124">OUTPUTS</span></span>

### <span data-ttu-id="18f51-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18f51-125">System.Boolean</span></span>

## <span data-ttu-id="18f51-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18f51-126">NOTES</span></span>

## <span data-ttu-id="18f51-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18f51-127">RELATED LINKS</span></span>

[<span data-ttu-id="18f51-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="18f51-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="18f51-130">Új – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="18f51-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="18f51-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18f51-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


