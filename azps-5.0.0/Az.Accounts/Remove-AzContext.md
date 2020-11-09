---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300053"
---
# <span data-ttu-id="cc0b8-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="cc0b8-101">Remove-AzContext</span></span>

## <span data-ttu-id="cc0b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0b8-103">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="cc0b8-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="cc0b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc0b8-104">SYNTAX</span></span>

### <span data-ttu-id="cc0b8-105">RemoveByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc0b8-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc0b8-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="cc0b8-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="cc0b8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc0b8-107">DESCRIPTION</span></span>
<span data-ttu-id="cc0b8-108">Azure-környezet eltávolítása a kontextusok halmazból</span><span class="sxs-lookup"><span data-stu-id="cc0b8-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="cc0b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc0b8-109">EXAMPLES</span></span>

### <span data-ttu-id="cc0b8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc0b8-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="cc0b8-111">Az alapértelmezett nevű környezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cc0b8-111">Remove the context named default</span></span>

## <span data-ttu-id="cc0b8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc0b8-112">PARAMETERS</span></span>

### <span data-ttu-id="cc0b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0b8-113">-DefaultProfile</span></span>
<span data-ttu-id="cc0b8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc0b8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc0b8-115">-Force</span></span>
<span data-ttu-id="cc0b8-116">A környezet eltávolítása annak ellenére, hogy az alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="cc0b8-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="cc0b8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc0b8-117">-InputObject</span></span>
<span data-ttu-id="cc0b8-118">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc0b8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc0b8-119">-Name</span></span>
<span data-ttu-id="cc0b8-120">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="cc0b8-120">The name of the context</span></span>

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

### <span data-ttu-id="cc0b8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc0b8-121">-PassThru</span></span>
<span data-ttu-id="cc0b8-122">Az eltávolított környezet visszaküldése</span><span class="sxs-lookup"><span data-stu-id="cc0b8-122">Return the removed context</span></span>

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

### <span data-ttu-id="cc0b8-123">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="cc0b8-123">-Scope</span></span>
<span data-ttu-id="cc0b8-124">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="cc0b8-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc0b8-125">-Confirm</span></span>
<span data-ttu-id="cc0b8-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc0b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc0b8-127">-WhatIf</span></span>
<span data-ttu-id="cc0b8-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc0b8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc0b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc0b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0b8-130">CommonParameters</span></span>
<span data-ttu-id="cc0b8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc0b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0b8-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc0b8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0b8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0b8-133">INPUTS</span></span>

### <span data-ttu-id="cc0b8-134">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="cc0b8-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="cc0b8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc0b8-135">OUTPUTS</span></span>

### <span data-ttu-id="cc0b8-136">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="cc0b8-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="cc0b8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc0b8-137">NOTES</span></span>

## <span data-ttu-id="cc0b8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc0b8-138">RELATED LINKS</span></span>
