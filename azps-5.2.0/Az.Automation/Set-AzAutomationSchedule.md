---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373042"
---
# <span data-ttu-id="65b8b-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="65b8b-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="65b8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="65b8b-103">Módosítja az automatizálási ütemezést.</span><span class="sxs-lookup"><span data-stu-id="65b8b-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="65b8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65b8b-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65b8b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="65b8b-106">A **Set-AzAutomationSchedule** parancsmag módosítja az ütemezést az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="65b8b-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="65b8b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="65b8b-108">1. példa: Ütemezés módosítása</span><span class="sxs-lookup"><span data-stu-id="65b8b-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="65b8b-109">Ez a parancs módosítja az Ütemezés01 nevű ütemezés leírását.</span><span class="sxs-lookup"><span data-stu-id="65b8b-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="65b8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65b8b-110">PARAMETERS</span></span>

### <span data-ttu-id="65b8b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65b8b-111">-AutomationAccountName</span></span>
<span data-ttu-id="65b8b-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja módosítja az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="65b8b-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="65b8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b8b-113">-DefaultProfile</span></span>
<span data-ttu-id="65b8b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65b8b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65b8b-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="65b8b-115">-Description</span></span>
<span data-ttu-id="65b8b-116">Megadja az ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="65b8b-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="65b8b-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="65b8b-117">-IsEnabled</span></span>
<span data-ttu-id="65b8b-118">Meghatározza, hogy ez a parancsmag engedélyezi-e az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="65b8b-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="65b8b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="65b8b-119">-Name</span></span>
<span data-ttu-id="65b8b-120">Megadja annak az ütemezésnek a nevét, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="65b8b-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="65b8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="65b8b-122">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja módosítja az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="65b8b-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="65b8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b8b-123">CommonParameters</span></span>
<span data-ttu-id="65b8b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b8b-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b8b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b8b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65b8b-126">INPUTS</span></span>

### <span data-ttu-id="65b8b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="65b8b-127">System.String</span></span>

### <span data-ttu-id="65b8b-128">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65b8b-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="65b8b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b8b-129">OUTPUTS</span></span>

### <span data-ttu-id="65b8b-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="65b8b-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="65b8b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65b8b-131">NOTES</span></span>

## <span data-ttu-id="65b8b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65b8b-132">RELATED LINKS</span></span>

[<span data-ttu-id="65b8b-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="65b8b-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="65b8b-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="65b8b-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="65b8b-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="65b8b-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


