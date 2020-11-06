---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501227"
---
# <span data-ttu-id="4b6e2-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4b6e2-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="4b6e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6e2-103">Automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b6e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b6e2-104">SYNTAX</span></span>

### <span data-ttu-id="4b6e2-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b6e2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b6e2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4b6e2-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6e2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b6e2-107">DESCRIPTION</span></span>
<span data-ttu-id="4b6e2-108">A **Get-AzureRmAutomationSchedule** parancsmag Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="4b6e2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4b6e2-109">EXAMPLES</span></span>

### <span data-ttu-id="4b6e2-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="4b6e2-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4b6e2-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="4b6e2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b6e2-112">PARAMETERS</span></span>

### <span data-ttu-id="4b6e2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b6e2-113">-AutomationAccountName</span></span>
<span data-ttu-id="4b6e2-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag beolvassa az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="4b6e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6e2-115">-DefaultProfile</span></span>
<span data-ttu-id="4b6e2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b6e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6e2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b6e2-117">-Name</span></span>
<span data-ttu-id="4b6e2-118">Itt adhatja meg annak az ütemezésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4b6e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b6e2-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag az ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="4b6e2-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="4b6e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6e2-121">CommonParameters</span></span>
<span data-ttu-id="4b6e2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b6e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6e2-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6e2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6e2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6e2-124">INPUTS</span></span>

### <span data-ttu-id="4b6e2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4b6e2-125">System.String</span></span>

## <span data-ttu-id="4b6e2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6e2-126">OUTPUTS</span></span>

### <span data-ttu-id="4b6e2-127">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="4b6e2-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="4b6e2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b6e2-128">NOTES</span></span>

## <span data-ttu-id="4b6e2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b6e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b6e2-130">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4b6e2-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="4b6e2-131">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4b6e2-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="4b6e2-132">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4b6e2-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


