---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 43681bb4dc4208eb8f12acc39d171f5ab6821dfa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013032"
---
# <span data-ttu-id="f6a26-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="f6a26-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="f6a26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6a26-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a26-103">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="f6a26-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="f6a26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6a26-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6a26-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a26-106">A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők.</span><span class="sxs-lookup"><span data-stu-id="f6a26-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="f6a26-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6a26-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a26-108">Az aktuális felhasználó automatikus mentésére vonatkozó hitelesítő adatok engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f6a26-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="f6a26-109">A hitelesítő adatok automatikus mentésének bekapcsolása az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="f6a26-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="f6a26-110">Minden alkalommal, amikor egy PowerShell-ablak van megnyitva, a jelenlegi környezete bejelentkezés nélkül emlékezni fog.</span><span class="sxs-lookup"><span data-stu-id="f6a26-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="f6a26-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6a26-111">PARAMETERS</span></span>

### <span data-ttu-id="f6a26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a26-112">-DefaultProfile</span></span>
<span data-ttu-id="f6a26-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f6a26-113">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a26-114">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="f6a26-114">-Scope</span></span>
<span data-ttu-id="f6a26-115">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="f6a26-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a26-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6a26-116">-Confirm</span></span>
<span data-ttu-id="f6a26-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6a26-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a26-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a26-118">-WhatIf</span></span>
<span data-ttu-id="f6a26-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6a26-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a26-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6a26-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a26-121">CommonParameters</span></span>
<span data-ttu-id="f6a26-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6a26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a26-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a26-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a26-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6a26-124">INPUTS</span></span>

### <span data-ttu-id="f6a26-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f6a26-125">None</span></span>

## <span data-ttu-id="f6a26-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6a26-126">OUTPUTS</span></span>

### <span data-ttu-id="f6a26-127">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="f6a26-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="f6a26-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6a26-128">NOTES</span></span>

## <span data-ttu-id="f6a26-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6a26-129">RELATED LINKS</span></span>
