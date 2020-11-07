---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 76cc8117458db23f947a998d29de09a900bb6d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672491"
---
# <span data-ttu-id="fedea-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fedea-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="fedea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fedea-102">SYNOPSIS</span></span>
<span data-ttu-id="fedea-103">Automatizálási ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="fedea-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fedea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fedea-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fedea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fedea-105">DESCRIPTION</span></span>
<span data-ttu-id="fedea-106">A **set-AzureRmAutomationSchedule** parancsmag az Azure automatizálási ütemtervét módosítja.</span><span class="sxs-lookup"><span data-stu-id="fedea-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="fedea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fedea-107">EXAMPLES</span></span>

### <span data-ttu-id="fedea-108">Példa 1: ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="fedea-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fedea-109">Ez a parancs módosítja a Schedule01 nevű ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="fedea-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="fedea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fedea-110">PARAMETERS</span></span>

### <span data-ttu-id="fedea-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fedea-111">-AutomationAccountName</span></span>
<span data-ttu-id="fedea-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez az adott parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="fedea-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="fedea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedea-113">-DefaultProfile</span></span>
<span data-ttu-id="fedea-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fedea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fedea-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fedea-115">-Description</span></span>
<span data-ttu-id="fedea-116">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fedea-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="fedea-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="fedea-117">-IsEnabled</span></span>
<span data-ttu-id="fedea-118">Megadja, hogy ez a parancsmag engedélyezi-e az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="fedea-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="fedea-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fedea-119">-Name</span></span>
<span data-ttu-id="fedea-120">A parancsmag által módosított ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fedea-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fedea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedea-121">-ResourceGroupName</span></span>
<span data-ttu-id="fedea-122">Annak a csoportnak a nevét adja meg, amelyhez a parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="fedea-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="fedea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedea-123">CommonParameters</span></span>
<span data-ttu-id="fedea-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fedea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedea-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedea-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fedea-126">INPUTS</span></span>

### <span data-ttu-id="fedea-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fedea-127">System.String</span></span>

### <span data-ttu-id="fedea-128">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fedea-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fedea-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fedea-129">OUTPUTS</span></span>

### <span data-ttu-id="fedea-130">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="fedea-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="fedea-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fedea-131">NOTES</span></span>

## <span data-ttu-id="fedea-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fedea-132">RELATED LINKS</span></span>

[<span data-ttu-id="fedea-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fedea-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="fedea-134">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fedea-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="fedea-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fedea-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


