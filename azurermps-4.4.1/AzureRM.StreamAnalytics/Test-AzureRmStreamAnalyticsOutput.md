---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5c961289267b0680a88cd16d58574c906a9f4408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499923"
---
# <span data-ttu-id="375c2-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="375c2-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="375c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="375c2-102">SYNOPSIS</span></span>
<span data-ttu-id="375c2-103">Teszteli a kimenet kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="375c2-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="375c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="375c2-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="375c2-105">DESCRIPTION</span></span>
<span data-ttu-id="375c2-106">A **AzureRmStreamAnalyticsOutput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat ki a kimenethez.</span><span class="sxs-lookup"><span data-stu-id="375c2-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="375c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="375c2-107">EXAMPLES</span></span>

### <span data-ttu-id="375c2-108">Példa 1: a kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="375c2-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="375c2-109">Ez a teszt a kimeneti kimenet kapcsolati állapotát teszteli a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="375c2-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="375c2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="375c2-110">PARAMETERS</span></span>

### <span data-ttu-id="375c2-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="375c2-111">-JobName</span></span>
<span data-ttu-id="375c2-112">Annak az Azure stream-elemzési feladatnak a neve, amelyhez a kívánt Azure stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="375c2-112">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="375c2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="375c2-113">-Name</span></span>
<span data-ttu-id="375c2-114">A teszthez az Azure stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="375c2-114">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="375c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="375c2-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="375c2-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="375c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375c2-117">-DefaultProfile</span></span>
<span data-ttu-id="375c2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="375c2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375c2-119">CommonParameters</span></span>
<span data-ttu-id="375c2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="375c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375c2-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375c2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375c2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="375c2-122">INPUTS</span></span>

## <span data-ttu-id="375c2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="375c2-123">OUTPUTS</span></span>

### <span data-ttu-id="375c2-124">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="375c2-124">System.Object</span></span>

## <span data-ttu-id="375c2-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="375c2-125">NOTES</span></span>

## <span data-ttu-id="375c2-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="375c2-126">RELATED LINKS</span></span>

[<span data-ttu-id="375c2-127">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="375c2-127">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="375c2-128">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="375c2-128">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="375c2-129">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="375c2-129">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


