---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 98074a9893525882ce63ab86e31c677281f34ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492696"
---
# <span data-ttu-id="43013-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="43013-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="43013-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43013-102">SYNOPSIS</span></span>
<span data-ttu-id="43013-103">Az adatfolyam-elemzésből származó adatok kimenetének törlése.</span><span class="sxs-lookup"><span data-stu-id="43013-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43013-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43013-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43013-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43013-105">DESCRIPTION</span></span>
<span data-ttu-id="43013-106">A **Remove-AzureRmStreamAnalyticsOutput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési feladatok kimenetét.</span><span class="sxs-lookup"><span data-stu-id="43013-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="43013-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43013-107">EXAMPLES</span></span>

### <span data-ttu-id="43013-108">1. példa: a kimenet eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="43013-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="43013-109">Ez a parancs eltávolítja a kimeneti kimenetet a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="43013-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="43013-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43013-110">PARAMETERS</span></span>

### <span data-ttu-id="43013-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43013-111">-DefaultProfile</span></span>
<span data-ttu-id="43013-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43013-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43013-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="43013-113">-JobName</span></span>
<span data-ttu-id="43013-114">Annak az Azure stream-Analytics-feladatnak a neve, amelyhez az Azure stream Analytics kimenete tartozik.</span><span class="sxs-lookup"><span data-stu-id="43013-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="43013-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43013-115">-Name</span></span>
<span data-ttu-id="43013-116">Itt adhatja meg az Azure stream Analytics által eltávolítandó kimenet nevét.</span><span class="sxs-lookup"><span data-stu-id="43013-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="43013-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43013-117">-ResourceGroupName</span></span>
<span data-ttu-id="43013-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="43013-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="43013-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43013-119">-Confirm</span></span>
<span data-ttu-id="43013-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43013-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43013-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43013-121">-WhatIf</span></span>
<span data-ttu-id="43013-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43013-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43013-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43013-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43013-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43013-124">CommonParameters</span></span>
<span data-ttu-id="43013-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43013-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43013-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43013-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43013-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43013-127">INPUTS</span></span>

### <span data-ttu-id="43013-128">System. String</span><span class="sxs-lookup"><span data-stu-id="43013-128">System.String</span></span>

## <span data-ttu-id="43013-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43013-129">OUTPUTS</span></span>

### <span data-ttu-id="43013-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43013-130">System.Boolean</span></span>

## <span data-ttu-id="43013-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43013-131">NOTES</span></span>

## <span data-ttu-id="43013-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43013-132">RELATED LINKS</span></span>

[<span data-ttu-id="43013-133">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="43013-133">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="43013-134">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="43013-134">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="43013-135">Teszt-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="43013-135">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


