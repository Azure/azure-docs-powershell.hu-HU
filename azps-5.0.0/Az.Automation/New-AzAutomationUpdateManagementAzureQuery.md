---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299780"
---
# <span data-ttu-id="423cf-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="423cf-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="423cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="423cf-102">SYNOPSIS</span></span>
<span data-ttu-id="423cf-103">Azure Automation Software Update Configuration Azure Query-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="423cf-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="423cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="423cf-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="423cf-105">DESCRIPTION</span></span>
<span data-ttu-id="423cf-106">A szoftverfrissítési konfiguráció Azure lekérdezési objektumát hozza létre, amely egy, az ütemterven futtatott szoftverfrissítési konfiguráció létrehozásához használható, amely frissíti az Azure virtuális gépek dinamikusan megoldott listája listáját.</span><span class="sxs-lookup"><span data-stu-id="423cf-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="423cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="423cf-107">EXAMPLES</span></span>

### <span data-ttu-id="423cf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="423cf-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="423cf-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="423cf-109">PARAMETERS</span></span>

### <span data-ttu-id="423cf-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="423cf-110">-AutomationAccountName</span></span>
<span data-ttu-id="423cf-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="423cf-111">The automation account name.</span></span>

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

### <span data-ttu-id="423cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423cf-112">-DefaultProfile</span></span>
<span data-ttu-id="423cf-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="423cf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="423cf-114">-FilterOperator</span></span>
<span data-ttu-id="423cf-115">Címke szűrő operátora.</span><span class="sxs-lookup"><span data-stu-id="423cf-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="423cf-116">-Location</span></span>
<span data-ttu-id="423cf-117">Az Azure Virtual Machines helyének listája.</span><span class="sxs-lookup"><span data-stu-id="423cf-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="423cf-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="423cf-119">The resource group name.</span></span>

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

### <span data-ttu-id="423cf-120">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="423cf-120">-Scope</span></span>
<span data-ttu-id="423cf-121">Az Azure Virtual Machines erőforrás-azonosítói.</span><span class="sxs-lookup"><span data-stu-id="423cf-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="423cf-122">-Tag</span></span>
<span data-ttu-id="423cf-123">Az Azure Virtual Machines címkéje</span><span class="sxs-lookup"><span data-stu-id="423cf-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423cf-124">CommonParameters</span></span>
<span data-ttu-id="423cf-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="423cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="423cf-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423cf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423cf-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="423cf-127">INPUTS</span></span>

### <span data-ttu-id="423cf-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="423cf-128">System.String[]</span></span>

### <span data-ttu-id="423cf-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="423cf-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="423cf-130">Microsoft. Azure. Command. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="423cf-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="423cf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="423cf-131">System.String</span></span>

## <span data-ttu-id="423cf-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="423cf-132">OUTPUTS</span></span>

### <span data-ttu-id="423cf-133">Microsoft. Azure. Command. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="423cf-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="423cf-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="423cf-134">NOTES</span></span>

## <span data-ttu-id="423cf-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="423cf-135">RELATED LINKS</span></span>
