---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f8bd4feab9bdcf99daf713d3a584a574f699a8b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492695"
---
# <span data-ttu-id="aa7b3-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="aa7b3-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="aa7b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7b3-103">Teszteli a kimenet kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa7b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa7b3-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa7b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="aa7b3-106">A **AzureRmStreamAnalyticsOutput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat ki a kimenethez.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="aa7b3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa7b3-107">EXAMPLES</span></span>

### <span data-ttu-id="aa7b3-108">Példa 1: a kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="aa7b3-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="aa7b3-109">Ez a teszt a kimeneti kimenet kapcsolati állapotát teszteli a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="aa7b3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa7b3-110">PARAMETERS</span></span>

### <span data-ttu-id="aa7b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7b3-111">-DefaultProfile</span></span>
<span data-ttu-id="aa7b3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa7b3-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="aa7b3-113">-JobName</span></span>
<span data-ttu-id="aa7b3-114">Annak az Azure stream-elemzési feladatnak a neve, amelyhez a kívánt Azure stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="aa7b3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa7b3-115">-Name</span></span>
<span data-ttu-id="aa7b3-116">A teszthez az Azure stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="aa7b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa7b3-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="aa7b3-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="aa7b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7b3-119">CommonParameters</span></span>
<span data-ttu-id="aa7b3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa7b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7b3-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7b3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7b3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa7b3-122">INPUTS</span></span>

### <span data-ttu-id="aa7b3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7b3-123">System.String</span></span>

## <span data-ttu-id="aa7b3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa7b3-124">OUTPUTS</span></span>

### <span data-ttu-id="aa7b3-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa7b3-125">System.Boolean</span></span>

## <span data-ttu-id="aa7b3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa7b3-126">NOTES</span></span>

## <span data-ttu-id="aa7b3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa7b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="aa7b3-128">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="aa7b3-128">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="aa7b3-129">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="aa7b3-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="aa7b3-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="aa7b3-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


