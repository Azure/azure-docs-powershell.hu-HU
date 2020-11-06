---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 83481e1d12782c3381c2d5923aa610072da41d9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504584"
---
# <span data-ttu-id="7640d-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7640d-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="7640d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7640d-102">SYNOPSIS</span></span>
<span data-ttu-id="7640d-103">Automatizálási ütemterv törlése</span><span class="sxs-lookup"><span data-stu-id="7640d-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7640d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7640d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7640d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7640d-105">DESCRIPTION</span></span>
<span data-ttu-id="7640d-106">A **Remove-AzureRmAutomationSchedule** parancsmag az Azure Automation szolgáltatásból törli az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="7640d-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="7640d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7640d-107">EXAMPLES</span></span>

### <span data-ttu-id="7640d-108">1. példa: ütemterv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7640d-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7640d-109">Ez a parancs módosítja a Schedule01 nevű ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="7640d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="7640d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7640d-110">PARAMETERS</span></span>

### <span data-ttu-id="7640d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7640d-111">-AutomationAccountName</span></span>
<span data-ttu-id="7640d-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez az adott parancsmag módosította az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="7640d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="7640d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7640d-113">-DefaultProfile</span></span>
<span data-ttu-id="7640d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7640d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7640d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7640d-115">-Force</span></span>
<span data-ttu-id="7640d-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7640d-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7640d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7640d-117">-Name</span></span>
<span data-ttu-id="7640d-118">A parancsmag által eltávolított ütemterv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7640d-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7640d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7640d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7640d-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag eltávolítja az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="7640d-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="7640d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7640d-121">-Confirm</span></span>
<span data-ttu-id="7640d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7640d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7640d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7640d-123">-WhatIf</span></span>
<span data-ttu-id="7640d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7640d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7640d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7640d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7640d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7640d-126">CommonParameters</span></span>
<span data-ttu-id="7640d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7640d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7640d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7640d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7640d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7640d-129">INPUTS</span></span>

### <span data-ttu-id="7640d-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="7640d-130">None</span></span>
<span data-ttu-id="7640d-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7640d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7640d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7640d-132">OUTPUTS</span></span>

## <span data-ttu-id="7640d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7640d-133">NOTES</span></span>

## <span data-ttu-id="7640d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7640d-134">RELATED LINKS</span></span>

[<span data-ttu-id="7640d-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7640d-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7640d-136">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7640d-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7640d-137">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7640d-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


