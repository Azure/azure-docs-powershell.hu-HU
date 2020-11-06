---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 1252864be8e55638ec5e982bd075aec647b68a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505680"
---
# <span data-ttu-id="da1f9-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da1f9-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="da1f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="da1f9-103">Automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="da1f9-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da1f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da1f9-104">SYNTAX</span></span>

### <span data-ttu-id="da1f9-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da1f9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da1f9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="da1f9-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da1f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="da1f9-107">DESCRIPTION</span></span>
<span data-ttu-id="da1f9-108">A **Get-AzureRmAutomationSchedule** parancsmag Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="da1f9-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="da1f9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da1f9-109">EXAMPLES</span></span>

### <span data-ttu-id="da1f9-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="da1f9-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da1f9-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="da1f9-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="da1f9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da1f9-112">PARAMETERS</span></span>

### <span data-ttu-id="da1f9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da1f9-113">-AutomationAccountName</span></span>
<span data-ttu-id="da1f9-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag beolvassa az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="da1f9-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="da1f9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da1f9-115">-Name</span></span>
<span data-ttu-id="da1f9-116">Itt adhatja meg annak az ütemezésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="da1f9-116">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da1f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da1f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="da1f9-118">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag az ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="da1f9-118">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="da1f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1f9-119">-DefaultProfile</span></span>
<span data-ttu-id="da1f9-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da1f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da1f9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1f9-121">CommonParameters</span></span>
<span data-ttu-id="da1f9-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da1f9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1f9-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da1f9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1f9-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da1f9-124">INPUTS</span></span>

## <span data-ttu-id="da1f9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da1f9-125">OUTPUTS</span></span>

### <span data-ttu-id="da1f9-126">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="da1f9-126">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="da1f9-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da1f9-127">NOTES</span></span>

## <span data-ttu-id="da1f9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da1f9-128">RELATED LINKS</span></span>

[<span data-ttu-id="da1f9-129">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da1f9-129">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="da1f9-130">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da1f9-130">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="da1f9-131">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da1f9-131">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


