---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016171"
---
# <span data-ttu-id="a9795-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="a9795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9795-102">SYNOPSIS</span></span>

<span data-ttu-id="a9795-103">Eltávolít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="a9795-103">Removes a runbook.</span></span>

## <span data-ttu-id="a9795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9795-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9795-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9795-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a9795-106">A **Remove-AzureAutomationRunbook** parancsmag eltávolítja a Runbook a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a9795-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a9795-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9795-107">EXAMPLES</span></span>

### <span data-ttu-id="a9795-108">1. példa: runbook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a9795-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="a9795-109">Ez a parancs eltávolítja a MyRunbook nevű runbook a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a9795-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a9795-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9795-110">PARAMETERS</span></span>

### <span data-ttu-id="a9795-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9795-111">-AutomationAccountName</span></span>
<span data-ttu-id="a9795-112">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9795-112">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9795-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a9795-113">-Force</span></span>
<span data-ttu-id="a9795-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a9795-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9795-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9795-115">-Name</span></span>
<span data-ttu-id="a9795-116">Az eltávolítandó runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9795-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9795-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a9795-117">-Profile</span></span>
<span data-ttu-id="a9795-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a9795-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9795-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a9795-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9795-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9795-120">-Confirm</span></span>
<span data-ttu-id="a9795-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9795-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9795-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9795-122">-WhatIf</span></span>
<span data-ttu-id="a9795-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9795-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9795-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9795-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9795-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9795-125">CommonParameters</span></span>
<span data-ttu-id="a9795-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9795-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9795-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9795-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9795-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9795-128">INPUTS</span></span>

## <span data-ttu-id="a9795-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9795-129">OUTPUTS</span></span>

## <span data-ttu-id="a9795-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9795-130">NOTES</span></span>

## <span data-ttu-id="a9795-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9795-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9795-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="a9795-133">Új – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="a9795-134">Közzététel – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="a9795-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="a9795-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a9795-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


