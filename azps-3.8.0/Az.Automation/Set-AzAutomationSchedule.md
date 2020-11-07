---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847350"
---
# <span data-ttu-id="ad3c6-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ad3c6-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="ad3c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3c6-103">Automatizálási ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="ad3c6-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="ad3c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad3c6-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad3c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad3c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3c6-106">A **set-AzAutomationSchedule** parancsmag az Azure automatizálási ütemtervét módosítja.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="ad3c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad3c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3c6-108">Példa 1: ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="ad3c6-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ad3c6-109">Ez a parancs módosítja a Schedule01 nevű ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="ad3c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad3c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ad3c6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ad3c6-111">-AutomationAccountName</span></span>
<span data-ttu-id="ad3c6-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez az adott parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="ad3c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3c6-113">-DefaultProfile</span></span>
<span data-ttu-id="ad3c6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ad3c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad3c6-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ad3c6-115">-Description</span></span>
<span data-ttu-id="ad3c6-116">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3c6-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad3c6-117">-IsEnabled</span></span>
<span data-ttu-id="ad3c6-118">Megadja, hogy ez a parancsmag engedélyezi-e az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3c6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad3c6-119">-Name</span></span>
<span data-ttu-id="ad3c6-120">A parancsmag által módosított ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad3c6-122">Annak a csoportnak a nevét adja meg, amelyhez a parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="ad3c6-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="ad3c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3c6-123">CommonParameters</span></span>
<span data-ttu-id="ad3c6-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad3c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3c6-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3c6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3c6-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad3c6-126">INPUTS</span></span>

### <span data-ttu-id="ad3c6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ad3c6-127">System.String</span></span>

### <span data-ttu-id="ad3c6-128">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad3c6-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ad3c6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad3c6-129">OUTPUTS</span></span>

### <span data-ttu-id="ad3c6-130">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ad3c6-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ad3c6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad3c6-131">NOTES</span></span>

## <span data-ttu-id="ad3c6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad3c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad3c6-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ad3c6-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="ad3c6-134">Új – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ad3c6-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="ad3c6-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ad3c6-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


