---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: 237cd5dfa3ae64273361bb2f79f301ffa93dd29c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671603"
---
# <span data-ttu-id="7ef83-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ef83-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="7ef83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ef83-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef83-103">Automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="7ef83-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="7ef83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ef83-104">SYNTAX</span></span>

### <span data-ttu-id="7ef83-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ef83-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef83-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7ef83-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ef83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ef83-107">DESCRIPTION</span></span>
<span data-ttu-id="7ef83-108">A **Get-AzAutomationSchedule** parancsmag Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="7ef83-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="7ef83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7ef83-109">EXAMPLES</span></span>

### <span data-ttu-id="7ef83-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ef83-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ef83-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="7ef83-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="7ef83-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ef83-112">PARAMETERS</span></span>

### <span data-ttu-id="7ef83-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ef83-113">-AutomationAccountName</span></span>
<span data-ttu-id="7ef83-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag beolvassa az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="7ef83-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="7ef83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef83-115">-DefaultProfile</span></span>
<span data-ttu-id="7ef83-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ef83-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ef83-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ef83-117">-Name</span></span>
<span data-ttu-id="7ef83-118">Itt adhatja meg annak az ütemezésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7ef83-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ef83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef83-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ef83-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag az ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="7ef83-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="7ef83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef83-121">CommonParameters</span></span>
<span data-ttu-id="7ef83-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ef83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef83-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef83-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef83-124">INPUTS</span></span>

### <span data-ttu-id="7ef83-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7ef83-125">System.String</span></span>

## <span data-ttu-id="7ef83-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef83-126">OUTPUTS</span></span>

### <span data-ttu-id="7ef83-127">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="7ef83-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7ef83-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ef83-128">NOTES</span></span>

## <span data-ttu-id="7ef83-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ef83-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ef83-130">Új – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ef83-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="7ef83-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ef83-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="7ef83-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ef83-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


