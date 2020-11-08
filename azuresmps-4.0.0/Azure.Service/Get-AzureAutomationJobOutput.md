---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015658"
---
# <span data-ttu-id="0ce09-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0ce09-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="0ce09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ce09-102">SYNOPSIS</span></span>

<span data-ttu-id="0ce09-103">Az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="0ce09-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="0ce09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ce09-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ce09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ce09-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0ce09-106">A **Get-AzureAutomationJobOutput** parancsmag a Microsoft Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="0ce09-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="0ce09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ce09-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce09-108">Példa 1: az Azure automatizálási feladatok eredményének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ce09-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="0ce09-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="0ce09-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="0ce09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ce09-110">PARAMETERS</span></span>

### <span data-ttu-id="0ce09-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ce09-111">-AutomationAccountName</span></span>
<span data-ttu-id="0ce09-112">Az Azure automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce09-112">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="0ce09-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="0ce09-113">-Id</span></span>
<span data-ttu-id="0ce09-114">Egy feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce09-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce09-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="0ce09-115">-Profile</span></span>
<span data-ttu-id="0ce09-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0ce09-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ce09-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0ce09-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ce09-118">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="0ce09-118">-StartTime</span></span>
<span data-ttu-id="0ce09-119">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="0ce09-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce09-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="0ce09-120">-Stream</span></span>
<span data-ttu-id="0ce09-121">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce09-121">Specifies the type of output.</span></span>
<span data-ttu-id="0ce09-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0ce09-122">Valid values are:</span></span> 

- <span data-ttu-id="0ce09-123">Bármely</span><span class="sxs-lookup"><span data-stu-id="0ce09-123">Any</span></span>
- <span data-ttu-id="0ce09-124">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="0ce09-124">Debug</span></span>
- <span data-ttu-id="0ce09-125">Hiba</span><span class="sxs-lookup"><span data-stu-id="0ce09-125">Error</span></span>
- <span data-ttu-id="0ce09-126">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="0ce09-126">Output</span></span>
- <span data-ttu-id="0ce09-127">Haladás</span><span class="sxs-lookup"><span data-stu-id="0ce09-127">Progress</span></span>
- <span data-ttu-id="0ce09-128">Részletes</span><span class="sxs-lookup"><span data-stu-id="0ce09-128">Verbose</span></span>
- <span data-ttu-id="0ce09-129">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="0ce09-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce09-130">CommonParameters</span></span>
<span data-ttu-id="0ce09-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ce09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce09-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce09-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce09-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce09-133">INPUTS</span></span>

## <span data-ttu-id="0ce09-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce09-134">OUTPUTS</span></span>

## <span data-ttu-id="0ce09-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ce09-135">NOTES</span></span>

## <span data-ttu-id="0ce09-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ce09-136">RELATED LINKS</span></span>

[<span data-ttu-id="0ce09-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0ce09-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="0ce09-138">Önéletrajz – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0ce09-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="0ce09-139">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0ce09-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="0ce09-140">Felfüggesztés – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0ce09-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


