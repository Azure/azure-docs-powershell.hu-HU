---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496788"
---
# <span data-ttu-id="c3fa7-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="c3fa7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fa7-103">Beolvassa az adatfolyam-elemzési feladatokat.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3fa7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3fa7-104">SYNTAX</span></span>

### <span data-ttu-id="c3fa7-105">Adatfolyam-elemzési objektumok a megadott erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="c3fa7-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3fa7-106">Stream Analytics-objektumok a megadott előfizetésben</span><span class="sxs-lookup"><span data-stu-id="c3fa7-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3fa7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="c3fa7-108">A **Get-AzureRmStreamAnalyticsJob** parancsmag felsorolja az Azure-előfizetésben vagy a megadott erőforráscsoportben definiált összes adatfolyam-elemzési feladatot, vagy egy erőforráscsoport munkamennyiséggel kapcsolatos adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="c3fa7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c3fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="c3fa7-110">1. példa: információk kérése az előfizetésben szereplő összes feladatról</span><span class="sxs-lookup"><span data-stu-id="c3fa7-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="c3fa7-111">Ez a parancs az Azure-előfizetésből származó összes adatfolyam-elemzési feladatra vonatkozó információt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="c3fa7-112">2. példa: információk kérése egy erőforráscsoport minden feladatáról</span><span class="sxs-lookup"><span data-stu-id="c3fa7-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="c3fa7-113">Ez a parancs információt ad eredményül az összes stream-Analytics-feladatról az erőforráscsoport StreamAnalytics – default-West-US.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="c3fa7-114">3. példa: információ kérése egy erőforráscsoport adott feladatáról</span><span class="sxs-lookup"><span data-stu-id="c3fa7-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="c3fa7-115">Ez a parancs információt ad az adatfolyam-statisztika StreamingJob az erőforrás csoport StreamAnalytics – default – West-US.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="c3fa7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3fa7-116">PARAMETERS</span></span>

### <span data-ttu-id="c3fa7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3fa7-117">-Name</span></span>
<span data-ttu-id="c3fa7-118">A lekérdezni kívánt Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fa7-119">-Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="c3fa7-119">-NoExpand</span></span>
<span data-ttu-id="c3fa7-120">Jelzi, hogy a parancsmag beolvassa az Azure stream Analytics-feladatot, de nem ad vissza információkat a bemenetekről, a kimenetekről és az átalakításról.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="c3fa7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fa7-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3fa7-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fa7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fa7-123">-DefaultProfile</span></span>
<span data-ttu-id="c3fa7-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3fa7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3fa7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fa7-125">CommonParameters</span></span>
<span data-ttu-id="c3fa7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3fa7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fa7-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fa7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fa7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fa7-128">INPUTS</span></span>

## <span data-ttu-id="c3fa7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fa7-129">OUTPUTS</span></span>

### <span data-ttu-id="c3fa7-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSJob, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="c3fa7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3fa7-131">NOTES</span></span>

## <span data-ttu-id="c3fa7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3fa7-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3fa7-133">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c3fa7-134">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c3fa7-135">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="c3fa7-136">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c3fa7-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


