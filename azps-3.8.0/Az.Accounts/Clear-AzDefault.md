---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: aae604f28b2a7eebae62d290b3c1ab6905d9a15a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013039"
---
# <span data-ttu-id="b7bb3-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="b7bb3-101">Clear-AzDefault</span></span>

## <span data-ttu-id="b7bb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bb3-103">Törli a felhasználó által az aktuális környezetben beállított alapértékeket.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="b7bb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7bb3-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7bb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="b7bb3-106">A Clear-AzDefault parancsmag a felhasználó által megadott kapcsoló paramétertől függően eltávolítja a felhasználó által megadott alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="b7bb3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7bb3-107">EXAMPLES</span></span>

### <span data-ttu-id="b7bb3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7bb3-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="b7bb3-109">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított összes alapértelmezett beállítást.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="b7bb3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7bb3-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="b7bb3-111">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított alapértelmezett erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="b7bb3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7bb3-112">PARAMETERS</span></span>

### <span data-ttu-id="b7bb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bb3-113">-DefaultProfile</span></span>
<span data-ttu-id="b7bb3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7bb3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b7bb3-115">-Force</span></span>
<span data-ttu-id="b7bb3-116">Az összes alapértelmezett érték eltávolítása, ha nincs alapértelmezett megadva</span><span class="sxs-lookup"><span data-stu-id="b7bb3-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="b7bb3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7bb3-117">-PassThru</span></span>
<span data-ttu-id="b7bb3-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b7bb3-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7bb3-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7bb3-119">-ResourceGroup</span></span>
<span data-ttu-id="b7bb3-120">Az alapértelmezett erőforráscsoport törlése</span><span class="sxs-lookup"><span data-stu-id="b7bb3-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7bb3-121">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b7bb3-121">-Scope</span></span>
<span data-ttu-id="b7bb3-122">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b7bb3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7bb3-123">-Confirm</span></span>
<span data-ttu-id="b7bb3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7bb3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7bb3-125">-WhatIf</span></span>
<span data-ttu-id="b7bb3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7bb3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7bb3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7bb3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bb3-128">CommonParameters</span></span>
<span data-ttu-id="b7bb3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7bb3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bb3-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7bb3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bb3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7bb3-131">INPUTS</span></span>

### <span data-ttu-id="b7bb3-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b7bb3-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b7bb3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7bb3-133">OUTPUTS</span></span>

### <span data-ttu-id="b7bb3-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7bb3-134">System.Boolean</span></span>

## <span data-ttu-id="b7bb3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7bb3-135">NOTES</span></span>

## <span data-ttu-id="b7bb3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7bb3-136">RELATED LINKS</span></span>
