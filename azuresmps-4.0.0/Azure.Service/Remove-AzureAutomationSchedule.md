---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016170"
---
# <span data-ttu-id="50fa6-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="50fa6-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="50fa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50fa6-102">SYNOPSIS</span></span>

<span data-ttu-id="50fa6-103">Azure automatizálási ütemterv törlése</span><span class="sxs-lookup"><span data-stu-id="50fa6-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="50fa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50fa6-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50fa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50fa6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="50fa6-106">A **Remove-AzureAutomationSchedule** parancsmag a Microsoft Azure Automation szolgáltatásból törli az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="50fa6-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="50fa6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50fa6-107">EXAMPLES</span></span>

### <span data-ttu-id="50fa6-108">1. példa: ütemterv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="50fa6-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="50fa6-109">Ez a parancs eltávolítja a MySchedule nevű ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="50fa6-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="50fa6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50fa6-110">PARAMETERS</span></span>

### <span data-ttu-id="50fa6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50fa6-111">-AutomationAccountName</span></span>
<span data-ttu-id="50fa6-112">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50fa6-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="50fa6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="50fa6-113">-Force</span></span>
<span data-ttu-id="50fa6-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="50fa6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50fa6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50fa6-115">-Name</span></span>
<span data-ttu-id="50fa6-116">Az eltávolítandó ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50fa6-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="50fa6-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="50fa6-117">-Profile</span></span>
<span data-ttu-id="50fa6-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="50fa6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50fa6-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="50fa6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50fa6-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50fa6-120">-Confirm</span></span>
<span data-ttu-id="50fa6-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50fa6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fa6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fa6-122">-WhatIf</span></span>
<span data-ttu-id="50fa6-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50fa6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fa6-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50fa6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fa6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fa6-125">CommonParameters</span></span>
<span data-ttu-id="50fa6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50fa6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fa6-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50fa6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fa6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50fa6-128">INPUTS</span></span>

## <span data-ttu-id="50fa6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50fa6-129">OUTPUTS</span></span>

## <span data-ttu-id="50fa6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50fa6-130">NOTES</span></span>

## <span data-ttu-id="50fa6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50fa6-131">RELATED LINKS</span></span>

[<span data-ttu-id="50fa6-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="50fa6-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="50fa6-133">Új – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="50fa6-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="50fa6-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="50fa6-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


