---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210183"
---
# <span data-ttu-id="996b9-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="996b9-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="996b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="996b9-102">SYNOPSIS</span></span>
<span data-ttu-id="996b9-103">Leállít egy automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="996b9-103">Stops an Automation job.</span></span>

## <span data-ttu-id="996b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="996b9-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="996b9-105">DESCRIPTION</span></span>
<span data-ttu-id="996b9-106">A **Stop-AzAutomation Automation parancsmag** leállít egy Azure Automation-feladatot.</span><span class="sxs-lookup"><span data-stu-id="996b9-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="996b9-107">Adjon meg futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="996b9-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="996b9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="996b9-108">EXAMPLES</span></span>

### <span data-ttu-id="996b9-109">1. példa: Feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="996b9-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="996b9-110">Ez a parancs leállítja a megadott azonosítójú feladatot.</span><span class="sxs-lookup"><span data-stu-id="996b9-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="996b9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="996b9-111">PARAMETERS</span></span>

### <span data-ttu-id="996b9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="996b9-112">-AutomationAccountName</span></span>
<span data-ttu-id="996b9-113">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="996b9-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="996b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996b9-114">-DefaultProfile</span></span>
<span data-ttu-id="996b9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="996b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="996b9-116">-Id</span><span class="sxs-lookup"><span data-stu-id="996b9-116">-Id</span></span>
<span data-ttu-id="996b9-117">Annak a feladatnak az azonosítóját adja meg, amely leállítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="996b9-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="996b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="996b9-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="996b9-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="996b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996b9-120">CommonParameters</span></span>
<span data-ttu-id="996b9-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996b9-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996b9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996b9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="996b9-123">INPUTS</span></span>

### <span data-ttu-id="996b9-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="996b9-124">System.Guid</span></span>

### <span data-ttu-id="996b9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="996b9-125">System.String</span></span>

## <span data-ttu-id="996b9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="996b9-126">OUTPUTS</span></span>

### <span data-ttu-id="996b9-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="996b9-127">System.Void</span></span>

## <span data-ttu-id="996b9-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="996b9-128">NOTES</span></span>

## <span data-ttu-id="996b9-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="996b9-129">RELATED LINKS</span></span>

[<span data-ttu-id="996b9-130">Get-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="996b9-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="996b9-131">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="996b9-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="996b9-132">Resume-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="996b9-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="996b9-133">Suspend-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="996b9-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


