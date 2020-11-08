---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016032"
---
# <span data-ttu-id="1d11c-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="1d11c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d11c-102">SYNOPSIS</span></span>

<span data-ttu-id="1d11c-103">Elindít egy runbook-feladatot.</span><span class="sxs-lookup"><span data-stu-id="1d11c-103">Starts a runbook job.</span></span>

## <span data-ttu-id="1d11c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d11c-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1d11c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d11c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1d11c-106">A **Start-AzureAutomationRunbook** parancsmag elindítja a Microsoft Azure automatizálási runbook munkáját.</span><span class="sxs-lookup"><span data-stu-id="1d11c-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="1d11c-107">Adja meg a runbook AZONOSÍTÓját vagy nevét.</span><span class="sxs-lookup"><span data-stu-id="1d11c-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="1d11c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1d11c-108">EXAMPLES</span></span>

### <span data-ttu-id="1d11c-109">1. példa: runbook-feladat indítása</span><span class="sxs-lookup"><span data-stu-id="1d11c-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="1d11c-110">Ez a parancs runbook-feladatot indít az Contoso17 nevű automatizálási fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="1d11c-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d11c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d11c-111">PARAMETERS</span></span>

### <span data-ttu-id="1d11c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d11c-112">-AutomationAccountName</span></span>
<span data-ttu-id="1d11c-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d11c-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="1d11c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d11c-114">-Name</span></span>
<span data-ttu-id="1d11c-115">Egy runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d11c-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="1d11c-116">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="1d11c-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d11c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="1d11c-117">-Profile</span></span>
<span data-ttu-id="1d11c-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1d11c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d11c-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1d11c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d11c-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="1d11c-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d11c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d11c-121">CommonParameters</span></span>
<span data-ttu-id="1d11c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d11c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d11c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d11c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d11c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d11c-124">INPUTS</span></span>

## <span data-ttu-id="1d11c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d11c-125">OUTPUTS</span></span>

### <span data-ttu-id="1d11c-126">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="1d11c-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="1d11c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d11c-127">NOTES</span></span>

## <span data-ttu-id="1d11c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d11c-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d11c-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="1d11c-130">Új – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="1d11c-131">Közzététel – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="1d11c-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="1d11c-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d11c-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


