---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150146"
---
# <span data-ttu-id="a90cf-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="a90cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a90cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a90cf-103">Leállít egy Stream Analytics-feladatot.</span><span class="sxs-lookup"><span data-stu-id="a90cf-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="a90cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a90cf-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a90cf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a90cf-105">DESCRIPTION</span></span>
<span data-ttu-id="a90cf-106">A **Stop-AzStreamAnalytics Job** parancsmag aszinkron módon leállítja egy Stream Analytics-feladat futtatását az Azure-ban, és a felhasznált erőforrásokat használja.</span><span class="sxs-lookup"><span data-stu-id="a90cf-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="a90cf-107">A feladatdefiníció és a metaadatok elérhetők maradnak az előfizetésen belül az Azure Portal és a Felügyeleti API-k segítségével, így a feladat szerkeszthető és újraindítható.</span><span class="sxs-lookup"><span data-stu-id="a90cf-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="a90cf-108">A leállítva állapotban végzett munkáért nem számítunk fel díjat.</span><span class="sxs-lookup"><span data-stu-id="a90cf-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="a90cf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a90cf-109">EXAMPLES</span></span>

### <span data-ttu-id="a90cf-110">1. példa: Futó feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="a90cf-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="a90cf-111">Ez a parancs leállítja a Streaming Streaming Streaming feladatot.</span><span class="sxs-lookup"><span data-stu-id="a90cf-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="a90cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a90cf-112">PARAMETERS</span></span>

### <span data-ttu-id="a90cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90cf-113">-DefaultProfile</span></span>
<span data-ttu-id="a90cf-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a90cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a90cf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a90cf-115">-Name</span></span>
<span data-ttu-id="a90cf-116">A leállíthatja az Azure Stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a90cf-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="a90cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="a90cf-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="a90cf-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="a90cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90cf-119">CommonParameters</span></span>
<span data-ttu-id="a90cf-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a90cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90cf-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90cf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90cf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a90cf-122">INPUTS</span></span>

### <span data-ttu-id="a90cf-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a90cf-123">System.String</span></span>

## <span data-ttu-id="a90cf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a90cf-124">OUTPUTS</span></span>

### <span data-ttu-id="a90cf-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a90cf-125">System.Boolean</span></span>

## <span data-ttu-id="a90cf-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a90cf-126">NOTES</span></span>

## <span data-ttu-id="a90cf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a90cf-127">RELATED LINKS</span></span>

[<span data-ttu-id="a90cf-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a90cf-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a90cf-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a90cf-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a90cf-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a90cf-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


