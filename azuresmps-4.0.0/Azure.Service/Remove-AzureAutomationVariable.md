---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016169"
---
# <span data-ttu-id="8f854-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f854-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="8f854-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f854-102">SYNOPSIS</span></span>

<span data-ttu-id="8f854-103">Automatizálási változó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8f854-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="8f854-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f854-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f854-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f854-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8f854-106">A **Remove-AzureAutomationVariable** parancsmag egy változót távolít el a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="8f854-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="8f854-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f854-107">EXAMPLES</span></span>

### <span data-ttu-id="8f854-108">Példa 1: változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8f854-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="8f854-109">Ez a parancs eltávolítja a MyStringVariable nevű változót a Contoso17 nevű automatizálási fiókban a felhasználó érvényesítése kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8f854-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="8f854-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f854-110">PARAMETERS</span></span>

### <span data-ttu-id="8f854-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f854-111">-AutomationAccountName</span></span>
<span data-ttu-id="8f854-112">A változóval rendelkező automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f854-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="8f854-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8f854-113">-Force</span></span>
<span data-ttu-id="8f854-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8f854-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f854-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f854-115">-Name</span></span>
<span data-ttu-id="8f854-116">A változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f854-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="8f854-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8f854-117">-Profile</span></span>
<span data-ttu-id="8f854-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8f854-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f854-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8f854-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f854-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f854-120">CommonParameters</span></span>
<span data-ttu-id="8f854-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f854-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f854-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f854-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f854-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f854-123">INPUTS</span></span>

## <span data-ttu-id="8f854-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f854-124">OUTPUTS</span></span>

## <span data-ttu-id="8f854-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f854-125">NOTES</span></span>

## <span data-ttu-id="8f854-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f854-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f854-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f854-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="8f854-128">Új – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f854-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="8f854-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f854-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


