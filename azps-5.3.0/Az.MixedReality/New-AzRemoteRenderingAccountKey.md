---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468338"
---
# <span data-ttu-id="c02a7-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="c02a7-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="c02a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c02a7-103">A távoli leképezési fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="c02a7-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="c02a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c02a7-104">SYNTAX</span></span>

### <span data-ttu-id="c02a7-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c02a7-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c02a7-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c02a7-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c02a7-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c02a7-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02a7-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c02a7-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c02a7-111">DESCRIPTION</span></span>
<span data-ttu-id="c02a7-112">A távoli leképezési fiók elsődleges kulcsának vagy másodlagos kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c02a7-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="c02a7-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c02a7-113">EXAMPLES</span></span>

### <span data-ttu-id="c02a7-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="c02a7-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="c02a7-115">A távoli leképezési fiók "példa" másodlagos kulcsának újragenerálása az "rg1" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c02a7-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="c02a7-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="c02a7-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c02a7-117">A távoli leképezési fiók "példa" másodlagos kulcsának újragenerálása az aktuális Előfizetés és Erőforráscsoport "rg1" példából pipázással.</span><span class="sxs-lookup"><span data-stu-id="c02a7-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="c02a7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c02a7-118">PARAMETERS</span></span>

### <span data-ttu-id="c02a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02a7-119">-DefaultProfile</span></span>
<span data-ttu-id="c02a7-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c02a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c02a7-121">-Force</span></span>
<span data-ttu-id="c02a7-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c02a7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c02a7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c02a7-123">-InputObject</span></span>
<span data-ttu-id="c02a7-124">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="c02a7-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c02a7-125">-Name</span></span>
<span data-ttu-id="c02a7-126">Távoli leképezési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c02a7-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="c02a7-127">-Primary</span></span>
<span data-ttu-id="c02a7-128">A távoli leképezési fiók elsődleges kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c02a7-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02a7-129">-ResourceGroupName</span></span>
<span data-ttu-id="c02a7-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c02a7-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c02a7-131">-ResourceId</span></span>
<span data-ttu-id="c02a7-132">A távoli leképezési fiók erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c02a7-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="c02a7-133">-Secondary</span></span>
<span data-ttu-id="c02a7-134">A távoli leképezési fiók elsődleges kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c02a7-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02a7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c02a7-135">-Confirm</span></span>
<span data-ttu-id="c02a7-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c02a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c02a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c02a7-137">-WhatIf</span></span>
<span data-ttu-id="c02a7-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c02a7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c02a7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c02a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c02a7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02a7-140">CommonParameters</span></span>
<span data-ttu-id="c02a7-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02a7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c02a7-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02a7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02a7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c02a7-143">INPUTS</span></span>

### <span data-ttu-id="c02a7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c02a7-144">System.String</span></span>

### <span data-ttu-id="c02a7-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="c02a7-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="c02a7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c02a7-146">OUTPUTS</span></span>

### <span data-ttu-id="c02a7-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c02a7-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="c02a7-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c02a7-148">NOTES</span></span>

## <span data-ttu-id="c02a7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c02a7-149">RELATED LINKS</span></span>
