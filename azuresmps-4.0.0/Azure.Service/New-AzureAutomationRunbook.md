---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015934"
---
# <span data-ttu-id="58a66-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="58a66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58a66-102">SYNOPSIS</span></span>

<span data-ttu-id="58a66-103">Létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="58a66-103">Creates a runbook.</span></span>

## <span data-ttu-id="58a66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58a66-104">SYNTAX</span></span>

### <span data-ttu-id="58a66-105">ByRunbookName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58a66-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="58a66-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="58a66-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="58a66-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="58a66-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="58a66-108">A **New-AzureAutomationRunbook** parancsmag egy új, üres Microsoft Azure automatizálási runbook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="58a66-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="58a66-109">Adjon meg egy nevet az új runbook létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="58a66-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="58a66-110">A runbook importálásához megadhatja a Windows PowerShell-parancsfájlok (. ps1) elérési útját is.</span><span class="sxs-lookup"><span data-stu-id="58a66-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="58a66-111">Az importálandó parancsfájl csak egy Windows PowerShell-munkafolyamat-definíciót tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="58a66-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="58a66-112">Ennek a Windows PowerShell-munkafolyamatnak a neve a runbook neve lesz.</span><span class="sxs-lookup"><span data-stu-id="58a66-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="58a66-113">Példák</span><span class="sxs-lookup"><span data-stu-id="58a66-113">EXAMPLES</span></span>

### <span data-ttu-id="58a66-114">Példa 1: runbook létrehozása</span><span class="sxs-lookup"><span data-stu-id="58a66-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="58a66-115">Ez a parancs létrehoz egy Runbook02 nevű új runbook a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="58a66-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="58a66-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58a66-116">PARAMETERS</span></span>

### <span data-ttu-id="58a66-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="58a66-117">-AutomationAccountName</span></span>
<span data-ttu-id="58a66-118">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58a66-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="58a66-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="58a66-119">-Description</span></span>
<span data-ttu-id="58a66-120">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="58a66-120">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a66-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58a66-121">-Name</span></span>
<span data-ttu-id="58a66-122">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58a66-122">Specifies the name for the runbook.</span></span>

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

### <span data-ttu-id="58a66-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="58a66-123">-Path</span></span>
<span data-ttu-id="58a66-124">Az elérési utat adja meg.</span><span class="sxs-lookup"><span data-stu-id="58a66-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a66-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="58a66-125">-Profile</span></span>
<span data-ttu-id="58a66-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="58a66-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58a66-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="58a66-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58a66-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="58a66-128">-Tags</span></span>
<span data-ttu-id="58a66-129">A runbook címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="58a66-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a66-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a66-130">CommonParameters</span></span>
<span data-ttu-id="58a66-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58a66-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a66-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a66-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a66-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a66-133">INPUTS</span></span>

## <span data-ttu-id="58a66-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a66-134">OUTPUTS</span></span>

### <span data-ttu-id="58a66-135">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="58a66-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="58a66-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58a66-136">NOTES</span></span>

## <span data-ttu-id="58a66-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58a66-137">RELATED LINKS</span></span>

[<span data-ttu-id="58a66-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="58a66-139">Közzététel – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="58a66-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="58a66-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="58a66-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58a66-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


