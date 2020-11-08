---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016368"
---
# <span data-ttu-id="d3c0e-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3c0e-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="d3c0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3c0e-102">SYNOPSIS</span></span>

<span data-ttu-id="d3c0e-103">Az Azure automatizálási moduljának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3c0e-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="d3c0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3c0e-104">SYNTAX</span></span>

### <span data-ttu-id="d3c0e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3c0e-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3c0e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d3c0e-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3c0e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3c0e-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d3c0e-108">A **Get-AzureAutomationModule** parancsmag egy vagy több Microsoft Azure automatizálási modult kap.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="d3c0e-109">Alapértelmezés szerint az összes modult adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-109">By default, all modules are returned.</span></span>
<span data-ttu-id="d3c0e-110">Ha egy adott modult szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="d3c0e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d3c0e-111">EXAMPLES</span></span>

### <span data-ttu-id="d3c0e-112">Példa 1: az összes modul beolvasása</span><span class="sxs-lookup"><span data-stu-id="d3c0e-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d3c0e-113">Ez a parancs a Contoso17 nevű Azure automatizálási fiók összes modulját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d3c0e-114">2. példa: modul beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3c0e-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="d3c0e-115">Ez a parancs egy ContosoModule nevű modult kap a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d3c0e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3c0e-116">PARAMETERS</span></span>

### <span data-ttu-id="d3c0e-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3c0e-117">-AutomationAccountName</span></span>
<span data-ttu-id="d3c0e-118">A lekérdezni kívánt automatizálási fiók nevét adja meg a runbook.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="d3c0e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3c0e-119">-Name</span></span>
<span data-ttu-id="d3c0e-120">A lekérdezni kívánt modul nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c0e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3c0e-121">-Profile</span></span>
<span data-ttu-id="d3c0e-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3c0e-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d3c0e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3c0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c0e-124">CommonParameters</span></span>
<span data-ttu-id="d3c0e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3c0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c0e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c0e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3c0e-127">INPUTS</span></span>

## <span data-ttu-id="d3c0e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3c0e-128">OUTPUTS</span></span>

### <span data-ttu-id="d3c0e-129">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="d3c0e-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d3c0e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3c0e-130">NOTES</span></span>

## <span data-ttu-id="d3c0e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3c0e-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3c0e-132">Új – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3c0e-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="d3c0e-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3c0e-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="d3c0e-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3c0e-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


