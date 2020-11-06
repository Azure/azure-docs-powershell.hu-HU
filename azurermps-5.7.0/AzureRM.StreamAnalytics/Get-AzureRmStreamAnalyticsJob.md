---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494265"
---
# <span data-ttu-id="771cc-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="771cc-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="771cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="771cc-102">SYNOPSIS</span></span>
<span data-ttu-id="771cc-103">Beolvassa az adatfolyam-elemzési feladatokat.</span><span class="sxs-lookup"><span data-stu-id="771cc-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="771cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="771cc-104">SYNTAX</span></span>

### <span data-ttu-id="771cc-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="771cc-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="771cc-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="771cc-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="771cc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="771cc-107">DESCRIPTION</span></span>
<span data-ttu-id="771cc-108">A **Get-AzureRmStreamAnalyticsJob** parancsmag felsorolja az Azure-előfizetésben vagy a megadott erőforráscsoportben definiált összes adatfolyam-elemzési feladatot, vagy egy erőforráscsoport munkamennyiséggel kapcsolatos adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="771cc-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="771cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="771cc-109">EXAMPLES</span></span>

### <span data-ttu-id="771cc-110">1. példa: információk kérése az előfizetésben szereplő összes feladatról</span><span class="sxs-lookup"><span data-stu-id="771cc-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="771cc-111">Ez a parancs az Azure-előfizetésből származó összes adatfolyam-elemzési feladatra vonatkozó információt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="771cc-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="771cc-112">2. példa: információk kérése egy erőforráscsoport minden feladatáról</span><span class="sxs-lookup"><span data-stu-id="771cc-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="771cc-113">Ez a parancs információt ad eredményül az összes stream-Analytics-feladatról az erőforráscsoport StreamAnalytics – default-West-US.</span><span class="sxs-lookup"><span data-stu-id="771cc-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="771cc-114">3. példa: információ kérése egy erőforráscsoport adott feladatáról</span><span class="sxs-lookup"><span data-stu-id="771cc-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="771cc-115">Ez a parancs információt ad az adatfolyam-statisztika StreamingJob az erőforrás csoport StreamAnalytics – default – West-US.</span><span class="sxs-lookup"><span data-stu-id="771cc-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="771cc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="771cc-116">PARAMETERS</span></span>

### <span data-ttu-id="771cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771cc-117">-DefaultProfile</span></span>
<span data-ttu-id="771cc-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="771cc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="771cc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="771cc-119">-Name</span></span>
<span data-ttu-id="771cc-120">A lekérdezni kívánt Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="771cc-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771cc-121">-Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="771cc-121">-NoExpand</span></span>
<span data-ttu-id="771cc-122">Jelzi, hogy a parancsmag beolvassa az Azure stream Analytics-feladatot, de nem ad vissza információkat a bemenetekről, a kimenetekről és az átalakításról.</span><span class="sxs-lookup"><span data-stu-id="771cc-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="771cc-124">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="771cc-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771cc-125">CommonParameters</span></span>
<span data-ttu-id="771cc-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="771cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771cc-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771cc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771cc-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="771cc-128">INPUTS</span></span>

### <span data-ttu-id="771cc-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="771cc-129">None</span></span>
<span data-ttu-id="771cc-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="771cc-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="771cc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="771cc-131">OUTPUTS</span></span>

### <span data-ttu-id="771cc-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSJob, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="771cc-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="771cc-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="771cc-133">NOTES</span></span>

## <span data-ttu-id="771cc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="771cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="771cc-135">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="771cc-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="771cc-136">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="771cc-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="771cc-137">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="771cc-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="771cc-138">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="771cc-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


