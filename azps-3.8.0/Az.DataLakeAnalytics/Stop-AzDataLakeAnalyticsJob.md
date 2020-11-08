---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010593"
---
# <span data-ttu-id="690d1-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="690d1-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="690d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="690d1-102">SYNOPSIS</span></span>
<span data-ttu-id="690d1-103">Feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="690d1-103">Cancels a job.</span></span>

## <span data-ttu-id="690d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="690d1-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="690d1-105">DESCRIPTION</span></span>
<span data-ttu-id="690d1-106">A **stop-AzDataLakeAnalyticsJob** parancsmag visszamondja az Azure Data-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="690d1-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="690d1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="690d1-107">EXAMPLES</span></span>

### <span data-ttu-id="690d1-108">Példa 1: feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="690d1-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="690d1-109">Ez a parancs lemondja a feladatot a megadott AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="690d1-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="690d1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="690d1-110">PARAMETERS</span></span>

### <span data-ttu-id="690d1-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="690d1-111">-Account</span></span>
<span data-ttu-id="690d1-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="690d1-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690d1-113">-DefaultProfile</span></span>
<span data-ttu-id="690d1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="690d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="690d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="690d1-115">-Force</span></span>
<span data-ttu-id="690d1-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="690d1-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690d1-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="690d1-117">-JobId</span></span>
<span data-ttu-id="690d1-118">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="690d1-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="690d1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="690d1-119">-PassThru</span></span>
<span data-ttu-id="690d1-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="690d1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="690d1-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="690d1-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690d1-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="690d1-122">-Confirm</span></span>
<span data-ttu-id="690d1-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="690d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690d1-124">-WhatIf</span></span>
<span data-ttu-id="690d1-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="690d1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="690d1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="690d1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="690d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690d1-127">CommonParameters</span></span>
<span data-ttu-id="690d1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="690d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690d1-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690d1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690d1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="690d1-130">INPUTS</span></span>

### <span data-ttu-id="690d1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="690d1-131">System.String</span></span>

### <span data-ttu-id="690d1-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="690d1-132">System.Guid</span></span>

### <span data-ttu-id="690d1-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="690d1-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="690d1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="690d1-134">OUTPUTS</span></span>

### <span data-ttu-id="690d1-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="690d1-135">System.Boolean</span></span>

## <span data-ttu-id="690d1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="690d1-136">NOTES</span></span>

## <span data-ttu-id="690d1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="690d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="690d1-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="690d1-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="690d1-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="690d1-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="690d1-140">Várjon-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="690d1-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


