---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016071"
---
# <span data-ttu-id="7f4aa-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f4aa-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="7f4aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f4aa-102">SYNOPSIS</span></span>

<span data-ttu-id="7f4aa-103">Automatizálási ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="7f4aa-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="7f4aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f4aa-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f4aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f4aa-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7f4aa-106">A **set-AzureAutomationSchedule** parancsmag a Microsoft Azure automatizálási ütemtervét módosítja.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7f4aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f4aa-107">EXAMPLES</span></span>

### <span data-ttu-id="7f4aa-108">Példa 1: ütemterv módosítása</span><span class="sxs-lookup"><span data-stu-id="7f4aa-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="7f4aa-109">Ez a parancs módosítja a Schedule01 nevű ütemterv leírását.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="7f4aa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f4aa-110">PARAMETERS</span></span>

### <span data-ttu-id="7f4aa-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7f4aa-111">-AutomationAccountName</span></span>
<span data-ttu-id="7f4aa-112">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="7f4aa-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7f4aa-113">-Description</span></span>
<span data-ttu-id="7f4aa-114">Az ütemezés leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="7f4aa-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="7f4aa-115">-IsEnabled</span></span>
<span data-ttu-id="7f4aa-116">Azt jelzi, hogy az ütemezés engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-116">Indicates whether the schedule is enabled.</span></span>

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

### <span data-ttu-id="7f4aa-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f4aa-117">-Name</span></span>
<span data-ttu-id="7f4aa-118">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="7f4aa-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="7f4aa-119">-Profile</span></span>
<span data-ttu-id="7f4aa-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f4aa-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7f4aa-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f4aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4aa-122">CommonParameters</span></span>
<span data-ttu-id="7f4aa-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f4aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4aa-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f4aa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4aa-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f4aa-125">INPUTS</span></span>

## <span data-ttu-id="7f4aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f4aa-126">OUTPUTS</span></span>

### <span data-ttu-id="7f4aa-127">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="7f4aa-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7f4aa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f4aa-128">NOTES</span></span>

## <span data-ttu-id="7f4aa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f4aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f4aa-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f4aa-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="7f4aa-131">Új – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f4aa-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="7f4aa-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f4aa-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


