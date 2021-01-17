---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479194"
---
# <span data-ttu-id="aa8ae-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="aa8ae-101">Clear-AzDefault</span></span>

## <span data-ttu-id="aa8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8ae-103">Törli a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="aa8ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa8ae-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa8ae-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="aa8ae-106">A Clear-AzDefault parancsmag eltávolítja a felhasználó által beállított alapértelmezett értékeket a felhasználó által megadott kapcsolóparaméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="aa8ae-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa8ae-107">EXAMPLES</span></span>

### <span data-ttu-id="aa8ae-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="aa8ae-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="aa8ae-109">Ez a parancs eltávolítja a felhasználó által az aktuális környezetben beállított összes alapértelmezett beállítást.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="aa8ae-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="aa8ae-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="aa8ae-111">Ez a parancs eltávolítja a felhasználó által beállított alapértelmezett erőforráscsoportot az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="aa8ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa8ae-112">PARAMETERS</span></span>

### <span data-ttu-id="aa8ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8ae-113">-DefaultProfile</span></span>
<span data-ttu-id="aa8ae-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa8ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aa8ae-115">-Force</span></span>
<span data-ttu-id="aa8ae-116">Az összes alapértelmezett eltávolítása, ha nincs megadva alapértelmezett beállítás</span><span class="sxs-lookup"><span data-stu-id="aa8ae-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="aa8ae-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa8ae-117">-PassThru</span></span>
<span data-ttu-id="aa8ae-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aa8ae-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aa8ae-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aa8ae-119">-ResourceGroup</span></span>
<span data-ttu-id="aa8ae-120">Alapértelmezett erőforráscsoport ürítása</span><span class="sxs-lookup"><span data-stu-id="aa8ae-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="aa8ae-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="aa8ae-121">-Scope</span></span>
<span data-ttu-id="aa8ae-122">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="aa8ae-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa8ae-123">-Confirm</span></span>
<span data-ttu-id="aa8ae-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa8ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa8ae-125">-WhatIf</span></span>
<span data-ttu-id="aa8ae-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa8ae-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa8ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8ae-128">CommonParameters</span></span>
<span data-ttu-id="aa8ae-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa8ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8ae-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa8ae-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8ae-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa8ae-131">INPUTS</span></span>

### <span data-ttu-id="aa8ae-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa8ae-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa8ae-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa8ae-133">OUTPUTS</span></span>

### <span data-ttu-id="aa8ae-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa8ae-134">System.Boolean</span></span>

## <span data-ttu-id="aa8ae-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa8ae-135">NOTES</span></span>

## <span data-ttu-id="aa8ae-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa8ae-136">RELATED LINKS</span></span>
