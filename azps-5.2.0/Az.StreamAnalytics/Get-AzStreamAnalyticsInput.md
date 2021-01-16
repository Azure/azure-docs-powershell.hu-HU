---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366447"
---
# <span data-ttu-id="99a29-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="99a29-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="99a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a29-102">SYNOPSIS</span></span>
<span data-ttu-id="99a29-103">Stream Analytics-feladatokkal bevitt adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="99a29-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="99a29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99a29-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99a29-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99a29-105">DESCRIPTION</span></span>
<span data-ttu-id="99a29-106">A **Get-AzStreamAnalyticsInput** parancsmag felsorolja a Stream Analytics-feladatban definiált összes bemenetet, vagy információt kap egy adott bemenetről.</span><span class="sxs-lookup"><span data-stu-id="99a29-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="99a29-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99a29-107">EXAMPLES</span></span>

### <span data-ttu-id="99a29-108">1. példa: Információk lekérte a feladathoz definiált bemeneteket</span><span class="sxs-lookup"><span data-stu-id="99a29-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="99a29-109">Ez a parancs információkat ad vissza a Streaming Streaming Streaming feladaton definiált összes bemenetről.</span><span class="sxs-lookup"><span data-stu-id="99a29-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="99a29-110">2. példa: Információ lekérte egy adott bemenetről egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="99a29-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="99a29-111">Ez a parancs információkat ad vissza a Stream Streaming Streaming feladaton definiált EntryStream bemenetről.</span><span class="sxs-lookup"><span data-stu-id="99a29-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="99a29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99a29-112">PARAMETERS</span></span>

### <span data-ttu-id="99a29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a29-113">-DefaultProfile</span></span>
<span data-ttu-id="99a29-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99a29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99a29-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="99a29-115">-JobName</span></span>
<span data-ttu-id="99a29-116">Annak az Azure Stream Analytics-feladatnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="99a29-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="99a29-117">-Name</span><span class="sxs-lookup"><span data-stu-id="99a29-117">-Name</span></span>
<span data-ttu-id="99a29-118">A lekérni szükséges Azure Stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99a29-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a29-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a29-119">-ResourceGroupName</span></span>
<span data-ttu-id="99a29-120">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="99a29-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="99a29-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a29-121">CommonParameters</span></span>
<span data-ttu-id="99a29-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a29-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a29-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a29-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a29-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99a29-124">INPUTS</span></span>

### <span data-ttu-id="99a29-125">System.String</span><span class="sxs-lookup"><span data-stu-id="99a29-125">System.String</span></span>

## <span data-ttu-id="99a29-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99a29-126">OUTPUTS</span></span>

### <span data-ttu-id="99a29-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="99a29-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="99a29-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99a29-128">NOTES</span></span>

## <span data-ttu-id="99a29-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99a29-129">RELATED LINKS</span></span>

[<span data-ttu-id="99a29-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="99a29-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="99a29-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="99a29-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="99a29-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="99a29-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


