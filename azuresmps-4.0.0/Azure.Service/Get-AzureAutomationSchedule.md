---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015655"
---
# <span data-ttu-id="cc0e8-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc0e8-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="cc0e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc0e8-102">SYNOPSIS</span></span>

<span data-ttu-id="cc0e8-103">Azure automatizálási ütemtervet kap.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="cc0e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc0e8-104">SYNTAX</span></span>

### <span data-ttu-id="cc0e8-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc0e8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cc0e8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cc0e8-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc0e8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc0e8-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cc0e8-108">A **Get-AzureAutomationSchedule** parancsmag a Microsoft Azure automatizálási ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="cc0e8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc0e8-109">EXAMPLES</span></span>

### <span data-ttu-id="cc0e8-110">Példa 1: ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc0e8-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="cc0e8-111">Ez a parancs a DailySchedule08 nevű ütemtervet kapja.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="cc0e8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc0e8-112">PARAMETERS</span></span>

### <span data-ttu-id="cc0e8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc0e8-113">-AutomationAccountName</span></span>
<span data-ttu-id="cc0e8-114">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="cc0e8-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc0e8-115">-Name</span></span>
<span data-ttu-id="cc0e8-116">Az ütemezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0e8-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="cc0e8-117">-Profile</span></span>
<span data-ttu-id="cc0e8-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc0e8-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc0e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0e8-120">CommonParameters</span></span>
<span data-ttu-id="cc0e8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc0e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0e8-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc0e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0e8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0e8-123">INPUTS</span></span>

## <span data-ttu-id="cc0e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0e8-124">OUTPUTS</span></span>

### <span data-ttu-id="cc0e8-125">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="cc0e8-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="cc0e8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc0e8-126">NOTES</span></span>

## <span data-ttu-id="cc0e8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc0e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="cc0e8-128">Új – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc0e8-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="cc0e8-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc0e8-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="cc0e8-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cc0e8-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


