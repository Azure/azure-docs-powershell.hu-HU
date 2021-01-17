---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469189"
---
# <span data-ttu-id="8b995-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="8b995-101">Remove-AzContext</span></span>

## <span data-ttu-id="8b995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b995-102">SYNOPSIS</span></span>
<span data-ttu-id="8b995-103">Környezet eltávolítása az elérhető környezetek készletből</span><span class="sxs-lookup"><span data-stu-id="8b995-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="8b995-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b995-104">SYNTAX</span></span>

### <span data-ttu-id="8b995-105">RemoveByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b995-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b995-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="8b995-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="8b995-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b995-107">DESCRIPTION</span></span>
<span data-ttu-id="8b995-108">Azure-környezet eltávolítása a környezetek készletből</span><span class="sxs-lookup"><span data-stu-id="8b995-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="8b995-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b995-109">EXAMPLES</span></span>

### <span data-ttu-id="8b995-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8b995-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="8b995-111">Az alapértelmezettnek nevezett környezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8b995-111">Remove the context named default</span></span>

## <span data-ttu-id="8b995-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b995-112">PARAMETERS</span></span>

### <span data-ttu-id="8b995-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b995-113">-DefaultProfile</span></span>
<span data-ttu-id="8b995-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b995-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b995-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b995-115">-Force</span></span>
<span data-ttu-id="8b995-116">Környezet eltávolítása akkor is, ha az az alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8b995-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="8b995-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b995-117">-InputObject</span></span>
<span data-ttu-id="8b995-118">A context object, normally passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b995-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b995-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8b995-119">-Name</span></span>
<span data-ttu-id="8b995-120">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="8b995-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b995-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b995-121">-PassThru</span></span>
<span data-ttu-id="8b995-122">Az eltávolított környezet visszaadja</span><span class="sxs-lookup"><span data-stu-id="8b995-122">Return the removed context</span></span>

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

### <span data-ttu-id="8b995-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="8b995-123">-Scope</span></span>
<span data-ttu-id="8b995-124">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e</span><span class="sxs-lookup"><span data-stu-id="8b995-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="8b995-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b995-125">-Confirm</span></span>
<span data-ttu-id="8b995-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8b995-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b995-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b995-127">-WhatIf</span></span>
<span data-ttu-id="8b995-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8b995-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b995-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b995-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b995-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b995-130">CommonParameters</span></span>
<span data-ttu-id="8b995-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b995-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b995-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b995-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b995-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b995-133">INPUTS</span></span>

### <span data-ttu-id="8b995-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="8b995-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="8b995-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b995-135">OUTPUTS</span></span>

### <span data-ttu-id="8b995-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="8b995-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="8b995-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b995-137">NOTES</span></span>

## <span data-ttu-id="8b995-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b995-138">RELATED LINKS</span></span>
