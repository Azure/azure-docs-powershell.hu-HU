---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492968"
---
# <span data-ttu-id="eae6d-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eae6d-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="eae6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eae6d-102">SYNOPSIS</span></span>
<span data-ttu-id="eae6d-103">Egy bemenet kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="eae6d-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eae6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eae6d-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eae6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eae6d-105">DESCRIPTION</span></span>
<span data-ttu-id="eae6d-106">A **AzureRmStreamAnalyticsInput** parancsmag segítségével az adatfolyam-elemzés segítségével kapcsolódhat egy bemenethez.</span><span class="sxs-lookup"><span data-stu-id="eae6d-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="eae6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eae6d-107">EXAMPLES</span></span>

### <span data-ttu-id="eae6d-108">Példa 1: egy bemeneti adatfolyam kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="eae6d-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="eae6d-109">Ez teszteli a StreamingJob bemeneti EntryStream kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="eae6d-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="eae6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eae6d-110">PARAMETERS</span></span>

### <span data-ttu-id="eae6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae6d-111">-DefaultProfile</span></span>
<span data-ttu-id="eae6d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eae6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eae6d-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="eae6d-113">-JobName</span></span>
<span data-ttu-id="eae6d-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="eae6d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="eae6d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eae6d-115">-Name</span></span>
<span data-ttu-id="eae6d-116">A teszthez az Azure stream Analytics bemenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eae6d-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="eae6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="eae6d-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="eae6d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="eae6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae6d-119">CommonParameters</span></span>
<span data-ttu-id="eae6d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eae6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae6d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eae6d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae6d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eae6d-122">INPUTS</span></span>

### <span data-ttu-id="eae6d-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="eae6d-123">None</span></span>
<span data-ttu-id="eae6d-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="eae6d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eae6d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eae6d-125">OUTPUTS</span></span>

### <span data-ttu-id="eae6d-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="eae6d-126">System.Object</span></span>

## <span data-ttu-id="eae6d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eae6d-127">NOTES</span></span>

## <span data-ttu-id="eae6d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eae6d-128">RELATED LINKS</span></span>

[<span data-ttu-id="eae6d-129">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eae6d-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="eae6d-130">Új – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eae6d-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="eae6d-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eae6d-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


