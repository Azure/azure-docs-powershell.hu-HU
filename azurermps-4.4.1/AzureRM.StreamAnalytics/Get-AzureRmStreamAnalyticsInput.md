---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: e9f4017156a72b1284de8b62d1ae2ebf7d8321ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495515"
---
# <span data-ttu-id="44819-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44819-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="44819-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44819-102">SYNOPSIS</span></span>
<span data-ttu-id="44819-103">Beolvassa az adatfolyam-elemzést.</span><span class="sxs-lookup"><span data-stu-id="44819-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44819-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44819-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44819-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44819-105">DESCRIPTION</span></span>
<span data-ttu-id="44819-106">A **Get-AzureRmStreamAnalyticsInput** parancsmag felsorolja az adatfolyam-elemző munkafolyamatban definiált összes bemenetet, illetve információt kap egy adott bevitelről.</span><span class="sxs-lookup"><span data-stu-id="44819-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="44819-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44819-107">EXAMPLES</span></span>

### <span data-ttu-id="44819-108">1. példa: információk beszerzése a projekten definiált bemenetekről</span><span class="sxs-lookup"><span data-stu-id="44819-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="44819-109">Ez a parancs információt ad eredményül a projekt StreamingJob megadott összes bemenetről.</span><span class="sxs-lookup"><span data-stu-id="44819-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="44819-110">2. példa: információk beszerzése a projekten meghatározott konkrét adatokról</span><span class="sxs-lookup"><span data-stu-id="44819-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="44819-111">Ez a parancs információt ad eredményül a projekt StreamingJob definiált EntryStream-bevitelről.</span><span class="sxs-lookup"><span data-stu-id="44819-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="44819-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44819-112">PARAMETERS</span></span>

### <span data-ttu-id="44819-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="44819-113">-JobName</span></span>
<span data-ttu-id="44819-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="44819-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="44819-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44819-115">-Name</span></span>
<span data-ttu-id="44819-116">A lekérdezni kívánt Azure stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44819-116">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="44819-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44819-117">-ResourceGroupName</span></span>
<span data-ttu-id="44819-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="44819-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="44819-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44819-119">-DefaultProfile</span></span>
<span data-ttu-id="44819-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44819-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44819-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44819-121">CommonParameters</span></span>
<span data-ttu-id="44819-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44819-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44819-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44819-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44819-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44819-124">INPUTS</span></span>

## <span data-ttu-id="44819-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44819-125">OUTPUTS</span></span>

### <span data-ttu-id="44819-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSInput, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="44819-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="44819-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44819-127">NOTES</span></span>

## <span data-ttu-id="44819-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44819-128">RELATED LINKS</span></span>

[<span data-ttu-id="44819-129">Új – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44819-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="44819-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44819-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="44819-131">Teszt-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="44819-131">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


