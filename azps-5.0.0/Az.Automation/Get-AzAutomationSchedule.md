---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301610"
---
# <span data-ttu-id="a120a-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a120a-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="a120a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a120a-102">SYNOPSIS</span></span>
<span data-ttu-id="a120a-103">Automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="a120a-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="a120a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a120a-104">SYNTAX</span></span>

### <span data-ttu-id="a120a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a120a-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a120a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a120a-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a120a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a120a-107">DESCRIPTION</span></span>
<span data-ttu-id="a120a-108">A **Get-AzAutomationSchedule** parancsmag Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="a120a-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="a120a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a120a-109">EXAMPLES</span></span>

### <span data-ttu-id="a120a-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="a120a-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a120a-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="a120a-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="a120a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a120a-112">PARAMETERS</span></span>

### <span data-ttu-id="a120a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a120a-113">-AutomationAccountName</span></span>
<span data-ttu-id="a120a-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag beolvassa az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="a120a-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="a120a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a120a-115">-DefaultProfile</span></span>
<span data-ttu-id="a120a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a120a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a120a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a120a-117">-Name</span></span>
<span data-ttu-id="a120a-118">Itt adhatja meg annak az ütemezésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a120a-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a120a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a120a-119">-ResourceGroupName</span></span>
<span data-ttu-id="a120a-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag az ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="a120a-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="a120a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a120a-121">CommonParameters</span></span>
<span data-ttu-id="a120a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a120a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a120a-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a120a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a120a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a120a-124">INPUTS</span></span>

### <span data-ttu-id="a120a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a120a-125">System.String</span></span>

## <span data-ttu-id="a120a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a120a-126">OUTPUTS</span></span>

### <span data-ttu-id="a120a-127">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a120a-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a120a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a120a-128">NOTES</span></span>

## <span data-ttu-id="a120a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a120a-129">RELATED LINKS</span></span>

[<span data-ttu-id="a120a-130">Új – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a120a-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="a120a-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a120a-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="a120a-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a120a-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


