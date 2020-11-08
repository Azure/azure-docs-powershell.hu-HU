---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016070"
---
# <span data-ttu-id="80cd7-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="80cd7-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="80cd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80cd7-102">SYNOPSIS</span></span>

<span data-ttu-id="80cd7-103">Frissíti a runbook vázlat definícióját.</span><span class="sxs-lookup"><span data-stu-id="80cd7-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="80cd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80cd7-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80cd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80cd7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="80cd7-106">A **set-AzureAutomationRunbookDefinition** parancsmag frissíti a Microsoft Azure automatizálási runbook vázlatának definícióját.</span><span class="sxs-lookup"><span data-stu-id="80cd7-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="80cd7-107">Adjon meg egy olyan Windows PowerShell-parancsfájlt (. ps1) tartalmazó fájlt, amely a Piszkozat runbook runbook válik.</span><span class="sxs-lookup"><span data-stu-id="80cd7-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="80cd7-108">Ha már létezik Piszkozat-definíció, a *felülírás* paraméterrel kényszerítheti a parancsmagot, hogy felülírja a meglévő piszkozatot.</span><span class="sxs-lookup"><span data-stu-id="80cd7-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="80cd7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="80cd7-109">EXAMPLES</span></span>

### <span data-ttu-id="80cd7-110">Példa 1: egy runbook meglévő vázlat definíciójának felülírása</span><span class="sxs-lookup"><span data-stu-id="80cd7-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="80cd7-111">Ez a parancs felülírja a runbook meglévő Piszkozat-definícióját.</span><span class="sxs-lookup"><span data-stu-id="80cd7-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="80cd7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80cd7-112">PARAMETERS</span></span>

### <span data-ttu-id="80cd7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="80cd7-113">-AutomationAccountName</span></span>
<span data-ttu-id="80cd7-114">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80cd7-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="80cd7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80cd7-115">-Name</span></span>
<span data-ttu-id="80cd7-116">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="80cd7-116">Specifies a name.</span></span>

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

### <span data-ttu-id="80cd7-117">-Átír</span><span class="sxs-lookup"><span data-stu-id="80cd7-117">-Overwrite</span></span>
<span data-ttu-id="80cd7-118">Azt jelzi, hogy felülír-e egy meglévő Piszkozat definíciót.</span><span class="sxs-lookup"><span data-stu-id="80cd7-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cd7-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="80cd7-119">-Path</span></span>
<span data-ttu-id="80cd7-120">A runbook elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80cd7-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cd7-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="80cd7-121">-Profile</span></span>
<span data-ttu-id="80cd7-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="80cd7-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80cd7-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="80cd7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80cd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cd7-124">CommonParameters</span></span>
<span data-ttu-id="80cd7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80cd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cd7-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80cd7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cd7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80cd7-127">INPUTS</span></span>

## <span data-ttu-id="80cd7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80cd7-128">OUTPUTS</span></span>

### <span data-ttu-id="80cd7-129">Microsoft. Azure. Command. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="80cd7-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="80cd7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80cd7-130">NOTES</span></span>

## <span data-ttu-id="80cd7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80cd7-131">RELATED LINKS</span></span>

[<span data-ttu-id="80cd7-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="80cd7-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


