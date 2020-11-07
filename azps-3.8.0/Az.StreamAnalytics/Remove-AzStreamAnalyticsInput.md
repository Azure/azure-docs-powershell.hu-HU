---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846373"
---
# <span data-ttu-id="a4d83-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4d83-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="a4d83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4d83-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d83-103">Az adatfolyam-elemzési feladatokből származó adatok törlése</span><span class="sxs-lookup"><span data-stu-id="a4d83-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="a4d83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4d83-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d83-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4d83-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d83-106">A **Remove-AzStreamAnalyticsInput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési munkákból származó adatokat.</span><span class="sxs-lookup"><span data-stu-id="a4d83-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a4d83-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4d83-107">EXAMPLES</span></span>

### <span data-ttu-id="a4d83-108">1. példa: bemeneti adatfolyam eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="a4d83-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="a4d83-109">Ez a parancs eltávolítja a beviteli EventStream a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a4d83-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="a4d83-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4d83-110">PARAMETERS</span></span>

### <span data-ttu-id="a4d83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d83-111">-DefaultProfile</span></span>
<span data-ttu-id="a4d83-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4d83-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d83-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a4d83-113">-JobName</span></span>
<span data-ttu-id="a4d83-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="a4d83-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a4d83-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4d83-115">-Name</span></span>
<span data-ttu-id="a4d83-116">Itt adhatja meg az Azure stream Analytics által eltávolítandó adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="a4d83-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="a4d83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d83-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4d83-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="a4d83-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a4d83-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4d83-119">-Confirm</span></span>
<span data-ttu-id="a4d83-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4d83-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d83-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d83-121">-WhatIf</span></span>
<span data-ttu-id="a4d83-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4d83-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d83-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4d83-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d83-124">CommonParameters</span></span>
<span data-ttu-id="a4d83-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4d83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d83-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d83-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d83-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d83-127">INPUTS</span></span>

### <span data-ttu-id="a4d83-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d83-128">System.String</span></span>

## <span data-ttu-id="a4d83-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4d83-129">OUTPUTS</span></span>

### <span data-ttu-id="a4d83-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4d83-130">System.Boolean</span></span>

## <span data-ttu-id="a4d83-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4d83-131">NOTES</span></span>

## <span data-ttu-id="a4d83-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4d83-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4d83-133">Új – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4d83-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a4d83-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4d83-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a4d83-135">Teszt-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a4d83-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


