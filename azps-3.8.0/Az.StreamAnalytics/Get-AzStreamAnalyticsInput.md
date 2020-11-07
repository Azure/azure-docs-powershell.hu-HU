---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: ba64089da3673957eead10ef1301f5c7c4a59467
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847489"
---
# <span data-ttu-id="500e7-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="500e7-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="500e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="500e7-102">SYNOPSIS</span></span>
<span data-ttu-id="500e7-103">Beolvassa az adatfolyam-elemzést.</span><span class="sxs-lookup"><span data-stu-id="500e7-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="500e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="500e7-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="500e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="500e7-105">DESCRIPTION</span></span>
<span data-ttu-id="500e7-106">A **Get-AzStreamAnalyticsInput** parancsmag felsorolja az adatfolyam-elemző munkafolyamatban definiált összes bemenetet, illetve információt kap egy adott bevitelről.</span><span class="sxs-lookup"><span data-stu-id="500e7-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="500e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="500e7-107">EXAMPLES</span></span>

### <span data-ttu-id="500e7-108">1. példa: információk beszerzése a projekten definiált bemenetekről</span><span class="sxs-lookup"><span data-stu-id="500e7-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="500e7-109">Ez a parancs információt ad eredményül a projekt StreamingJob megadott összes bemenetről.</span><span class="sxs-lookup"><span data-stu-id="500e7-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="500e7-110">2. példa: információk beszerzése a projekten meghatározott konkrét adatokról</span><span class="sxs-lookup"><span data-stu-id="500e7-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="500e7-111">Ez a parancs információt ad eredményül a projekt StreamingJob definiált EntryStream-bevitelről.</span><span class="sxs-lookup"><span data-stu-id="500e7-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="500e7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="500e7-112">PARAMETERS</span></span>

### <span data-ttu-id="500e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500e7-113">-DefaultProfile</span></span>
<span data-ttu-id="500e7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="500e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="500e7-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="500e7-115">-JobName</span></span>
<span data-ttu-id="500e7-116">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="500e7-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="500e7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="500e7-117">-Name</span></span>
<span data-ttu-id="500e7-118">A lekérdezni kívánt Azure stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="500e7-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="500e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="500e7-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="500e7-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="500e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500e7-121">CommonParameters</span></span>
<span data-ttu-id="500e7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="500e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500e7-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500e7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500e7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="500e7-124">INPUTS</span></span>

### <span data-ttu-id="500e7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="500e7-125">System.String</span></span>

## <span data-ttu-id="500e7-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="500e7-126">OUTPUTS</span></span>

### <span data-ttu-id="500e7-127">Microsoft. Azure. Command. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="500e7-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="500e7-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="500e7-128">NOTES</span></span>

## <span data-ttu-id="500e7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="500e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="500e7-130">Új – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="500e7-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="500e7-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="500e7-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="500e7-132">Teszt-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="500e7-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


