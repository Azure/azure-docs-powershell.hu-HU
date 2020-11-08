---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015942"
---
# <span data-ttu-id="4875c-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4875c-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="4875c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4875c-102">SYNOPSIS</span></span>

<span data-ttu-id="4875c-103">Automatizálási feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="4875c-103">Stops an Automation job.</span></span>

## <span data-ttu-id="4875c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4875c-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4875c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4875c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4875c-106">A **stop-AzureAutomationJob** parancsmag leállítja a Microsoft Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="4875c-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="4875c-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="4875c-107">Specify a running automation job.</span></span>

## <span data-ttu-id="4875c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4875c-108">EXAMPLES</span></span>

### <span data-ttu-id="4875c-109">Példa 1: feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="4875c-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="4875c-110">Ez a parancs leállítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="4875c-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="4875c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4875c-111">PARAMETERS</span></span>

### <span data-ttu-id="4875c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4875c-112">-AutomationAccountName</span></span>
<span data-ttu-id="4875c-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4875c-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4875c-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4875c-114">-Id</span></span>
<span data-ttu-id="4875c-115">Egy feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4875c-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="4875c-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="4875c-116">-Profile</span></span>
<span data-ttu-id="4875c-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4875c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4875c-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4875c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4875c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4875c-119">CommonParameters</span></span>
<span data-ttu-id="4875c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4875c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4875c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4875c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4875c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4875c-122">INPUTS</span></span>

## <span data-ttu-id="4875c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4875c-123">OUTPUTS</span></span>

## <span data-ttu-id="4875c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4875c-124">NOTES</span></span>

## <span data-ttu-id="4875c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4875c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4875c-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4875c-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="4875c-127">Önéletrajz – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4875c-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="4875c-128">Felfüggesztés – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4875c-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


