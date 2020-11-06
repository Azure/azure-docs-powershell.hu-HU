---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 24313884b92a9a4c738425d64463c695ff689c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493813"
---
# <span data-ttu-id="2a39f-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2a39f-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="2a39f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a39f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a39f-103">Információkat kap az adatfolyam-elemzésről.</span><span class="sxs-lookup"><span data-stu-id="2a39f-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a39f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a39f-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a39f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a39f-105">DESCRIPTION</span></span>
<span data-ttu-id="2a39f-106">A **Get-AzureRmStreamAnalyticsTransformation** parancsmag információkat kap az adatfolyam-elemzési feladatokon meghatározott átalakításról.</span><span class="sxs-lookup"><span data-stu-id="2a39f-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="2a39f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2a39f-107">EXAMPLES</span></span>

### <span data-ttu-id="2a39f-108">1. példa: információk kérése az adatfolyam-elemzésről</span><span class="sxs-lookup"><span data-stu-id="2a39f-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="2a39f-109">Ez a parancs információt ad az StreamingJob nevű StreamingJob nevű átalakításról.</span><span class="sxs-lookup"><span data-stu-id="2a39f-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="2a39f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a39f-110">PARAMETERS</span></span>

### <span data-ttu-id="2a39f-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2a39f-111">-JobName</span></span>
<span data-ttu-id="2a39f-112">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="2a39f-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="2a39f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a39f-113">-Name</span></span>
<span data-ttu-id="2a39f-114">A lekérdezni kívánt Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a39f-114">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a39f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a39f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a39f-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="2a39f-116">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="2a39f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a39f-117">-DefaultProfile</span></span>
<span data-ttu-id="2a39f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a39f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a39f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a39f-119">CommonParameters</span></span>
<span data-ttu-id="2a39f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a39f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a39f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a39f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a39f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a39f-122">INPUTS</span></span>

## <span data-ttu-id="2a39f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a39f-123">OUTPUTS</span></span>

### <span data-ttu-id="2a39f-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSTransformation, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="2a39f-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="2a39f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a39f-125">NOTES</span></span>

## <span data-ttu-id="2a39f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a39f-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a39f-127">Új – AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2a39f-127">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


