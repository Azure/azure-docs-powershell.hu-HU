---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194941"
---
# <span data-ttu-id="f5603-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5603-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="f5603-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5603-102">SYNOPSIS</span></span>
<span data-ttu-id="f5603-103">Egy automatizálási feladat felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="f5603-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="f5603-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5603-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5603-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5603-105">DESCRIPTION</span></span>
<span data-ttu-id="f5603-106">A **felfüggesztés – AzAutomationJob** parancsmag felfüggeszti az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="f5603-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="f5603-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="f5603-107">Specify a running Automation job.</span></span>
<span data-ttu-id="f5603-108">Felfüggesztett feladat folytatásához használja az Resume-AzAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f5603-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="f5603-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5603-109">EXAMPLES</span></span>

### <span data-ttu-id="f5603-110">1. példa: feladat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="f5603-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f5603-111">Ez a parancs felfüggeszti a megadott azonosítót tartalmazó feladatot.</span><span class="sxs-lookup"><span data-stu-id="f5603-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="f5603-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5603-112">PARAMETERS</span></span>

### <span data-ttu-id="f5603-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5603-113">-AutomationAccountName</span></span>
<span data-ttu-id="f5603-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f5603-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="f5603-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5603-115">-DefaultProfile</span></span>
<span data-ttu-id="f5603-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5603-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5603-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f5603-117">-Id</span></span>
<span data-ttu-id="f5603-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="f5603-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="f5603-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5603-119">-ResourceGroupName</span></span>
<span data-ttu-id="f5603-120">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="f5603-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="f5603-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5603-121">CommonParameters</span></span>
<span data-ttu-id="f5603-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5603-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5603-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5603-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5603-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5603-124">INPUTS</span></span>

### <span data-ttu-id="f5603-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f5603-125">System.Guid</span></span>

### <span data-ttu-id="f5603-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f5603-126">System.String</span></span>

## <span data-ttu-id="f5603-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5603-127">OUTPUTS</span></span>

### <span data-ttu-id="f5603-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="f5603-128">System.Void</span></span>

## <span data-ttu-id="f5603-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5603-129">NOTES</span></span>

## <span data-ttu-id="f5603-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5603-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5603-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5603-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="f5603-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f5603-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="f5603-133">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5603-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="f5603-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f5603-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

