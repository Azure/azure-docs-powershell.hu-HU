---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b54cfdc68c1f6c400decdac9a1ef0f49823a1712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668280"
---
# <span data-ttu-id="6320c-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="6320c-101">Clear-AzContext</span></span>

## <span data-ttu-id="6320c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6320c-102">SYNOPSIS</span></span>
<span data-ttu-id="6320c-103">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6320c-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="6320c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6320c-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6320c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6320c-105">DESCRIPTION</span></span>
<span data-ttu-id="6320c-106">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6320c-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="6320c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6320c-107">EXAMPLES</span></span>

### <span data-ttu-id="6320c-108">Globális környezet törlése</span><span class="sxs-lookup"><span data-stu-id="6320c-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="6320c-109">Az összes fiók, előfizetés és hitelesítőadat-adat eltávolítása bármely PowerShell-munkamenethez</span><span class="sxs-lookup"><span data-stu-id="6320c-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="6320c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6320c-110">PARAMETERS</span></span>

### <span data-ttu-id="6320c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6320c-111">-DefaultProfile</span></span>
<span data-ttu-id="6320c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6320c-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6320c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6320c-113">-Force</span></span>
<span data-ttu-id="6320c-114">Az összes felhasználó és csoport törlése a globális hatókörből figyelmeztetés nélkül</span><span class="sxs-lookup"><span data-stu-id="6320c-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6320c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6320c-115">-PassThru</span></span>
<span data-ttu-id="6320c-116">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="6320c-116">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6320c-117">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="6320c-117">-Scope</span></span>
<span data-ttu-id="6320c-118">Törölje a csak az aktuális PowerShell-munkamenet vagy az összes munkamenet környezetét.</span><span class="sxs-lookup"><span data-stu-id="6320c-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="6320c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6320c-119">-Confirm</span></span>
<span data-ttu-id="6320c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6320c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6320c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6320c-121">-WhatIf</span></span>
<span data-ttu-id="6320c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6320c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6320c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6320c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6320c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6320c-124">CommonParameters</span></span>
<span data-ttu-id="6320c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6320c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6320c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6320c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6320c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6320c-127">INPUTS</span></span>

### <span data-ttu-id="6320c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="6320c-128">None</span></span>

## <span data-ttu-id="6320c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6320c-129">OUTPUTS</span></span>

### <span data-ttu-id="6320c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6320c-130">System.Boolean</span></span>

## <span data-ttu-id="6320c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6320c-131">NOTES</span></span>

## <span data-ttu-id="6320c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6320c-132">RELATED LINKS</span></span>
