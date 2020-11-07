---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 9dcf7b7d7149235d5a2ed211dbccf87415f1c496
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840941"
---
# <span data-ttu-id="b81bc-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="b81bc-101">Clear-AzContext</span></span>

## <span data-ttu-id="b81bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b81bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b81bc-103">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b81bc-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="b81bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b81bc-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b81bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b81bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b81bc-106">Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b81bc-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="b81bc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b81bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b81bc-108">Globális környezet törlése</span><span class="sxs-lookup"><span data-stu-id="b81bc-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="b81bc-109">Az összes fiók, előfizetés és hitelesítőadat-adat eltávolítása bármely PowerShell-munkamenethez</span><span class="sxs-lookup"><span data-stu-id="b81bc-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="b81bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b81bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b81bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81bc-111">-DefaultProfile</span></span>
<span data-ttu-id="b81bc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b81bc-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b81bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b81bc-113">-Force</span></span>
<span data-ttu-id="b81bc-114">Az összes felhasználó és csoport törlése a globális hatókörből figyelmeztetés nélkül</span><span class="sxs-lookup"><span data-stu-id="b81bc-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="b81bc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b81bc-115">-PassThru</span></span>
<span data-ttu-id="b81bc-116">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="b81bc-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="b81bc-117">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b81bc-117">-Scope</span></span>
<span data-ttu-id="b81bc-118">Törölje a csak az aktuális PowerShell-munkamenet vagy az összes munkamenet környezetét.</span><span class="sxs-lookup"><span data-stu-id="b81bc-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="b81bc-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b81bc-119">-Confirm</span></span>
<span data-ttu-id="b81bc-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b81bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b81bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b81bc-121">-WhatIf</span></span>
<span data-ttu-id="b81bc-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b81bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b81bc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b81bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b81bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81bc-124">CommonParameters</span></span>
<span data-ttu-id="b81bc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b81bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81bc-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b81bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81bc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81bc-127">INPUTS</span></span>

### <span data-ttu-id="b81bc-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="b81bc-128">None</span></span>

## <span data-ttu-id="b81bc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81bc-129">OUTPUTS</span></span>

### <span data-ttu-id="b81bc-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b81bc-130">System.Boolean</span></span>

## <span data-ttu-id="b81bc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b81bc-131">NOTES</span></span>

## <span data-ttu-id="b81bc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b81bc-132">RELATED LINKS</span></span>
