---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168435"
---
# <span data-ttu-id="d9ed4-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d9ed4-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="d9ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ed4-103">Az Automatizálási DSC fordítási feladat naplózási adatfolyamát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="d9ed4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9ed4-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ed4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ed4-106">A **Get-AzAutomationDscCompilationOutput** parancsmag az APS kívánt állapotkonfigurációs (DSC) összeállítási feladatának adatfolyam-rekordjait kapja meg az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="d9ed4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9ed4-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ed4-108">1. példa: A DSC összeállítási feladat naplóinak lekérte</span><span class="sxs-lookup"><span data-stu-id="d9ed4-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="d9ed4-109">Az első parancs a Contoso17 nevű automatizálási fiókban az összeállítási feladatokat a Get-AzAutomationDscCompilationJob parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="d9ed4-110">A parancs ezeket az objektumokat a $Jobs tárolja.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="d9ed4-111">A második parancs az összes adatfolyamhoz megkapja az összeállítási feladat kimenetét a $Jobs első tagja számára.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="d9ed4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ed4-112">PARAMETERS</span></span>

### <span data-ttu-id="d9ed4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9ed4-113">-AutomationAccountName</span></span>
<span data-ttu-id="d9ed4-114">Annak az automatizálási fióknak a nevét adja meg, amely a DSC fordítási feladatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="d9ed4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ed4-115">-DefaultProfile</span></span>
<span data-ttu-id="d9ed4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9ed4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9ed4-117">-Id</span><span class="sxs-lookup"><span data-stu-id="d9ed4-117">-Id</span></span>
<span data-ttu-id="d9ed4-118">Annak a DSC-fordítási feladatnak az egyedi azonosítóját adja meg, amelynek a parancsmagja kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="d9ed4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ed4-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9ed4-120">Annak az erőforráscsoportnak a nevét adja meg, amely azt a DSC-fordítási feladatot tartalmazza, amelyhez a parancsmag adatfolyam-rekordokat kap.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="d9ed4-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d9ed4-121">-StartTime</span></span>
<span data-ttu-id="d9ed4-122">Megadja a kezdési időt.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-122">Specifies a start time.</span></span>
<span data-ttu-id="d9ed4-123">Ez a parancsmag olyan adatfolyam-rekordokat kap, amelyek a DSC összeállítási feladat kimenetét ez idő után kapják meg.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="d9ed4-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="d9ed4-124">-Stream</span></span>
<span data-ttu-id="d9ed4-125">A parancsmag kimenetének adatfolyamtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="d9ed4-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="d9ed4-126">Valid values are:</span></span> 
- <span data-ttu-id="d9ed4-127">Bármely</span><span class="sxs-lookup"><span data-stu-id="d9ed4-127">Any</span></span> 
- <span data-ttu-id="d9ed4-128">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="d9ed4-128">Warning</span></span> 
- <span data-ttu-id="d9ed4-129">Hiba</span><span class="sxs-lookup"><span data-stu-id="d9ed4-129">Error</span></span> 
- <span data-ttu-id="d9ed4-130">Verbose</span><span class="sxs-lookup"><span data-stu-id="d9ed4-130">Verbose</span></span>

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

### <span data-ttu-id="d9ed4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ed4-131">CommonParameters</span></span>
<span data-ttu-id="d9ed4-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ed4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ed4-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ed4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ed4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9ed4-134">INPUTS</span></span>

### <span data-ttu-id="d9ed4-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d9ed4-135">System.Guid</span></span>

### <span data-ttu-id="d9ed4-136">Microsoft.Azure.Commands.Automation.Common.CompilationStreamType</span><span class="sxs-lookup"><span data-stu-id="d9ed4-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="d9ed4-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9ed4-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d9ed4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ed4-138">System.String</span></span>

## <span data-ttu-id="d9ed4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9ed4-139">OUTPUTS</span></span>

### <span data-ttu-id="d9ed4-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="d9ed4-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="d9ed4-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9ed4-141">NOTES</span></span>

## <span data-ttu-id="d9ed4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9ed4-142">RELATED LINKS</span></span>

[<span data-ttu-id="d9ed4-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d9ed4-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="d9ed4-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d9ed4-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


