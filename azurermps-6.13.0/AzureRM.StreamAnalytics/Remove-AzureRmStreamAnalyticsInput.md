---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497208"
---
# <span data-ttu-id="5ef57-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ef57-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="5ef57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ef57-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef57-103">Az adatfolyam-elemzési feladatokből származó adatok törlése</span><span class="sxs-lookup"><span data-stu-id="5ef57-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ef57-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ef57-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef57-106">A **Remove-AzureRmStreamAnalyticsInput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési munkákból származó adatokat.</span><span class="sxs-lookup"><span data-stu-id="5ef57-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5ef57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ef57-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef57-108">1. példa: bemeneti adatfolyam eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="5ef57-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="5ef57-109">Ez a parancs eltávolítja a beviteli EventStream a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5ef57-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="5ef57-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ef57-110">PARAMETERS</span></span>

### <span data-ttu-id="5ef57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef57-111">-DefaultProfile</span></span>
<span data-ttu-id="5ef57-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ef57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef57-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="5ef57-113">-JobName</span></span>
<span data-ttu-id="5ef57-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="5ef57-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5ef57-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ef57-115">-Name</span></span>
<span data-ttu-id="5ef57-116">Itt adhatja meg az Azure stream Analytics által eltávolítandó adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="5ef57-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="5ef57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef57-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ef57-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="5ef57-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5ef57-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ef57-119">-Confirm</span></span>
<span data-ttu-id="5ef57-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ef57-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef57-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef57-121">-WhatIf</span></span>
<span data-ttu-id="5ef57-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ef57-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef57-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ef57-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef57-124">CommonParameters</span></span>
<span data-ttu-id="5ef57-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ef57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef57-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef57-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef57-127">INPUTS</span></span>

### <span data-ttu-id="5ef57-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5ef57-128">System.String</span></span>

## <span data-ttu-id="5ef57-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef57-129">OUTPUTS</span></span>

### <span data-ttu-id="5ef57-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ef57-130">System.Boolean</span></span>

## <span data-ttu-id="5ef57-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ef57-131">NOTES</span></span>

## <span data-ttu-id="5ef57-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ef57-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ef57-133">Új – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ef57-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5ef57-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ef57-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5ef57-135">Teszt-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ef57-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


