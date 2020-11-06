---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 03763ad7c2212eb89650749eb6d407d9ce973693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493881"
---
# <span data-ttu-id="c0712-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c0712-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="c0712-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0712-102">SYNOPSIS</span></span>
<span data-ttu-id="c0712-103">Automatizálási ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="c0712-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0712-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0712-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0712-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0712-105">DESCRIPTION</span></span>
<span data-ttu-id="c0712-106">A **set-AzureRmAutomationSchedule** parancsmag az Azure automatizálási ütemtervét módosítja.</span><span class="sxs-lookup"><span data-stu-id="c0712-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="c0712-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0712-107">EXAMPLES</span></span>

### <span data-ttu-id="c0712-108">Példa 1: ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="c0712-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0712-109">Ez a parancs módosítja a Schedule01 nevű ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="c0712-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="c0712-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0712-110">PARAMETERS</span></span>

### <span data-ttu-id="c0712-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0712-111">-AutomationAccountName</span></span>
<span data-ttu-id="c0712-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez az adott parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="c0712-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="c0712-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c0712-113">-Description</span></span>
<span data-ttu-id="c0712-114">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0712-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="c0712-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0712-115">-IsEnabled</span></span>
<span data-ttu-id="c0712-116">Megadja, hogy ez a parancsmag engedélyezi-e az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="c0712-116">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="c0712-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0712-117">-Name</span></span>
<span data-ttu-id="c0712-118">A parancsmag által módosított ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0712-118">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c0712-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0712-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0712-120">Annak a csoportnak a nevét adja meg, amelyhez a parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="c0712-120">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="c0712-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0712-121">-DefaultProfile</span></span>
<span data-ttu-id="c0712-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0712-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0712-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0712-123">CommonParameters</span></span>
<span data-ttu-id="c0712-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0712-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0712-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0712-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0712-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0712-126">INPUTS</span></span>

## <span data-ttu-id="c0712-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0712-127">OUTPUTS</span></span>

### <span data-ttu-id="c0712-128">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="c0712-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="c0712-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0712-129">NOTES</span></span>

## <span data-ttu-id="c0712-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0712-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0712-131">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c0712-131">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c0712-132">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c0712-132">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c0712-133">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c0712-133">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


