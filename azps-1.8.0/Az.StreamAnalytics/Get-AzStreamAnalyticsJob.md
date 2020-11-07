---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668463"
---
# <span data-ttu-id="ef11a-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ef11a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef11a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef11a-103">Beolvassa az adatfolyam-elemzési feladatokat.</span><span class="sxs-lookup"><span data-stu-id="ef11a-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="ef11a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef11a-104">SYNTAX</span></span>

### <span data-ttu-id="ef11a-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef11a-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef11a-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ef11a-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef11a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef11a-107">DESCRIPTION</span></span>
<span data-ttu-id="ef11a-108">A **Get-AzStreamAnalyticsJob** parancsmag felsorolja az Azure-előfizetésben vagy a megadott erőforráscsoportben definiált összes adatfolyam-elemzési feladatot, vagy egy erőforráscsoport munkamennyiséggel kapcsolatos adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ef11a-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="ef11a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef11a-109">EXAMPLES</span></span>

### <span data-ttu-id="ef11a-110">1. példa: információk kérése az előfizetésben szereplő összes feladatról</span><span class="sxs-lookup"><span data-stu-id="ef11a-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="ef11a-111">Ez a parancs az Azure-előfizetésből származó összes adatfolyam-elemzési feladatra vonatkozó információt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ef11a-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="ef11a-112">2. példa: információk kérése egy erőforráscsoport minden feladatáról</span><span class="sxs-lookup"><span data-stu-id="ef11a-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="ef11a-113">Ez a parancs információt ad eredményül az összes stream-Analytics-feladatról az erőforráscsoport StreamAnalytics – default-West-US.</span><span class="sxs-lookup"><span data-stu-id="ef11a-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="ef11a-114">3. példa: információ kérése egy erőforráscsoport adott feladatáról</span><span class="sxs-lookup"><span data-stu-id="ef11a-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="ef11a-115">Ez a parancs információt ad az adatfolyam-statisztika StreamingJob az erőforrás csoport StreamAnalytics – default – West-US.</span><span class="sxs-lookup"><span data-stu-id="ef11a-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="ef11a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef11a-116">PARAMETERS</span></span>

### <span data-ttu-id="ef11a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef11a-117">-DefaultProfile</span></span>
<span data-ttu-id="ef11a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef11a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef11a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef11a-119">-Name</span></span>
<span data-ttu-id="ef11a-120">A lekérdezni kívánt Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef11a-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="ef11a-121">-Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="ef11a-121">-NoExpand</span></span>
<span data-ttu-id="ef11a-122">Jelzi, hogy a parancsmag beolvassa az Azure stream Analytics-feladatot, de nem ad vissza információkat a bemenetekről, a kimenetekről és az átalakításról.</span><span class="sxs-lookup"><span data-stu-id="ef11a-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="ef11a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef11a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef11a-124">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="ef11a-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="ef11a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef11a-125">CommonParameters</span></span>
<span data-ttu-id="ef11a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef11a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef11a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef11a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef11a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef11a-128">INPUTS</span></span>

### <span data-ttu-id="ef11a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef11a-129">System.String</span></span>

### <span data-ttu-id="ef11a-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef11a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ef11a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef11a-131">OUTPUTS</span></span>

### <span data-ttu-id="ef11a-132">Microsoft. Azure. Command. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="ef11a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef11a-133">NOTES</span></span>

## <span data-ttu-id="ef11a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef11a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ef11a-135">Új – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef11a-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef11a-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ef11a-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ef11a-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


