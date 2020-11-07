---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672183"
---
# <span data-ttu-id="fd528-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fd528-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="fd528-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd528-102">SYNOPSIS</span></span>
<span data-ttu-id="fd528-103">Az adatfolyam-elemzésből származó adatok kimenetének törlése.</span><span class="sxs-lookup"><span data-stu-id="fd528-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd528-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd528-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd528-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd528-105">DESCRIPTION</span></span>
<span data-ttu-id="fd528-106">A **Remove-AzureRmStreamAnalyticsOutput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési feladatok kimenetét.</span><span class="sxs-lookup"><span data-stu-id="fd528-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="fd528-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd528-107">EXAMPLES</span></span>

### <span data-ttu-id="fd528-108">1. példa: a kimenet eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="fd528-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="fd528-109">Ez a parancs eltávolítja a kimeneti kimenetet a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="fd528-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="fd528-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd528-110">PARAMETERS</span></span>

### <span data-ttu-id="fd528-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="fd528-111">-JobName</span></span>
<span data-ttu-id="fd528-112">Annak az Azure stream-Analytics-feladatnak a neve, amelyhez az Azure stream Analytics kimenete tartozik.</span><span class="sxs-lookup"><span data-stu-id="fd528-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="fd528-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd528-113">-Name</span></span>
<span data-ttu-id="fd528-114">Itt adhatja meg az Azure stream Analytics által eltávolítandó kimenet nevét.</span><span class="sxs-lookup"><span data-stu-id="fd528-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="fd528-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd528-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd528-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="fd528-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="fd528-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd528-117">-Confirm</span></span>
<span data-ttu-id="fd528-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd528-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd528-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd528-119">-WhatIf</span></span>
<span data-ttu-id="fd528-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd528-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd528-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd528-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd528-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd528-122">-DefaultProfile</span></span>
<span data-ttu-id="fd528-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd528-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd528-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd528-124">CommonParameters</span></span>
<span data-ttu-id="fd528-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd528-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd528-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd528-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd528-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd528-127">INPUTS</span></span>

## <span data-ttu-id="fd528-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd528-128">OUTPUTS</span></span>

### <span data-ttu-id="fd528-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fd528-129">System.Object</span></span>

## <span data-ttu-id="fd528-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd528-130">NOTES</span></span>

## <span data-ttu-id="fd528-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd528-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd528-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fd528-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="fd528-133">Új – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fd528-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="fd528-134">Teszt-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fd528-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


