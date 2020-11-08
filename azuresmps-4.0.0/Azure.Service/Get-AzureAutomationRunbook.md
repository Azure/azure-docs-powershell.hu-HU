---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015657"
---
# <span data-ttu-id="ab648-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="ab648-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab648-102">SYNOPSIS</span></span>

<span data-ttu-id="ab648-103">Kap egy runbook.</span><span class="sxs-lookup"><span data-stu-id="ab648-103">Gets a runbook.</span></span>

## <span data-ttu-id="ab648-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab648-104">SYNTAX</span></span>

### <span data-ttu-id="ab648-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab648-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ab648-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ab648-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab648-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab648-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ab648-108">A **Get-AzureAutomationRunbook** parancsmag egy vagy több Microsoft Azure automatizálási runbooks kap.</span><span class="sxs-lookup"><span data-stu-id="ab648-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="ab648-109">Alapértelmezés szerint az összes runbooks adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ab648-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="ab648-110">Ha meghatározott runbook szeretne kapni, adja meg annak nevét vagy AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="ab648-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="ab648-111">Ha az összes olyan runbooks meg szeretné kapni, amely egy adott ütemtervhez van társítva, adja meg az ütemezés nevét.</span><span class="sxs-lookup"><span data-stu-id="ab648-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="ab648-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ab648-112">EXAMPLES</span></span>

### <span data-ttu-id="ab648-113">Példa 1: az összes runbooks beolvasása</span><span class="sxs-lookup"><span data-stu-id="ab648-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ab648-114">Ez a parancs a Contoso17 nevű Azure automatizálási fiók minden runbooks bekerül.</span><span class="sxs-lookup"><span data-stu-id="ab648-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ab648-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab648-115">PARAMETERS</span></span>

### <span data-ttu-id="ab648-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab648-116">-AutomationAccountName</span></span>
<span data-ttu-id="ab648-117">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab648-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="ab648-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab648-118">-Name</span></span>
<span data-ttu-id="ab648-119">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab648-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab648-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab648-120">-Profile</span></span>
<span data-ttu-id="ab648-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ab648-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ab648-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ab648-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab648-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab648-123">CommonParameters</span></span>
<span data-ttu-id="ab648-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab648-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab648-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab648-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab648-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab648-126">INPUTS</span></span>

## <span data-ttu-id="ab648-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab648-127">OUTPUTS</span></span>

### <span data-ttu-id="ab648-128">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ab648-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ab648-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab648-129">NOTES</span></span>

## <span data-ttu-id="ab648-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab648-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab648-131">Új – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="ab648-132">Közzététel – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="ab648-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="ab648-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="ab648-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab648-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


