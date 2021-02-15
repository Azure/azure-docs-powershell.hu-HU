---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166834"
---
# <span data-ttu-id="8a19c-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8a19c-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="8a19c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a19c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a19c-103">Automatizálási feladat felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="8a19c-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="8a19c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a19c-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a19c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a19c-105">DESCRIPTION</span></span>
<span data-ttu-id="8a19c-106">A **Suspend-AzAutomation Automation parancsmag** felfüggeszti az Azure Automation-feladatot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="8a19c-107">Adjon meg futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-107">Specify a running Automation job.</span></span>
<span data-ttu-id="8a19c-108">A felfüggesztett feladat folytatásához használja a Resume-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="8a19c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a19c-109">EXAMPLES</span></span>

### <span data-ttu-id="8a19c-110">1. példa: Feladat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="8a19c-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8a19c-111">Ez a parancs felfüggeszti a megadott azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="8a19c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a19c-112">PARAMETERS</span></span>

### <span data-ttu-id="8a19c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8a19c-113">-AutomationAccountName</span></span>
<span data-ttu-id="8a19c-114">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="8a19c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a19c-115">-DefaultProfile</span></span>
<span data-ttu-id="8a19c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8a19c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a19c-117">-Id</span><span class="sxs-lookup"><span data-stu-id="8a19c-117">-Id</span></span>
<span data-ttu-id="8a19c-118">Annak a feladatnak az azonosítóját adja meg, amely felfüggeszti a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="8a19c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a19c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a19c-120">Annak a feladatnak az azonosítóját adja meg, amely felfüggeszti a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8a19c-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="8a19c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a19c-121">CommonParameters</span></span>
<span data-ttu-id="8a19c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a19c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a19c-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a19c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a19c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a19c-124">INPUTS</span></span>

### <span data-ttu-id="8a19c-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8a19c-125">System.Guid</span></span>

### <span data-ttu-id="8a19c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8a19c-126">System.String</span></span>

## <span data-ttu-id="8a19c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a19c-127">OUTPUTS</span></span>

### <span data-ttu-id="8a19c-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="8a19c-128">System.Void</span></span>

## <span data-ttu-id="8a19c-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a19c-129">NOTES</span></span>

## <span data-ttu-id="8a19c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a19c-130">RELATED LINKS</span></span>

[<span data-ttu-id="8a19c-131">Get-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="8a19c-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="8a19c-132">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="8a19c-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="8a19c-133">Resume-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="8a19c-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="8a19c-134">Stop-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="8a19c-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


