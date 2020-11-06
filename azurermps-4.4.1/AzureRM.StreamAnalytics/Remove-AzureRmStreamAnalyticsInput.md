---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503147"
---
# <span data-ttu-id="51de0-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="51de0-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="51de0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51de0-102">SYNOPSIS</span></span>
<span data-ttu-id="51de0-103">Az adatfolyam-elemzési feladatokből származó adatok törlése</span><span class="sxs-lookup"><span data-stu-id="51de0-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51de0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51de0-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51de0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51de0-105">DESCRIPTION</span></span>
<span data-ttu-id="51de0-106">A **Remove-AzureRmStreamAnalyticsInput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési munkákból származó adatokat.</span><span class="sxs-lookup"><span data-stu-id="51de0-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="51de0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51de0-107">EXAMPLES</span></span>

### <span data-ttu-id="51de0-108">1. példa: bemeneti adatfolyam eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="51de0-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="51de0-109">Ez a parancs eltávolítja a beviteli EventStream a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="51de0-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="51de0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51de0-110">PARAMETERS</span></span>

### <span data-ttu-id="51de0-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="51de0-111">-JobName</span></span>
<span data-ttu-id="51de0-112">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="51de0-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="51de0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51de0-113">-Name</span></span>
<span data-ttu-id="51de0-114">Itt adhatja meg az Azure stream Analytics által eltávolítandó adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="51de0-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="51de0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51de0-115">-ResourceGroupName</span></span>
<span data-ttu-id="51de0-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="51de0-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="51de0-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51de0-117">-Confirm</span></span>
<span data-ttu-id="51de0-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51de0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51de0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51de0-119">-WhatIf</span></span>
<span data-ttu-id="51de0-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51de0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51de0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51de0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51de0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51de0-122">-DefaultProfile</span></span>
<span data-ttu-id="51de0-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51de0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51de0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51de0-124">CommonParameters</span></span>
<span data-ttu-id="51de0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51de0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51de0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51de0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51de0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51de0-127">INPUTS</span></span>

## <span data-ttu-id="51de0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51de0-128">OUTPUTS</span></span>

### <span data-ttu-id="51de0-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="51de0-129">System.Object</span></span>

## <span data-ttu-id="51de0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51de0-130">NOTES</span></span>

## <span data-ttu-id="51de0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51de0-131">RELATED LINKS</span></span>

[<span data-ttu-id="51de0-132">Új – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="51de0-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="51de0-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="51de0-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="51de0-134">Teszt-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="51de0-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


