---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025852"
---
# <span data-ttu-id="3a807-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3a807-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="3a807-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a807-102">SYNOPSIS</span></span>
<span data-ttu-id="3a807-103">Teszteli a kimenet kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="3a807-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="3a807-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a807-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a807-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a807-105">DESCRIPTION</span></span>
<span data-ttu-id="3a807-106">A **AzStreamAnalyticsOutput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat ki a kimenethez.</span><span class="sxs-lookup"><span data-stu-id="3a807-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="3a807-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a807-107">EXAMPLES</span></span>

### <span data-ttu-id="3a807-108">Példa 1: a kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="3a807-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="3a807-109">Ez a teszt a kimeneti kimenet kapcsolati állapotát teszteli a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3a807-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="3a807-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a807-110">PARAMETERS</span></span>

### <span data-ttu-id="3a807-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a807-111">-DefaultProfile</span></span>
<span data-ttu-id="3a807-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a807-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a807-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3a807-113">-JobName</span></span>
<span data-ttu-id="3a807-114">Annak az Azure stream-elemzési feladatnak a neve, amelyhez a kívánt Azure stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="3a807-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="3a807-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a807-115">-Name</span></span>
<span data-ttu-id="3a807-116">A teszthez az Azure stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a807-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="3a807-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a807-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a807-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="3a807-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="3a807-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a807-119">CommonParameters</span></span>
<span data-ttu-id="3a807-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a807-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a807-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a807-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a807-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a807-122">INPUTS</span></span>

### <span data-ttu-id="3a807-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3a807-123">System.String</span></span>

## <span data-ttu-id="3a807-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a807-124">OUTPUTS</span></span>

### <span data-ttu-id="3a807-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a807-125">System.Boolean</span></span>

## <span data-ttu-id="3a807-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a807-126">NOTES</span></span>

## <span data-ttu-id="3a807-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a807-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a807-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3a807-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="3a807-129">Új – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3a807-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="3a807-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3a807-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


