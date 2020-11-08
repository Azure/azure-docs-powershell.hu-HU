---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016362"
---
# <span data-ttu-id="bc616-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="bc616-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="bc616-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc616-102">SYNOPSIS</span></span>

<span data-ttu-id="bc616-103">Runbook-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="bc616-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="bc616-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc616-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc616-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc616-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="bc616-106">A **Get-AzureAutomationRunbookDefinition** parancsmag a Piszkozat definícióját, a közzétett definíciót vagy az Azure automatizálási runbook mindkét definícióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="bc616-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="bc616-107">A program alapértelmezés szerint a közzétett verziót adja vissza.</span><span class="sxs-lookup"><span data-stu-id="bc616-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="bc616-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bc616-108">EXAMPLES</span></span>

### <span data-ttu-id="bc616-109">Példa 1: a runbook definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc616-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="bc616-110">Ez a parancs a Contoso17 nevű Azure automatizálási fiókban a RunbookDef01 nevű runbook közzétett runbook-definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc616-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bc616-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc616-111">PARAMETERS</span></span>

### <span data-ttu-id="bc616-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc616-112">-AutomationAccountName</span></span>
<span data-ttu-id="bc616-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc616-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="bc616-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc616-114">-Name</span></span>
<span data-ttu-id="bc616-115">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc616-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="bc616-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="bc616-116">-Profile</span></span>
<span data-ttu-id="bc616-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="bc616-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc616-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="bc616-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc616-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="bc616-119">-Slot</span></span>
<span data-ttu-id="bc616-120">A bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc616-120">Specifies the slot.</span></span>
<span data-ttu-id="bc616-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bc616-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc616-122">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="bc616-122">Draft</span></span>
- <span data-ttu-id="bc616-123">Közzétett</span><span class="sxs-lookup"><span data-stu-id="bc616-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc616-124">CommonParameters</span></span>
<span data-ttu-id="bc616-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc616-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc616-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc616-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc616-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc616-127">INPUTS</span></span>

## <span data-ttu-id="bc616-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc616-128">OUTPUTS</span></span>

## <span data-ttu-id="bc616-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc616-129">NOTES</span></span>

## <span data-ttu-id="bc616-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc616-130">RELATED LINKS</span></span>

[<span data-ttu-id="bc616-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="bc616-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


