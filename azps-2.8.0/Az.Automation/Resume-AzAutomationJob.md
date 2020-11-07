---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 6315ba9079729779a7db872a87237e1b664837c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667744"
---
# <span data-ttu-id="22ab2-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="22ab2-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="22ab2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="22ab2-103">Befejezi a felfüggesztett automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="22ab2-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="22ab2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22ab2-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ab2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="22ab2-106">A **resume-AzAutomationJob** parancsmag felfüggesztette az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="22ab2-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="22ab2-107">Adja meg a felfüggesztett feladatot.</span><span class="sxs-lookup"><span data-stu-id="22ab2-107">Specify the suspended job.</span></span>
<span data-ttu-id="22ab2-108">A feladat felfüggesztéséhez használja az Suspend-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22ab2-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="22ab2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="22ab2-109">EXAMPLES</span></span>

### <span data-ttu-id="22ab2-110">1. példa: felfüggesztett feladat folytatása</span><span class="sxs-lookup"><span data-stu-id="22ab2-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="22ab2-111">Ez a parancs folytatja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="22ab2-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="22ab2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22ab2-112">PARAMETERS</span></span>

### <span data-ttu-id="22ab2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22ab2-113">-AutomationAccountName</span></span>
<span data-ttu-id="22ab2-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag folytatja a munkát.</span><span class="sxs-lookup"><span data-stu-id="22ab2-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="22ab2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ab2-115">-DefaultProfile</span></span>
<span data-ttu-id="22ab2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22ab2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22ab2-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="22ab2-117">-Id</span></span>
<span data-ttu-id="22ab2-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag visszatér.</span><span class="sxs-lookup"><span data-stu-id="22ab2-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="22ab2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ab2-119">-ResourceGroupName</span></span>
<span data-ttu-id="22ab2-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag folytatja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="22ab2-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="22ab2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ab2-121">CommonParameters</span></span>
<span data-ttu-id="22ab2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22ab2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ab2-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ab2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ab2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22ab2-124">INPUTS</span></span>

### <span data-ttu-id="22ab2-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="22ab2-125">System.Guid</span></span>

### <span data-ttu-id="22ab2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="22ab2-126">System.String</span></span>

## <span data-ttu-id="22ab2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22ab2-127">OUTPUTS</span></span>

### <span data-ttu-id="22ab2-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="22ab2-128">System.Void</span></span>

## <span data-ttu-id="22ab2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22ab2-129">NOTES</span></span>

## <span data-ttu-id="22ab2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22ab2-130">RELATED LINKS</span></span>

[<span data-ttu-id="22ab2-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="22ab2-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="22ab2-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="22ab2-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="22ab2-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="22ab2-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="22ab2-134">Felfüggesztés – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="22ab2-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


