---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161970"
---
# <span data-ttu-id="96a27-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96a27-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="96a27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a27-102">SYNOPSIS</span></span>
<span data-ttu-id="96a27-103">Megszakít egy feladatot.</span><span class="sxs-lookup"><span data-stu-id="96a27-103">Cancels a job.</span></span>

## <span data-ttu-id="96a27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96a27-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96a27-105">DESCRIPTION</span></span>
<span data-ttu-id="96a27-106">A **Stop-AzDataLakeAnalytics Job** parancsmag megszakítja az Azure Data Lake Analytics-feladatot.</span><span class="sxs-lookup"><span data-stu-id="96a27-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="96a27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96a27-107">EXAMPLES</span></span>

### <span data-ttu-id="96a27-108">1. példa: Feladat lemondása</span><span class="sxs-lookup"><span data-stu-id="96a27-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="96a27-109">Ez a parancs megszakítja a feladatot a megadott azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="96a27-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="96a27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a27-110">PARAMETERS</span></span>

### <span data-ttu-id="96a27-111">-Account</span><span class="sxs-lookup"><span data-stu-id="96a27-111">-Account</span></span>
<span data-ttu-id="96a27-112">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96a27-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="96a27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a27-113">-DefaultProfile</span></span>
<span data-ttu-id="96a27-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="96a27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96a27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96a27-115">-Force</span></span>
<span data-ttu-id="96a27-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="96a27-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96a27-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="96a27-117">-JobId</span></span>
<span data-ttu-id="96a27-118">A megszakítható feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="96a27-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="96a27-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96a27-119">-PassThru</span></span>
<span data-ttu-id="96a27-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="96a27-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96a27-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="96a27-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96a27-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a27-122">-Confirm</span></span>
<span data-ttu-id="96a27-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96a27-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a27-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a27-124">-WhatIf</span></span>
<span data-ttu-id="96a27-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96a27-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a27-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96a27-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a27-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a27-127">CommonParameters</span></span>
<span data-ttu-id="96a27-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a27-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a27-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a27-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a27-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a27-130">INPUTS</span></span>

### <span data-ttu-id="96a27-131">System.String</span><span class="sxs-lookup"><span data-stu-id="96a27-131">System.String</span></span>

### <span data-ttu-id="96a27-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="96a27-132">System.Guid</span></span>

### <span data-ttu-id="96a27-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="96a27-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="96a27-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96a27-134">OUTPUTS</span></span>

### <span data-ttu-id="96a27-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96a27-135">System.Boolean</span></span>

## <span data-ttu-id="96a27-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96a27-136">NOTES</span></span>

## <span data-ttu-id="96a27-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96a27-137">RELATED LINKS</span></span>

[<span data-ttu-id="96a27-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96a27-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96a27-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96a27-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96a27-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96a27-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


