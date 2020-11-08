---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016587"
---
# <span data-ttu-id="b1e26-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="b1e26-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="b1e26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1e26-102">SYNOPSIS</span></span>

<span data-ttu-id="b1e26-103">Egy runbook és egy ütemterv közötti társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b1e26-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="b1e26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1e26-104">SYNTAX</span></span>

### <span data-ttu-id="b1e26-105">ByJobScheduleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1e26-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b1e26-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="b1e26-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1e26-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1e26-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b1e26-108">A **unregister-AzureAutomationScheduledRunbook** parancsmag eltávolítja a társítást a Microsoft Azure automatizálási runbook és az ütemezés között, amely az ütemezési tüzektől kezdve leáll a runbook.</span><span class="sxs-lookup"><span data-stu-id="b1e26-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="b1e26-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b1e26-109">EXAMPLES</span></span>

### <span data-ttu-id="b1e26-110">1. példa: a runbook és az ütemterv közötti társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b1e26-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="b1e26-111">Ez a parancs eltávolítja a Runbk01 nevű runbook társítását és a Runbk01Sched nevű ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="b1e26-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="b1e26-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1e26-112">PARAMETERS</span></span>

### <span data-ttu-id="b1e26-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1e26-113">-AutomationAccountName</span></span>
<span data-ttu-id="b1e26-114">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1e26-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="b1e26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b1e26-115">-Force</span></span>
<span data-ttu-id="b1e26-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b1e26-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1e26-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b1e26-117">-JobScheduleId</span></span>
<span data-ttu-id="b1e26-118">Az ütemezett runbook AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1e26-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1e26-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1e26-119">-Profile</span></span>
<span data-ttu-id="b1e26-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b1e26-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1e26-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b1e26-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1e26-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b1e26-122">-RunbookName</span></span>
<span data-ttu-id="b1e26-123">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1e26-123">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="b1e26-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="b1e26-124">-ScheduleName</span></span>
<span data-ttu-id="b1e26-125">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1e26-125">Specifies the name of a schedule.</span></span>

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

### <span data-ttu-id="b1e26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e26-126">CommonParameters</span></span>
<span data-ttu-id="b1e26-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1e26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e26-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e26-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e26-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1e26-129">INPUTS</span></span>

## <span data-ttu-id="b1e26-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1e26-130">OUTPUTS</span></span>

## <span data-ttu-id="b1e26-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1e26-131">NOTES</span></span>

## <span data-ttu-id="b1e26-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1e26-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1e26-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="b1e26-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


