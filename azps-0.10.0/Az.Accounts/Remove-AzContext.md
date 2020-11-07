---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: accea2f11e00cecf3771e87e14a42a446a75367d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841041"
---
# <span data-ttu-id="76eda-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="76eda-101">Remove-AzContext</span></span>

## <span data-ttu-id="76eda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76eda-102">SYNOPSIS</span></span>
<span data-ttu-id="76eda-103">Környezet eltávolítása az elérhető környezetek halmazból</span><span class="sxs-lookup"><span data-stu-id="76eda-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="76eda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76eda-104">SYNTAX</span></span>

### <span data-ttu-id="76eda-105">RemoveByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76eda-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76eda-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="76eda-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="76eda-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76eda-107">DESCRIPTION</span></span>
<span data-ttu-id="76eda-108">Azure-környezet eltávolítása a kontextusok halmazból</span><span class="sxs-lookup"><span data-stu-id="76eda-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="76eda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76eda-109">EXAMPLES</span></span>

### <span data-ttu-id="76eda-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76eda-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="76eda-111">Az alapértelmezett nevű környezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="76eda-111">Remove the context named default</span></span>

## <span data-ttu-id="76eda-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76eda-112">PARAMETERS</span></span>

### <span data-ttu-id="76eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76eda-113">-DefaultProfile</span></span>
<span data-ttu-id="76eda-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76eda-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76eda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="76eda-115">-Force</span></span>
<span data-ttu-id="76eda-116">A környezet eltávolítása annak ellenére, hogy az alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="76eda-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="76eda-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76eda-117">-InputObject</span></span>
<span data-ttu-id="76eda-118">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="76eda-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="76eda-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76eda-119">-Name</span></span>
<span data-ttu-id="76eda-120">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="76eda-120">The name of the context</span></span>

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

### <span data-ttu-id="76eda-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76eda-121">-PassThru</span></span>
<span data-ttu-id="76eda-122">Az eltávolított környezet visszaküldése</span><span class="sxs-lookup"><span data-stu-id="76eda-122">Return the removed context</span></span>

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

### <span data-ttu-id="76eda-123">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="76eda-123">-Scope</span></span>
<span data-ttu-id="76eda-124">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="76eda-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="76eda-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76eda-125">-Confirm</span></span>
<span data-ttu-id="76eda-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76eda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76eda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76eda-127">-WhatIf</span></span>
<span data-ttu-id="76eda-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76eda-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76eda-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76eda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76eda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76eda-130">CommonParameters</span></span>
<span data-ttu-id="76eda-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76eda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76eda-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76eda-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76eda-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76eda-133">INPUTS</span></span>

### <span data-ttu-id="76eda-134">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="76eda-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="76eda-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76eda-135">OUTPUTS</span></span>

### <span data-ttu-id="76eda-136">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="76eda-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="76eda-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76eda-137">NOTES</span></span>

## <span data-ttu-id="76eda-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76eda-138">RELATED LINKS</span></span>
