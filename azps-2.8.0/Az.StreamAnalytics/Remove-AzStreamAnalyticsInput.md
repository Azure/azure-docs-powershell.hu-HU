---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: fe6c78c0a4d1f4fa3ae9f7f917bdcffa49431575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839810"
---
# <span data-ttu-id="f9365-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f9365-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="f9365-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9365-102">SYNOPSIS</span></span>
<span data-ttu-id="f9365-103">Az adatfolyam-elemzési feladatokből származó adatok törlése</span><span class="sxs-lookup"><span data-stu-id="f9365-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="f9365-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9365-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9365-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9365-105">DESCRIPTION</span></span>
<span data-ttu-id="f9365-106">A **Remove-AzStreamAnalyticsInput** parancsmag aszinkron módon törli az Azure-ban az adatfolyam-elemzési munkákból származó adatokat.</span><span class="sxs-lookup"><span data-stu-id="f9365-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f9365-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9365-107">EXAMPLES</span></span>

### <span data-ttu-id="f9365-108">1. példa: bemeneti adatfolyam eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="f9365-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="f9365-109">Ez a parancs eltávolítja a beviteli EventStream a StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f9365-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="f9365-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9365-110">PARAMETERS</span></span>

### <span data-ttu-id="f9365-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9365-111">-DefaultProfile</span></span>
<span data-ttu-id="f9365-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9365-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9365-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="f9365-113">-JobName</span></span>
<span data-ttu-id="f9365-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="f9365-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f9365-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9365-115">-Name</span></span>
<span data-ttu-id="f9365-116">Itt adhatja meg az Azure stream Analytics által eltávolítandó adatok nevét.</span><span class="sxs-lookup"><span data-stu-id="f9365-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="f9365-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9365-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9365-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="f9365-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f9365-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9365-119">-Confirm</span></span>
<span data-ttu-id="f9365-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9365-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9365-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9365-121">-WhatIf</span></span>
<span data-ttu-id="f9365-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9365-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9365-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9365-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9365-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9365-124">CommonParameters</span></span>
<span data-ttu-id="f9365-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9365-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9365-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9365-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9365-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9365-127">INPUTS</span></span>

### <span data-ttu-id="f9365-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f9365-128">System.String</span></span>

## <span data-ttu-id="f9365-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9365-129">OUTPUTS</span></span>

### <span data-ttu-id="f9365-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9365-130">System.Boolean</span></span>

## <span data-ttu-id="f9365-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9365-131">NOTES</span></span>

## <span data-ttu-id="f9365-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9365-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9365-133">Új – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f9365-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f9365-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f9365-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f9365-135">Teszt-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f9365-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


