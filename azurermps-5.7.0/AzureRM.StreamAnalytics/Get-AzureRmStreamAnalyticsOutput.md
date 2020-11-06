---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: ff9ab6f4efe5794b3f1eca9b8ceab91b5cd11316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498679"
---
# <span data-ttu-id="8c7e5-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8c7e5-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="8c7e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7e5-103">A megadott adatfolyam-munkafolyamatban vagy kimenetben meghatározott kimeneteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c7e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c7e5-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c7e5-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7e5-106">A **Get-AzureRmStreamAnalyticsOutput** parancsmag felsorolja a megadott adatfolyam-adatforrásban definiált összes kimenetet, illetve információt kap egy adott kimenetről.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="8c7e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c7e5-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7e5-108">1. példa: adatok beszerzése a projekt kimenetéről</span><span class="sxs-lookup"><span data-stu-id="8c7e5-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="8c7e5-109">Ez a parancs információt ad eredményül a projekt StreamingJob meghatározott kimenetekről.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="8c7e5-110">2. példa: információk kérése egy adott projekt kimenetéről</span><span class="sxs-lookup"><span data-stu-id="8c7e5-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="8c7e5-111">Ez a parancs információt ad eredményül a projekt StreamingJob definiált kimenetről.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="8c7e5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c7e5-112">PARAMETERS</span></span>

### <span data-ttu-id="8c7e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7e5-113">-DefaultProfile</span></span>
<span data-ttu-id="8c7e5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7e5-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="8c7e5-115">-JobName</span></span>
<span data-ttu-id="8c7e5-116">Annak az Azure stream-Analytics-feladatnak a neve, amelyhez az Azure stream Analytics kimenete tartozik.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7e5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c7e5-117">-Name</span></span>
<span data-ttu-id="8c7e5-118">A lekérdezni kívánt Azure stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c7e5-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7e5-121">CommonParameters</span></span>
<span data-ttu-id="8c7e5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c7e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7e5-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7e5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c7e5-124">INPUTS</span></span>

### <span data-ttu-id="8c7e5-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="8c7e5-125">None</span></span>
<span data-ttu-id="8c7e5-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8c7e5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c7e5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c7e5-127">OUTPUTS</span></span>

### <span data-ttu-id="8c7e5-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSOutput, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="8c7e5-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="8c7e5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c7e5-129">NOTES</span></span>

## <span data-ttu-id="8c7e5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c7e5-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c7e5-131">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8c7e5-131">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="8c7e5-132">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8c7e5-132">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="8c7e5-133">Teszt-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8c7e5-133">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


