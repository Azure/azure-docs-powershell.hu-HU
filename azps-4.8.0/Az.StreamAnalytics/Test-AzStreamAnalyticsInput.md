---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025855"
---
# <span data-ttu-id="97fbf-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="97fbf-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="97fbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="97fbf-103">Egy bemenet kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="97fbf-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="97fbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97fbf-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97fbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="97fbf-106">A **AzStreamAnalyticsInput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat egy bemenethez.</span><span class="sxs-lookup"><span data-stu-id="97fbf-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="97fbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97fbf-107">EXAMPLES</span></span>

### <span data-ttu-id="97fbf-108">Példa 1: egy bemeneti adatfolyam kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="97fbf-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="97fbf-109">Ez teszteli a StreamingJob bemeneti EntryStream kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="97fbf-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="97fbf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97fbf-110">PARAMETERS</span></span>

### <span data-ttu-id="97fbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fbf-111">-DefaultProfile</span></span>
<span data-ttu-id="97fbf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97fbf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97fbf-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="97fbf-113">-JobName</span></span>
<span data-ttu-id="97fbf-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="97fbf-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="97fbf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97fbf-115">-Name</span></span>
<span data-ttu-id="97fbf-116">A teszthez az Azure stream Analytics bemenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97fbf-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="97fbf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97fbf-117">-ResourceGroupName</span></span>
<span data-ttu-id="97fbf-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="97fbf-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="97fbf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fbf-119">CommonParameters</span></span>
<span data-ttu-id="97fbf-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97fbf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fbf-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fbf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fbf-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97fbf-122">INPUTS</span></span>

### <span data-ttu-id="97fbf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="97fbf-123">System.String</span></span>

## <span data-ttu-id="97fbf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97fbf-124">OUTPUTS</span></span>

### <span data-ttu-id="97fbf-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97fbf-125">System.Boolean</span></span>

## <span data-ttu-id="97fbf-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97fbf-126">NOTES</span></span>

## <span data-ttu-id="97fbf-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97fbf-127">RELATED LINKS</span></span>

[<span data-ttu-id="97fbf-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="97fbf-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="97fbf-129">Új – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="97fbf-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="97fbf-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="97fbf-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


