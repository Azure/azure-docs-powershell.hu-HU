---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015462"
---
# <span data-ttu-id="97178-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97178-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="97178-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97178-102">SYNOPSIS</span></span>

<span data-ttu-id="97178-103">Befejezi a felfüggesztett automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="97178-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="97178-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97178-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="97178-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97178-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="97178-106">A **resume-AzureAutomationJob** parancsmag folytatja a felfüggesztett Microsoft Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="97178-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="97178-107">Használja az *azonosító* paramétert a felfüggesztett feladat megadásához.</span><span class="sxs-lookup"><span data-stu-id="97178-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="97178-108">A feladat felfüggesztéséhez használja az Suspend-AzureAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="97178-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="97178-109">Példák</span><span class="sxs-lookup"><span data-stu-id="97178-109">EXAMPLES</span></span>

### <span data-ttu-id="97178-110">1. példa: felfüggesztett feladat folytatása</span><span class="sxs-lookup"><span data-stu-id="97178-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="97178-111">Ez a parancs folytatja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="97178-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="97178-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97178-112">PARAMETERS</span></span>

### <span data-ttu-id="97178-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97178-113">-AutomationAccountName</span></span>
<span data-ttu-id="97178-114">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97178-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="97178-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="97178-115">-Id</span></span>
<span data-ttu-id="97178-116">Egy feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="97178-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="97178-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="97178-117">-Profile</span></span>
<span data-ttu-id="97178-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="97178-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97178-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="97178-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97178-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97178-120">CommonParameters</span></span>
<span data-ttu-id="97178-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97178-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97178-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97178-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97178-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97178-123">INPUTS</span></span>

## <span data-ttu-id="97178-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97178-124">OUTPUTS</span></span>

## <span data-ttu-id="97178-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97178-125">NOTES</span></span>

## <span data-ttu-id="97178-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97178-126">RELATED LINKS</span></span>

[<span data-ttu-id="97178-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97178-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="97178-128">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97178-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="97178-129">Felfüggesztés – AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97178-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


