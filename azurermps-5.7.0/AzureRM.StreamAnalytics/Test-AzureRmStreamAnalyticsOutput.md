---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501316"
---
# <span data-ttu-id="4837c-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4837c-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="4837c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4837c-102">SYNOPSIS</span></span>
<span data-ttu-id="4837c-103">Teszteli a kimenet kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="4837c-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4837c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4837c-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4837c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4837c-105">DESCRIPTION</span></span>
<span data-ttu-id="4837c-106">A **AzureRmStreamAnalyticsOutput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat ki a kimenethez.</span><span class="sxs-lookup"><span data-stu-id="4837c-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="4837c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4837c-107">EXAMPLES</span></span>

### <span data-ttu-id="4837c-108">Példa 1: a kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="4837c-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="4837c-109">Ez a teszt a kimeneti kimenet kapcsolati állapotát teszteli a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="4837c-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="4837c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4837c-110">PARAMETERS</span></span>

### <span data-ttu-id="4837c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4837c-111">-DefaultProfile</span></span>
<span data-ttu-id="4837c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4837c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4837c-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="4837c-113">-JobName</span></span>
<span data-ttu-id="4837c-114">Annak az Azure stream-elemzési feladatnak a neve, amelyhez a kívánt Azure stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="4837c-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="4837c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4837c-115">-Name</span></span>
<span data-ttu-id="4837c-116">A teszthez az Azure stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4837c-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4837c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4837c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4837c-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="4837c-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="4837c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4837c-119">CommonParameters</span></span>
<span data-ttu-id="4837c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4837c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4837c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4837c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4837c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4837c-122">INPUTS</span></span>

### <span data-ttu-id="4837c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="4837c-123">None</span></span>
<span data-ttu-id="4837c-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4837c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4837c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4837c-125">OUTPUTS</span></span>

### <span data-ttu-id="4837c-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="4837c-126">System.Object</span></span>

## <span data-ttu-id="4837c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4837c-127">NOTES</span></span>

## <span data-ttu-id="4837c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4837c-128">RELATED LINKS</span></span>

[<span data-ttu-id="4837c-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4837c-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="4837c-130">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4837c-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="4837c-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4837c-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


