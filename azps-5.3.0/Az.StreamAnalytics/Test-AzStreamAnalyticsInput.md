---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384242"
---
# <span data-ttu-id="567e8-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="567e8-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="567e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="567e8-102">SYNOPSIS</span></span>
<span data-ttu-id="567e8-103">Egy bevitel kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="567e8-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="567e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="567e8-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="567e8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="567e8-105">DESCRIPTION</span></span>
<span data-ttu-id="567e8-106">A **Test-AzStreamAnalyticsInput** parancsmag teszteli, hogy a Stream Analytics képes-e csatlakozni egy bemenethez.</span><span class="sxs-lookup"><span data-stu-id="567e8-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="567e8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="567e8-107">EXAMPLES</span></span>

### <span data-ttu-id="567e8-108">1. példa: Bemeneti adatfolyam kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="567e8-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="567e8-109">Ez teszteli az input EntryStream kapcsolati állapotát a StreamingStreamben.</span><span class="sxs-lookup"><span data-stu-id="567e8-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="567e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="567e8-110">PARAMETERS</span></span>

### <span data-ttu-id="567e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567e8-111">-DefaultProfile</span></span>
<span data-ttu-id="567e8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="567e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="567e8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="567e8-113">-JobName</span></span>
<span data-ttu-id="567e8-114">Annak az Azure Stream Analytics-feladatnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="567e8-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="567e8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="567e8-115">-Name</span></span>
<span data-ttu-id="567e8-116">Megadja a tesztelni szükséges Azure Stream Analytics-bemenet nevét.</span><span class="sxs-lookup"><span data-stu-id="567e8-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="567e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="567e8-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="567e8-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="567e8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567e8-119">CommonParameters</span></span>
<span data-ttu-id="567e8-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567e8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567e8-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="567e8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567e8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="567e8-122">INPUTS</span></span>

### <span data-ttu-id="567e8-123">System.String</span><span class="sxs-lookup"><span data-stu-id="567e8-123">System.String</span></span>

## <span data-ttu-id="567e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="567e8-124">OUTPUTS</span></span>

### <span data-ttu-id="567e8-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="567e8-125">System.Boolean</span></span>

## <span data-ttu-id="567e8-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="567e8-126">NOTES</span></span>

## <span data-ttu-id="567e8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="567e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="567e8-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="567e8-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="567e8-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="567e8-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="567e8-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="567e8-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


