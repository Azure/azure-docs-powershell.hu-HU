---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 850ff932bdae35bd21ab83c745b5da8c056d778d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671483"
---
# <span data-ttu-id="23de3-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="23de3-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="23de3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23de3-102">SYNOPSIS</span></span>
<span data-ttu-id="23de3-103">Egy automatizálási feladat felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="23de3-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="23de3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23de3-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23de3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23de3-105">DESCRIPTION</span></span>
<span data-ttu-id="23de3-106">A **felfüggesztés – AzAutomationJob** parancsmag felfüggeszti az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="23de3-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="23de3-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="23de3-107">Specify a running Automation job.</span></span>
<span data-ttu-id="23de3-108">Felfüggesztett feladat folytatásához használja az Resume-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23de3-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="23de3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23de3-109">EXAMPLES</span></span>

### <span data-ttu-id="23de3-110">1. példa: feladat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="23de3-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="23de3-111">Ez a parancs felfüggeszti a megadott azonosítót tartalmazó feladatot.</span><span class="sxs-lookup"><span data-stu-id="23de3-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="23de3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23de3-112">PARAMETERS</span></span>

### <span data-ttu-id="23de3-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23de3-113">-AutomationAccountName</span></span>
<span data-ttu-id="23de3-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="23de3-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="23de3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23de3-115">-DefaultProfile</span></span>
<span data-ttu-id="23de3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23de3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23de3-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="23de3-117">-Id</span></span>
<span data-ttu-id="23de3-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="23de3-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="23de3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23de3-119">-ResourceGroupName</span></span>
<span data-ttu-id="23de3-120">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="23de3-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="23de3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23de3-121">CommonParameters</span></span>
<span data-ttu-id="23de3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23de3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23de3-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23de3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23de3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23de3-124">INPUTS</span></span>

### <span data-ttu-id="23de3-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="23de3-125">System.Guid</span></span>

### <span data-ttu-id="23de3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23de3-126">System.String</span></span>

## <span data-ttu-id="23de3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23de3-127">OUTPUTS</span></span>

### <span data-ttu-id="23de3-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="23de3-128">System.Void</span></span>

## <span data-ttu-id="23de3-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23de3-129">NOTES</span></span>

## <span data-ttu-id="23de3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23de3-130">RELATED LINKS</span></span>

[<span data-ttu-id="23de3-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="23de3-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="23de3-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="23de3-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="23de3-133">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="23de3-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="23de3-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="23de3-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


