---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016481"
---
# <span data-ttu-id="a1c76-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a1c76-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="a1c76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1c76-102">SYNOPSIS</span></span>

<span data-ttu-id="a1c76-103">Modul eltávolítása az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="a1c76-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="a1c76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1c76-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1c76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1c76-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a1c76-106">A **Remove-AzureAutomationModule** parancsmag egy automatizálási fiókot távolít el a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a1c76-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a1c76-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1c76-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c76-108">1. példa: modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a1c76-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="a1c76-109">Ez a parancs eltávolítja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="a1c76-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a1c76-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1c76-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c76-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1c76-111">-AutomationAccountName</span></span>
<span data-ttu-id="a1c76-112">A modulhoz tartozó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c76-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="a1c76-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a1c76-113">-Force</span></span>
<span data-ttu-id="a1c76-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a1c76-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1c76-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1c76-115">-Name</span></span>
<span data-ttu-id="a1c76-116">Az eltávolítandó modul nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1c76-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="a1c76-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a1c76-117">-Profile</span></span>
<span data-ttu-id="a1c76-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a1c76-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1c76-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a1c76-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1c76-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c76-120">CommonParameters</span></span>
<span data-ttu-id="a1c76-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1c76-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c76-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c76-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c76-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1c76-123">INPUTS</span></span>

## <span data-ttu-id="a1c76-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1c76-124">OUTPUTS</span></span>

## <span data-ttu-id="a1c76-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1c76-125">NOTES</span></span>

## <span data-ttu-id="a1c76-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1c76-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1c76-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a1c76-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="a1c76-128">Új – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a1c76-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="a1c76-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a1c76-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


