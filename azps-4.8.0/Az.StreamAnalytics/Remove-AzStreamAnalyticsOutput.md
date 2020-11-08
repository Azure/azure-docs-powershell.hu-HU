---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024280"
---
# <span data-ttu-id="c802a-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c802a-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c802a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c802a-102">SYNOPSIS</span></span>
<span data-ttu-id="c802a-103">Az adatfolyam-elemzésből származó adatok kimenetének törlése.</span><span class="sxs-lookup"><span data-stu-id="c802a-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="c802a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c802a-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c802a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c802a-105">DESCRIPTION</span></span>
<span data-ttu-id="c802a-106">A **Remove-AzStreamAnalyticsOutput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési feladatok kimenetét.</span><span class="sxs-lookup"><span data-stu-id="c802a-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="c802a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c802a-107">EXAMPLES</span></span>

### <span data-ttu-id="c802a-108">1. példa: a kimenet eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="c802a-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c802a-109">Ez a parancs eltávolítja a kimeneti kimenetet a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c802a-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="c802a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c802a-110">PARAMETERS</span></span>

### <span data-ttu-id="c802a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c802a-111">-DefaultProfile</span></span>
<span data-ttu-id="c802a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c802a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c802a-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="c802a-113">-JobName</span></span>
<span data-ttu-id="c802a-114">Annak az Azure stream-Analytics-feladatnak a neve, amelyhez az Azure stream Analytics kimenete tartozik.</span><span class="sxs-lookup"><span data-stu-id="c802a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c802a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c802a-115">-Name</span></span>
<span data-ttu-id="c802a-116">Itt adhatja meg az Azure stream Analytics által eltávolítandó kimenet nevét.</span><span class="sxs-lookup"><span data-stu-id="c802a-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="c802a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c802a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c802a-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="c802a-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c802a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c802a-119">-Confirm</span></span>
<span data-ttu-id="c802a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c802a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c802a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c802a-121">-WhatIf</span></span>
<span data-ttu-id="c802a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c802a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c802a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c802a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c802a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c802a-124">CommonParameters</span></span>
<span data-ttu-id="c802a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c802a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c802a-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c802a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c802a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c802a-127">INPUTS</span></span>

### <span data-ttu-id="c802a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c802a-128">System.String</span></span>

## <span data-ttu-id="c802a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c802a-129">OUTPUTS</span></span>

### <span data-ttu-id="c802a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c802a-130">System.Boolean</span></span>

## <span data-ttu-id="c802a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c802a-131">NOTES</span></span>

## <span data-ttu-id="c802a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c802a-132">RELATED LINKS</span></span>

[<span data-ttu-id="c802a-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c802a-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c802a-134">Új – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c802a-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c802a-135">Teszt-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c802a-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


