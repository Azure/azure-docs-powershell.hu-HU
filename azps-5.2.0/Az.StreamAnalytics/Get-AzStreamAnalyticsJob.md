---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366433"
---
# <span data-ttu-id="58e79-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="58e79-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="58e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e79-102">SYNOPSIS</span></span>
<span data-ttu-id="58e79-103">Stream Analytics-feladatokkal kapcsolatos információkat kap.</span><span class="sxs-lookup"><span data-stu-id="58e79-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="58e79-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58e79-104">SYNTAX</span></span>

### <span data-ttu-id="58e79-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="58e79-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e79-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="58e79-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e79-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58e79-107">DESCRIPTION</span></span>
<span data-ttu-id="58e79-108">A **Get-AzStreamAnalytics Jobs** parancsmag felsorolja az Azure-előfizetésben vagy adott erőforráscsoportban definiált Összes Stream Analytics-feladatot, illetve egy erőforráscsoporton belül egy adott feladatra vonatkozó feladatinformációkat kap.</span><span class="sxs-lookup"><span data-stu-id="58e79-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="58e79-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58e79-109">EXAMPLES</span></span>

### <span data-ttu-id="58e79-110">1. PÉLDA: Információ az előfizetésben található összes állásról</span><span class="sxs-lookup"><span data-stu-id="58e79-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="58e79-111">Ez a parancs az Azure-előfizetés összes Stream Analytics-feladatával kapcsolatos információkat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="58e79-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="58e79-112">2. PÉLDA: Információ az erőforráscsoportokban található összes feladatról</span><span class="sxs-lookup"><span data-stu-id="58e79-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="58e79-113">Ez a parancs a StreamAnalytics-Default-West-US erőforráscsoport összes Stream Analytics-feladatával kapcsolatos információkat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="58e79-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="58e79-114">3. PÉLDA: Információ lekérte egy erőforráscsoport adott feladatának adatait</span><span class="sxs-lookup"><span data-stu-id="58e79-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="58e79-115">Ez a parancs információkat ad vissza a Stream Analytics Streaming Job feladatról a StreamAnalytics-Default-West-US erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="58e79-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="58e79-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e79-116">PARAMETERS</span></span>

### <span data-ttu-id="58e79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e79-117">-DefaultProfile</span></span>
<span data-ttu-id="58e79-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58e79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e79-119">-Name</span><span class="sxs-lookup"><span data-stu-id="58e79-119">-Name</span></span>
<span data-ttu-id="58e79-120">Megadja a lekért Azure Stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="58e79-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e79-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="58e79-121">-NoExpand</span></span>
<span data-ttu-id="58e79-122">Azt jelzi, hogy a parancsmag beolvassa az Azure Stream Analytics-feladatot, de nem ad vissza adatokat a bemenetekkel, kimenetekkel és átalakításokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="58e79-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e79-123">-ResourceGroupName</span></span>
<span data-ttu-id="58e79-124">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="58e79-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e79-125">CommonParameters</span></span>
<span data-ttu-id="58e79-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e79-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e79-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e79-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58e79-128">INPUTS</span></span>

### <span data-ttu-id="58e79-129">System.String</span><span class="sxs-lookup"><span data-stu-id="58e79-129">System.String</span></span>

### <span data-ttu-id="58e79-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58e79-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58e79-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58e79-131">OUTPUTS</span></span>

### <span data-ttu-id="58e79-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="58e79-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="58e79-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58e79-133">NOTES</span></span>

## <span data-ttu-id="58e79-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58e79-134">RELATED LINKS</span></span>

[<span data-ttu-id="58e79-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="58e79-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="58e79-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="58e79-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="58e79-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="58e79-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="58e79-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="58e79-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


