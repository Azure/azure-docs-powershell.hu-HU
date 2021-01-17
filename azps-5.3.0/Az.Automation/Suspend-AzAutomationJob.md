---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478437"
---
# <span data-ttu-id="11016-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11016-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="11016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11016-102">SYNOPSIS</span></span>
<span data-ttu-id="11016-103">Automatizálási feladat felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="11016-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="11016-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11016-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11016-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11016-105">DESCRIPTION</span></span>
<span data-ttu-id="11016-106">A **Suspend-AzAutomation Automation parancsmag** felfüggeszti az Azure Automation-feladatot.</span><span class="sxs-lookup"><span data-stu-id="11016-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="11016-107">Adjon meg futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="11016-107">Specify a running Automation job.</span></span>
<span data-ttu-id="11016-108">A felfüggesztett feladat folytatásához használja a Resume-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11016-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="11016-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11016-109">EXAMPLES</span></span>

### <span data-ttu-id="11016-110">1. példa: Feladat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="11016-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="11016-111">Ez a parancs felfüggeszti a megadott azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="11016-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="11016-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11016-112">PARAMETERS</span></span>

### <span data-ttu-id="11016-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11016-113">-AutomationAccountName</span></span>
<span data-ttu-id="11016-114">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="11016-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="11016-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11016-115">-DefaultProfile</span></span>
<span data-ttu-id="11016-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11016-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11016-117">-Id</span><span class="sxs-lookup"><span data-stu-id="11016-117">-Id</span></span>
<span data-ttu-id="11016-118">Annak a feladatnak az azonosítóját adja meg, amely felfüggeszti a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11016-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="11016-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11016-119">-ResourceGroupName</span></span>
<span data-ttu-id="11016-120">Annak a feladatnak az azonosítóját adja meg, amely felfüggeszti a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11016-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="11016-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11016-121">CommonParameters</span></span>
<span data-ttu-id="11016-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11016-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11016-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11016-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11016-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11016-124">INPUTS</span></span>

### <span data-ttu-id="11016-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="11016-125">System.Guid</span></span>

### <span data-ttu-id="11016-126">System.String</span><span class="sxs-lookup"><span data-stu-id="11016-126">System.String</span></span>

## <span data-ttu-id="11016-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11016-127">OUTPUTS</span></span>

### <span data-ttu-id="11016-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="11016-128">System.Void</span></span>

## <span data-ttu-id="11016-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11016-129">NOTES</span></span>

## <span data-ttu-id="11016-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11016-130">RELATED LINKS</span></span>

[<span data-ttu-id="11016-131">Get-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="11016-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="11016-132">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="11016-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="11016-133">Resume-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="11016-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="11016-134">Stop-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="11016-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


