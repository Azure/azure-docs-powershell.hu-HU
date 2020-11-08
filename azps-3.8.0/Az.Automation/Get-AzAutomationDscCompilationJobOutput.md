---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012705"
---
# <span data-ttu-id="735cf-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="735cf-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="735cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="735cf-102">SYNOPSIS</span></span>
<span data-ttu-id="735cf-103">Egy automatizálási DSC összeállítási feladat naplózási folyamait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="735cf-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="735cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="735cf-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="735cf-105">DESCRIPTION</span></span>
<span data-ttu-id="735cf-106">A **Get-AzAutomationDscCompilationJobOutput** PARANCSMAG a APS-alapú szükséges állapot-konfiguráció (DSC) fordítási feladatának stream-rekordjait kapja meg az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="735cf-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="735cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="735cf-107">EXAMPLES</span></span>

### <span data-ttu-id="735cf-108">Példa 1: a DSC-összeállítási feladathoz tartozó naplók beszerzése</span><span class="sxs-lookup"><span data-stu-id="735cf-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="735cf-109">Az első parancs a fordítási feladatokat a Contoso17 nevű automatizálási fiókból kapja meg az Get-AzAutomationDscCompilationJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="735cf-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="735cf-110">A parancs ezeket az objektumokat a $Jobs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="735cf-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="735cf-111">A második parancs beolvassa a fordítási munka kimenetét a $Jobs tömb első tagjának minden adatfolyamhoz.</span><span class="sxs-lookup"><span data-stu-id="735cf-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="735cf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="735cf-112">PARAMETERS</span></span>

### <span data-ttu-id="735cf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="735cf-113">-AutomationAccountName</span></span>
<span data-ttu-id="735cf-114">A DSC összeállítási feladatot tartalmazó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="735cf-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="735cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735cf-115">-DefaultProfile</span></span>
<span data-ttu-id="735cf-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="735cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="735cf-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="735cf-117">-Id</span></span>
<span data-ttu-id="735cf-118">Megadja annak a DSC-összeállításnak az egyedi AZONOSÍTÓját, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="735cf-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="735cf-120">Annak a DSC-összeállítási feladatot tartalmazó erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag adatfolyam-nyilvántartást kap.</span><span class="sxs-lookup"><span data-stu-id="735cf-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="735cf-121">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="735cf-121">-StartTime</span></span>
<span data-ttu-id="735cf-122">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="735cf-122">Specifies a start time.</span></span>
<span data-ttu-id="735cf-123">Ez a parancsmag olyan adatfolyam-rekordokat kap, amelyekben a DSC fordítási feladat az adott időpont után kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="735cf-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735cf-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="735cf-124">-Stream</span></span>
<span data-ttu-id="735cf-125">Annak a kimenetnek az adatfolyam-típusát adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="735cf-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="735cf-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="735cf-126">Valid values are:</span></span> 
- <span data-ttu-id="735cf-127">Bármely</span><span class="sxs-lookup"><span data-stu-id="735cf-127">Any</span></span> 
- <span data-ttu-id="735cf-128">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="735cf-128">Warning</span></span> 
- <span data-ttu-id="735cf-129">Hiba</span><span class="sxs-lookup"><span data-stu-id="735cf-129">Error</span></span> 
- <span data-ttu-id="735cf-130">Részletes</span><span class="sxs-lookup"><span data-stu-id="735cf-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735cf-131">CommonParameters</span></span>
<span data-ttu-id="735cf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="735cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735cf-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735cf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735cf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="735cf-134">INPUTS</span></span>

### <span data-ttu-id="735cf-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="735cf-135">System.Guid</span></span>

### <span data-ttu-id="735cf-136">Microsoft. Azure. Command. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="735cf-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="735cf-137">System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="735cf-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="735cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="735cf-138">System.String</span></span>

## <span data-ttu-id="735cf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="735cf-139">OUTPUTS</span></span>

### <span data-ttu-id="735cf-140">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="735cf-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="735cf-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="735cf-141">NOTES</span></span>

## <span data-ttu-id="735cf-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="735cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="735cf-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="735cf-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="735cf-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="735cf-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


