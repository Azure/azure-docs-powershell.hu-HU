---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925385"
---
# <span data-ttu-id="a2402-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="a2402-101">Rename-AzContext</span></span>

## <span data-ttu-id="a2402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2402-102">SYNOPSIS</span></span>
<span data-ttu-id="a2402-103">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="a2402-103">Rename an Azure context.</span></span>  <span data-ttu-id="a2402-104">Az alapértelmezett környezetek neve felhasználói fiók és előfizetés szerint van elnevezve.</span><span class="sxs-lookup"><span data-stu-id="a2402-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="a2402-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2402-105">SYNTAX</span></span>

### <span data-ttu-id="a2402-106">RenameByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2402-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="a2402-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="a2402-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="a2402-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2402-108">DESCRIPTION</span></span>
<span data-ttu-id="a2402-109">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="a2402-109">Rename an Azure context.</span></span>  <span data-ttu-id="a2402-110">Az alapértelmezett környezetek neve felhasználói fiók és előfizetés szerint van elnevezve.</span><span class="sxs-lookup"><span data-stu-id="a2402-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="a2402-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2402-111">EXAMPLES</span></span>

### <span data-ttu-id="a2402-112">1. példa: Környezet átnevezése elnevezett paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a2402-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="a2402-113">A '' környezetének átnevezése user1@contoso.org az előfizetésben ('12345-6789-2345-3567890') "Munka" névre.</span><span class="sxs-lookup"><span data-stu-id="a2402-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="a2402-114">A parancs után a "Select-AzContext Work" paranccsal megcélzható a környezet.</span><span class="sxs-lookup"><span data-stu-id="a2402-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="a2402-115">A Tab billentyűvel végiglaposulhat a "SourceName" értéken a tabulátor befejezésével.</span><span class="sxs-lookup"><span data-stu-id="a2402-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="a2402-116">2. példa: Környezet átnevezése pozicionális paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a2402-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="a2402-117">Nevezze át a "Saját környezet" környezet nevét "Munka" névre.</span><span class="sxs-lookup"><span data-stu-id="a2402-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="a2402-118">A parancs után a munka Select-AzContext meg a környezetét.</span><span class="sxs-lookup"><span data-stu-id="a2402-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="a2402-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2402-119">PARAMETERS</span></span>

### <span data-ttu-id="a2402-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2402-120">-DefaultProfile</span></span>
<span data-ttu-id="a2402-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2402-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2402-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a2402-122">-Force</span></span>
<span data-ttu-id="a2402-123">A környezet átnevezése akkor is, ha a célkörnyezet már létezik</span><span class="sxs-lookup"><span data-stu-id="a2402-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="a2402-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2402-124">-InputObject</span></span>
<span data-ttu-id="a2402-125">A context object, normally passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2402-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2402-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2402-126">-PassThru</span></span>
<span data-ttu-id="a2402-127">Adja vissza az átnevezett környezetet.</span><span class="sxs-lookup"><span data-stu-id="a2402-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="a2402-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="a2402-128">-Scope</span></span>
<span data-ttu-id="a2402-129">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e</span><span class="sxs-lookup"><span data-stu-id="a2402-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="a2402-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="a2402-130">-SourceName</span></span>
<span data-ttu-id="a2402-131">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="a2402-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2402-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="a2402-132">-TargetName</span></span>
<span data-ttu-id="a2402-133">A környezet új neve</span><span class="sxs-lookup"><span data-stu-id="a2402-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2402-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2402-134">-Confirm</span></span>
<span data-ttu-id="a2402-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2402-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2402-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2402-136">-WhatIf</span></span>
<span data-ttu-id="a2402-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2402-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2402-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2402-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2402-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2402-139">CommonParameters</span></span>
<span data-ttu-id="a2402-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2402-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2402-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2402-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2402-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2402-142">INPUTS</span></span>

### <span data-ttu-id="a2402-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a2402-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a2402-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2402-144">OUTPUTS</span></span>

### <span data-ttu-id="a2402-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a2402-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a2402-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2402-146">NOTES</span></span>

## <span data-ttu-id="a2402-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2402-147">RELATED LINKS</span></span>
