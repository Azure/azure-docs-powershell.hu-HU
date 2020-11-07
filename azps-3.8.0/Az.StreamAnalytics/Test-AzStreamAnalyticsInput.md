---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 0123392604b9ea0a6d75d70fcf4f2caaff159702
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846361"
---
# <span data-ttu-id="ae388-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ae388-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="ae388-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae388-102">SYNOPSIS</span></span>
<span data-ttu-id="ae388-103">Egy bemenet kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="ae388-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="ae388-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae388-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae388-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae388-105">DESCRIPTION</span></span>
<span data-ttu-id="ae388-106">A **AzStreamAnalyticsInput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat egy bemenethez.</span><span class="sxs-lookup"><span data-stu-id="ae388-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="ae388-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae388-107">EXAMPLES</span></span>

### <span data-ttu-id="ae388-108">Példa 1: egy bemeneti adatfolyam kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="ae388-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="ae388-109">Ez teszteli a StreamingJob bemeneti EntryStream kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="ae388-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="ae388-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae388-110">PARAMETERS</span></span>

### <span data-ttu-id="ae388-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae388-111">-DefaultProfile</span></span>
<span data-ttu-id="ae388-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae388-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae388-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="ae388-113">-JobName</span></span>
<span data-ttu-id="ae388-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae388-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ae388-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae388-115">-Name</span></span>
<span data-ttu-id="ae388-116">A teszthez az Azure stream Analytics bemenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae388-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="ae388-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae388-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae388-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae388-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ae388-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae388-119">CommonParameters</span></span>
<span data-ttu-id="ae388-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae388-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae388-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae388-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae388-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae388-122">INPUTS</span></span>

### <span data-ttu-id="ae388-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ae388-123">System.String</span></span>

## <span data-ttu-id="ae388-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae388-124">OUTPUTS</span></span>

### <span data-ttu-id="ae388-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae388-125">System.Boolean</span></span>

## <span data-ttu-id="ae388-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae388-126">NOTES</span></span>

## <span data-ttu-id="ae388-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae388-127">RELATED LINKS</span></span>

[<span data-ttu-id="ae388-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ae388-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ae388-129">Új – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ae388-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ae388-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ae388-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


