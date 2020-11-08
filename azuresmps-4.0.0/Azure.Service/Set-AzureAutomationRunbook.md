---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016072"
---
# <span data-ttu-id="9d6e5-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="9d6e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d6e5-102">SYNOPSIS</span></span>

<span data-ttu-id="9d6e5-103">Módosítja egy runbook konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="9d6e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d6e5-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d6e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d6e5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9d6e5-106">A **set-AzureAutomationRunbook** parancsmag a Microsoft Azure Automation runbook konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="9d6e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d6e5-107">EXAMPLES</span></span>

### <span data-ttu-id="9d6e5-108">Példa 1: a runbook részletes naplózásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="9d6e5-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="9d6e5-109">Ez a parancs lehetővé teszi a Contoso17 nevű automatizálási fiókban megadott runbook-feladatok részletes naplózását.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9d6e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d6e5-110">PARAMETERS</span></span>

### <span data-ttu-id="9d6e5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d6e5-111">-AutomationAccountName</span></span>
<span data-ttu-id="9d6e5-112">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="9d6e5-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9d6e5-113">-Description</span></span>
<span data-ttu-id="9d6e5-114">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="9d6e5-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="9d6e5-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d6e5-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="9d6e5-116">-LogVerbose</span></span>
<span data-ttu-id="9d6e5-117">Azt jelzi, hogy a részletes naplózást használja-e.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d6e5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d6e5-118">-Name</span></span>
<span data-ttu-id="9d6e5-119">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-119">Specifies a name.</span></span>

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

### <span data-ttu-id="9d6e5-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d6e5-120">-Profile</span></span>
<span data-ttu-id="9d6e5-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d6e5-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d6e5-123">-Címkék</span><span class="sxs-lookup"><span data-stu-id="9d6e5-123">-Tags</span></span>
<span data-ttu-id="9d6e5-124">A címkék tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6e5-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d6e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6e5-125">CommonParameters</span></span>
<span data-ttu-id="9d6e5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d6e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6e5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d6e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6e5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6e5-128">INPUTS</span></span>

## <span data-ttu-id="9d6e5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6e5-129">OUTPUTS</span></span>

### <span data-ttu-id="9d6e5-130">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9d6e5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d6e5-131">NOTES</span></span>

## <span data-ttu-id="9d6e5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d6e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="9d6e5-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="9d6e5-134">Új – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="9d6e5-135">Közzététel – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="9d6e5-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="9d6e5-137">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9d6e5-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


