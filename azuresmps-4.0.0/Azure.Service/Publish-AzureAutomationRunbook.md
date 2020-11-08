---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015885"
---
# <span data-ttu-id="72dad-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="72dad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72dad-102">SYNOPSIS</span></span>

<span data-ttu-id="72dad-103">Közzétesz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="72dad-103">Publishes a runbook.</span></span>

## <span data-ttu-id="72dad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72dad-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="72dad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72dad-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="72dad-106">A **Közzététel-AzureAutomationRunbook** parancsmag a Microsoft Azure automatizálás üzemi környezetében használható runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="72dad-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="72dad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72dad-107">EXAMPLES</span></span>

### <span data-ttu-id="72dad-108">Példa 1: runbook közzététele</span><span class="sxs-lookup"><span data-stu-id="72dad-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="72dad-109">Ez a parancs a Contoso17 nevű automatizálási fiókban közzéteszi a Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="72dad-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="72dad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72dad-110">PARAMETERS</span></span>

### <span data-ttu-id="72dad-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72dad-111">-AutomationAccountName</span></span>
<span data-ttu-id="72dad-112">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dad-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="72dad-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72dad-113">-Name</span></span>
<span data-ttu-id="72dad-114">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dad-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="72dad-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="72dad-115">-Profile</span></span>
<span data-ttu-id="72dad-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="72dad-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72dad-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="72dad-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72dad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dad-118">CommonParameters</span></span>
<span data-ttu-id="72dad-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72dad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dad-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dad-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dad-121">INPUTS</span></span>

## <span data-ttu-id="72dad-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dad-122">OUTPUTS</span></span>

## <span data-ttu-id="72dad-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72dad-123">NOTES</span></span>

## <span data-ttu-id="72dad-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72dad-124">RELATED LINKS</span></span>

[<span data-ttu-id="72dad-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="72dad-126">Új – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="72dad-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="72dad-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="72dad-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72dad-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


