---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 2b35281cd276be9149f2d4c4e17cb38f48eadc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503119"
---
# <span data-ttu-id="3808c-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3808c-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="3808c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3808c-102">SYNOPSIS</span></span>
<span data-ttu-id="3808c-103">Automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="3808c-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3808c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3808c-104">SYNTAX</span></span>

### <span data-ttu-id="3808c-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3808c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3808c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3808c-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3808c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3808c-107">DESCRIPTION</span></span>
<span data-ttu-id="3808c-108">A **Get-AzureRmAutomationSchedule** parancsmag Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="3808c-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="3808c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3808c-109">EXAMPLES</span></span>

### <span data-ttu-id="3808c-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="3808c-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3808c-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="3808c-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="3808c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3808c-112">PARAMETERS</span></span>

### <span data-ttu-id="3808c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3808c-113">-AutomationAccountName</span></span>
<span data-ttu-id="3808c-114">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag beolvassa az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="3808c-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3808c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3808c-115">-DefaultProfile</span></span>
<span data-ttu-id="3808c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3808c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3808c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3808c-117">-Name</span></span>
<span data-ttu-id="3808c-118">Itt adhatja meg annak az ütemezésnek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3808c-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3808c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3808c-119">-ResourceGroupName</span></span>
<span data-ttu-id="3808c-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag az ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="3808c-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3808c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3808c-121">CommonParameters</span></span>
<span data-ttu-id="3808c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3808c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3808c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3808c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3808c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3808c-124">INPUTS</span></span>

### <span data-ttu-id="3808c-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="3808c-125">None</span></span>
<span data-ttu-id="3808c-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3808c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3808c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3808c-127">OUTPUTS</span></span>

### <span data-ttu-id="3808c-128">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="3808c-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3808c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3808c-129">NOTES</span></span>

## <span data-ttu-id="3808c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3808c-130">RELATED LINKS</span></span>

[<span data-ttu-id="3808c-131">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3808c-131">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3808c-132">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3808c-132">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3808c-133">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3808c-133">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


