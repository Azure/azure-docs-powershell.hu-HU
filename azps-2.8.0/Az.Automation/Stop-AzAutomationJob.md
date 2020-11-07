---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 9559a599a6d0a50078dbec176ad937947facce7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667717"
---
# <span data-ttu-id="a40ab-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a40ab-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="a40ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a40ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a40ab-103">Automatizálási feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="a40ab-103">Stops an Automation job.</span></span>

## <span data-ttu-id="a40ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a40ab-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a40ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a40ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a40ab-106">A **stop-AzAutomationJob** parancsmag leállítja az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="a40ab-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="a40ab-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="a40ab-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="a40ab-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a40ab-108">EXAMPLES</span></span>

### <span data-ttu-id="a40ab-109">Példa 1: feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="a40ab-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a40ab-110">Ez a parancs leállítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="a40ab-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="a40ab-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a40ab-111">PARAMETERS</span></span>

### <span data-ttu-id="a40ab-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a40ab-112">-AutomationAccountName</span></span>
<span data-ttu-id="a40ab-113">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a40ab-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="a40ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40ab-114">-DefaultProfile</span></span>
<span data-ttu-id="a40ab-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a40ab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a40ab-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a40ab-116">-Id</span></span>
<span data-ttu-id="a40ab-117">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="a40ab-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a40ab-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40ab-118">-ResourceGroupName</span></span>
<span data-ttu-id="a40ab-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a40ab-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a40ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40ab-120">CommonParameters</span></span>
<span data-ttu-id="a40ab-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a40ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40ab-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40ab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40ab-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a40ab-123">INPUTS</span></span>

### <span data-ttu-id="a40ab-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a40ab-124">System.Guid</span></span>

### <span data-ttu-id="a40ab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a40ab-125">System.String</span></span>

## <span data-ttu-id="a40ab-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a40ab-126">OUTPUTS</span></span>

### <span data-ttu-id="a40ab-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="a40ab-127">System.Void</span></span>

## <span data-ttu-id="a40ab-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a40ab-128">NOTES</span></span>

## <span data-ttu-id="a40ab-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a40ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="a40ab-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a40ab-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="a40ab-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a40ab-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="a40ab-132">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a40ab-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a40ab-133">Felfüggesztés – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a40ab-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


