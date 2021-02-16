---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145202"
---
# <span data-ttu-id="71dd1-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="71dd1-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="71dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="71dd1-103">Felfüggesztett automatizálási feladat folytatása.</span><span class="sxs-lookup"><span data-stu-id="71dd1-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="71dd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71dd1-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71dd1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="71dd1-106">A **Resume-AzAutomation Automation parancsmag** egy felfüggesztett Azure Automation-feladatot folytat.</span><span class="sxs-lookup"><span data-stu-id="71dd1-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="71dd1-107">Adja meg a felfüggesztett feladatot.</span><span class="sxs-lookup"><span data-stu-id="71dd1-107">Specify the suspended job.</span></span>
<span data-ttu-id="71dd1-108">A feladat felfüggesztéséhez használja a Suspend-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="71dd1-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="71dd1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="71dd1-110">1. példa: Felfüggesztett feladat folytatása</span><span class="sxs-lookup"><span data-stu-id="71dd1-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71dd1-111">Ez a parancs folytatja a megadott azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="71dd1-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="71dd1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="71dd1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71dd1-113">-AutomationAccountName</span></span>
<span data-ttu-id="71dd1-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag folytatja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="71dd1-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="71dd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71dd1-115">-DefaultProfile</span></span>
<span data-ttu-id="71dd1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="71dd1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71dd1-117">-Id</span><span class="sxs-lookup"><span data-stu-id="71dd1-117">-Id</span></span>
<span data-ttu-id="71dd1-118">Annak a feladatnak az azonosítóját adja meg, amely a parancsmagot folytatja.</span><span class="sxs-lookup"><span data-stu-id="71dd1-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="71dd1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71dd1-119">-ResourceGroupName</span></span>
<span data-ttu-id="71dd1-120">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja folytatja a munkát.</span><span class="sxs-lookup"><span data-stu-id="71dd1-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="71dd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71dd1-121">CommonParameters</span></span>
<span data-ttu-id="71dd1-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71dd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71dd1-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71dd1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71dd1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71dd1-124">INPUTS</span></span>

### <span data-ttu-id="71dd1-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="71dd1-125">System.Guid</span></span>

### <span data-ttu-id="71dd1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="71dd1-126">System.String</span></span>

## <span data-ttu-id="71dd1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71dd1-127">OUTPUTS</span></span>

### <span data-ttu-id="71dd1-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="71dd1-128">System.Void</span></span>

## <span data-ttu-id="71dd1-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71dd1-129">NOTES</span></span>

## <span data-ttu-id="71dd1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71dd1-130">RELATED LINKS</span></span>

[<span data-ttu-id="71dd1-131">Get-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="71dd1-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="71dd1-132">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="71dd1-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="71dd1-133">Stop-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="71dd1-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="71dd1-134">Suspend-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="71dd1-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


