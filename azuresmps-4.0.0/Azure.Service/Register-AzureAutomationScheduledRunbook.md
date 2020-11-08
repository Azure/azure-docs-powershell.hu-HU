---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015873"
---
# <span data-ttu-id="a381f-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="a381f-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="a381f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a381f-102">SYNOPSIS</span></span>

<span data-ttu-id="a381f-103">Runbook társít egy ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="a381f-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="a381f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a381f-104">SYNTAX</span></span>

### <span data-ttu-id="a381f-105">ByRunbookName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a381f-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a381f-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="a381f-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a381f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a381f-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a381f-108">A **Register-AzureAutomationScheduledRunbook** parancsmag egy runbook társít egy ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="a381f-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="a381f-109">A runbook a *ScheduleName* paraméterrel megadott ütemezés alapján kezdődik.</span><span class="sxs-lookup"><span data-stu-id="a381f-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="a381f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a381f-110">EXAMPLES</span></span>

### <span data-ttu-id="a381f-111">1. példa: runbook társítása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="a381f-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="a381f-112">Ez a parancs a Runbk01 nevű runbook társítja a Contoso17 nevű Azure automatizálási fiók Sched01 nevű munkabeosztásával.</span><span class="sxs-lookup"><span data-stu-id="a381f-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a381f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a381f-113">PARAMETERS</span></span>

### <span data-ttu-id="a381f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a381f-114">-AutomationAccountName</span></span>
<span data-ttu-id="a381f-115">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a381f-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="a381f-116">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="a381f-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a381f-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a381f-117">-Profile</span></span>
<span data-ttu-id="a381f-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a381f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a381f-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a381f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a381f-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a381f-120">-RunbookName</span></span>
<span data-ttu-id="a381f-121">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a381f-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a381f-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="a381f-122">-ScheduleName</span></span>
<span data-ttu-id="a381f-123">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a381f-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a381f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a381f-124">CommonParameters</span></span>
<span data-ttu-id="a381f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a381f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a381f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a381f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a381f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a381f-127">INPUTS</span></span>

## <span data-ttu-id="a381f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a381f-128">OUTPUTS</span></span>

### <span data-ttu-id="a381f-129">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="a381f-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="a381f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a381f-130">NOTES</span></span>

## <span data-ttu-id="a381f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a381f-131">RELATED LINKS</span></span>

[<span data-ttu-id="a381f-132">Új – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a381f-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="a381f-133">Regisztráció törlése – AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="a381f-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


