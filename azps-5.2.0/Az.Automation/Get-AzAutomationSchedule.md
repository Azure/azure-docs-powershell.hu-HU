---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373755"
---
# <span data-ttu-id="f042d-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f042d-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="f042d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f042d-102">SYNOPSIS</span></span>
<span data-ttu-id="f042d-103">Automatizálási ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="f042d-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="f042d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f042d-104">SYNTAX</span></span>

### <span data-ttu-id="f042d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f042d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f042d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f042d-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f042d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f042d-107">DESCRIPTION</span></span>
<span data-ttu-id="f042d-108">A **Get-AzAutomationSchedule** parancsmag azure automatizálási ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="f042d-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="f042d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f042d-109">EXAMPLES</span></span>

### <span data-ttu-id="f042d-110">1. példa: Ütemezés lekérte</span><span class="sxs-lookup"><span data-stu-id="f042d-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f042d-111">Ez a parancs a DailySchedule08 nevű ütemezést kapja.</span><span class="sxs-lookup"><span data-stu-id="f042d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="f042d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f042d-112">PARAMETERS</span></span>

### <span data-ttu-id="f042d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f042d-113">-AutomationAccountName</span></span>
<span data-ttu-id="f042d-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="f042d-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="f042d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f042d-115">-DefaultProfile</span></span>
<span data-ttu-id="f042d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f042d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f042d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f042d-117">-Name</span></span>
<span data-ttu-id="f042d-118">A parancsmag által lekért ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f042d-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f042d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f042d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f042d-120">Annak az erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag ütemezést kap.</span><span class="sxs-lookup"><span data-stu-id="f042d-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="f042d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f042d-121">CommonParameters</span></span>
<span data-ttu-id="f042d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f042d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f042d-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f042d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f042d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f042d-124">INPUTS</span></span>

### <span data-ttu-id="f042d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f042d-125">System.String</span></span>

## <span data-ttu-id="f042d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f042d-126">OUTPUTS</span></span>

### <span data-ttu-id="f042d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="f042d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f042d-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f042d-128">NOTES</span></span>

## <span data-ttu-id="f042d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f042d-129">RELATED LINKS</span></span>

[<span data-ttu-id="f042d-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f042d-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="f042d-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f042d-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="f042d-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f042d-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


