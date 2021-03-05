---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010101"
---
# <span data-ttu-id="a0b4d-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="a0b4d-101">Set-AzDefault</span></span>

## <span data-ttu-id="a0b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b4d-103">Alapértelmezett beállítás az aktuális környezetben</span><span class="sxs-lookup"><span data-stu-id="a0b4d-103">Sets a default in the current context</span></span>

## <span data-ttu-id="a0b4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0b4d-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b4d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b4d-106">A Set-AzDefault parancsmag hozzáadja vagy módosítja az alapértelmezett értékeket az aktuális környezetben.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="a0b4d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b4d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0b4d-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a0b4d-109">Ez a parancs az alapértelmezett erőforráscsoportot a felhasználó által megadott erőforráscsoportra állítja be.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="a0b4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b4d-111">-DefaultProfile</span></span>
<span data-ttu-id="a0b4d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0b4d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a0b4d-113">-Force</span></span>
<span data-ttu-id="a0b4d-114">Új erőforráscsoport létrehozása, ha az alapértelmezett beállítás nem létezik</span><span class="sxs-lookup"><span data-stu-id="a0b4d-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="a0b4d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b4d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0b4d-116">Az alapértelmezettként beállított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a0b4d-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b4d-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="a0b4d-117">-Scope</span></span>
<span data-ttu-id="a0b4d-118">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a0b4d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0b4d-119">-Confirm</span></span>
<span data-ttu-id="a0b4d-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0b4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b4d-121">-WhatIf</span></span>
<span data-ttu-id="a0b4d-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0b4d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0b4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b4d-124">CommonParameters</span></span>
<span data-ttu-id="a0b4d-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b4d-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0b4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b4d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0b4d-127">INPUTS</span></span>

### <span data-ttu-id="a0b4d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a0b4d-128">System.String</span></span>

## <span data-ttu-id="a0b4d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0b4d-129">OUTPUTS</span></span>

### <span data-ttu-id="a0b4d-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0b4d-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a0b4d-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0b4d-131">NOTES</span></span>

## <span data-ttu-id="a0b4d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0b4d-132">RELATED LINKS</span></span>
