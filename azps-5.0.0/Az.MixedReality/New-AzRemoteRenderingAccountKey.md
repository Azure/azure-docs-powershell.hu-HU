---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187310"
---
# <span data-ttu-id="7ef39-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ef39-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="7ef39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ef39-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef39-103">Távoli megjelenítési fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="7ef39-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="7ef39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ef39-104">SYNTAX</span></span>

### <span data-ttu-id="7ef39-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef39-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef39-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef39-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef39-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef39-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef39-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ef39-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ef39-111">DESCRIPTION</span></span>
<span data-ttu-id="7ef39-112">Regenerálódni a távoli megjelenítési fiók elsődleges kulcsát vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7ef39-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="7ef39-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7ef39-113">EXAMPLES</span></span>

### <span data-ttu-id="7ef39-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ef39-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="7ef39-115">Regenerálódni "példa" típusú távoli megjelenítési fiók másodlagos kulcsát "rg1".</span><span class="sxs-lookup"><span data-stu-id="7ef39-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="7ef39-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ef39-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7ef39-117">Regenerálódni a "példa" típusú távoli megjelenítési fiók másodlagos kulcsát az aktuális előfizetésből és a "rg1"-erőforrásból csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="7ef39-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="7ef39-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ef39-118">PARAMETERS</span></span>

### <span data-ttu-id="7ef39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef39-119">-DefaultProfile</span></span>
<span data-ttu-id="7ef39-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ef39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ef39-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7ef39-121">-Force</span></span>
<span data-ttu-id="7ef39-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7ef39-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ef39-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ef39-123">-InputObject</span></span>
<span data-ttu-id="7ef39-124">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="7ef39-124">The custom domain object.</span></span>

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

### <span data-ttu-id="7ef39-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ef39-125">-Name</span></span>
<span data-ttu-id="7ef39-126">Távoli megjelenítési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7ef39-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="7ef39-127">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="7ef39-127">-Primary</span></span>
<span data-ttu-id="7ef39-128">Regenerálódni a távoli megjelenítési fiók elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7ef39-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="7ef39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef39-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ef39-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7ef39-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ef39-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ef39-131">-ResourceId</span></span>
<span data-ttu-id="7ef39-132">A távoli megjelenítési fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ef39-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="7ef39-133">-Másodlagos</span><span class="sxs-lookup"><span data-stu-id="7ef39-133">-Secondary</span></span>
<span data-ttu-id="7ef39-134">Regenerálódni a távoli megjelenítési fiók elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7ef39-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="7ef39-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ef39-135">-Confirm</span></span>
<span data-ttu-id="7ef39-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ef39-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef39-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef39-137">-WhatIf</span></span>
<span data-ttu-id="7ef39-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ef39-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ef39-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ef39-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef39-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef39-140">CommonParameters</span></span>
<span data-ttu-id="7ef39-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ef39-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ef39-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef39-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef39-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef39-143">INPUTS</span></span>

### <span data-ttu-id="7ef39-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7ef39-144">System.String</span></span>

### <span data-ttu-id="7ef39-145">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7ef39-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="7ef39-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef39-146">OUTPUTS</span></span>

### <span data-ttu-id="7ef39-147">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7ef39-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="7ef39-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ef39-148">NOTES</span></span>

## <span data-ttu-id="7ef39-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ef39-149">RELATED LINKS</span></span>
