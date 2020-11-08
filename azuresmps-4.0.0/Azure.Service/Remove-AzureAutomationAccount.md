---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016495"
---
# <span data-ttu-id="3fbb5-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3fbb5-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="3fbb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3fbb5-102">SYNOPSIS</span></span>

<span data-ttu-id="3fbb5-103">Automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3fbb5-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="3fbb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3fbb5-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3fbb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3fbb5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3fbb5-106">A **Remove-AzureAutomationAccount** parancsmag eltávolítja a fiókot a Microsoft Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3fbb5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3fbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="3fbb5-108">1. példa: automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3fbb5-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="3fbb5-109">Ez a parancs eltávolítja a MyAutomationAccount nevű automatizálási fiókot a felhasználó érvényesítése kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="3fbb5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3fbb5-110">PARAMETERS</span></span>

### <span data-ttu-id="3fbb5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3fbb5-111">-Force</span></span>
<span data-ttu-id="3fbb5-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fbb5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3fbb5-113">-Name</span></span>
<span data-ttu-id="3fbb5-114">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbb5-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="3fbb5-115">-Profile</span></span>
<span data-ttu-id="3fbb5-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fbb5-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fbb5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbb5-118">CommonParameters</span></span>
<span data-ttu-id="3fbb5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3fbb5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbb5-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fbb5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbb5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fbb5-121">INPUTS</span></span>

## <span data-ttu-id="3fbb5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fbb5-122">OUTPUTS</span></span>

## <span data-ttu-id="3fbb5-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3fbb5-123">NOTES</span></span>

## <span data-ttu-id="3fbb5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fbb5-124">RELATED LINKS</span></span>

[<span data-ttu-id="3fbb5-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3fbb5-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="3fbb5-126">Új – AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3fbb5-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


