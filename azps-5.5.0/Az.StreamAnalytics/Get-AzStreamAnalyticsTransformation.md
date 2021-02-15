---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150227"
---
# <span data-ttu-id="31c24-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="31c24-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="31c24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31c24-102">SYNOPSIS</span></span>
<span data-ttu-id="31c24-103">Információkat kap a Stream Analytics-feladatátalakításról.</span><span class="sxs-lookup"><span data-stu-id="31c24-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="31c24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31c24-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31c24-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31c24-105">DESCRIPTION</span></span>
<span data-ttu-id="31c24-106">A **Get-AzStreamAnalyticsTransformation** parancsmag információt kap a Stream Analytics-feladaton definiált átalakításról.</span><span class="sxs-lookup"><span data-stu-id="31c24-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="31c24-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31c24-107">EXAMPLES</span></span>

### <span data-ttu-id="31c24-108">1. PÉLDA: Információ a Stream Analytics átalakításáról</span><span class="sxs-lookup"><span data-stu-id="31c24-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="31c24-109">Ez a parancs információkat ad vissza a Streaming Streaming Streaming nevű átalakításról a Streaming Streaming Nevű feladaton.</span><span class="sxs-lookup"><span data-stu-id="31c24-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="31c24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31c24-110">PARAMETERS</span></span>

### <span data-ttu-id="31c24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c24-111">-DefaultProfile</span></span>
<span data-ttu-id="31c24-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31c24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31c24-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="31c24-113">-JobName</span></span>
<span data-ttu-id="31c24-114">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics-átalakítás tartozik.</span><span class="sxs-lookup"><span data-stu-id="31c24-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="31c24-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31c24-115">-Name</span></span>
<span data-ttu-id="31c24-116">A lekérni szükséges Azure Stream Analytics-átalakítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31c24-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="31c24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c24-117">-ResourceGroupName</span></span>
<span data-ttu-id="31c24-118">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics-átalakítás tartozik.</span><span class="sxs-lookup"><span data-stu-id="31c24-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="31c24-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c24-119">CommonParameters</span></span>
<span data-ttu-id="31c24-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c24-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c24-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c24-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c24-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31c24-122">INPUTS</span></span>

### <span data-ttu-id="31c24-123">System.String</span><span class="sxs-lookup"><span data-stu-id="31c24-123">System.String</span></span>

## <span data-ttu-id="31c24-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31c24-124">OUTPUTS</span></span>

### <span data-ttu-id="31c24-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="31c24-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="31c24-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31c24-126">NOTES</span></span>

## <span data-ttu-id="31c24-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31c24-127">RELATED LINKS</span></span>

[<span data-ttu-id="31c24-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="31c24-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


