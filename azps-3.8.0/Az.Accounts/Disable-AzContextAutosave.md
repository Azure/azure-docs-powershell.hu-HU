---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: c5d01fcc7ba007a0336fac5c08db44b840e75806
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013030"
---
# <span data-ttu-id="52b66-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="52b66-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="52b66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52b66-102">SYNOPSIS</span></span>
<span data-ttu-id="52b66-103">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="52b66-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="52b66-104">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="52b66-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="52b66-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52b66-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b66-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="52b66-106">DESCRIPTION</span></span>
<span data-ttu-id="52b66-107">Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="52b66-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="52b66-108">A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait</span><span class="sxs-lookup"><span data-stu-id="52b66-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="52b66-109">Példák</span><span class="sxs-lookup"><span data-stu-id="52b66-109">EXAMPLES</span></span>

### <span data-ttu-id="52b66-110">A környezet automatikus mentésének letiltása</span><span class="sxs-lookup"><span data-stu-id="52b66-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="52b66-111">Tiltsa le az automatikus mentés funkciót az aktuális felhasználónál.</span><span class="sxs-lookup"><span data-stu-id="52b66-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="52b66-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52b66-112">PARAMETERS</span></span>

### <span data-ttu-id="52b66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b66-113">-DefaultProfile</span></span>
<span data-ttu-id="52b66-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52b66-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52b66-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="52b66-115">-Scope</span></span>
<span data-ttu-id="52b66-116">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="52b66-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="52b66-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52b66-117">-Confirm</span></span>
<span data-ttu-id="52b66-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52b66-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b66-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b66-119">-WhatIf</span></span>
<span data-ttu-id="52b66-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52b66-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b66-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52b66-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b66-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b66-122">CommonParameters</span></span>
<span data-ttu-id="52b66-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52b66-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b66-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b66-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b66-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52b66-125">INPUTS</span></span>

### <span data-ttu-id="52b66-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="52b66-126">None</span></span>

## <span data-ttu-id="52b66-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52b66-127">OUTPUTS</span></span>

### <span data-ttu-id="52b66-128">Microsoft. Azure. commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="52b66-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="52b66-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52b66-129">NOTES</span></span>

## <span data-ttu-id="52b66-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52b66-130">RELATED LINKS</span></span>
