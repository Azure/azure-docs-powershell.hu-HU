---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378110"
---
# <span data-ttu-id="fd273-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fd273-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="fd273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd273-102">SYNOPSIS</span></span>
<span data-ttu-id="fd273-103">A Hibrid összekapcsolás engedélyezési szabályának eltávolítása a megadott továbbítási entitásból (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fd273-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fd273-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd273-104">SYNTAX</span></span>

### <span data-ttu-id="fd273-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd273-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd273-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fd273-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd273-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fd273-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd273-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd273-108">DESCRIPTION</span></span>
<span data-ttu-id="fd273-109">A **Remove-AzRelayAuthorizationRule** parancsmag eltávolítja a megadott továbbítási entitások engedélyezési szabályát (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fd273-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fd273-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd273-110">EXAMPLES</span></span>

### <span data-ttu-id="fd273-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd273-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="fd273-112">Eltávolítja a névtér `AuthoRule1` engedélyezési `TestNameSpace-Relay1` szabályát.</span><span class="sxs-lookup"><span data-stu-id="fd273-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="fd273-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd273-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="fd273-114">Eltávolítja a `AuthoRule1` WcfRelay engedélyezési szabályát `TestWcfRelay` a névtérből. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="fd273-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="fd273-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fd273-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="fd273-116">Eltávolítja a HybridConnection engedélyezési szabályát `AuthoRule1` `TestHybridConnection` a névtérből. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="fd273-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="fd273-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd273-117">PARAMETERS</span></span>

### <span data-ttu-id="fd273-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd273-118">-DefaultProfile</span></span>
<span data-ttu-id="fd273-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd273-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd273-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fd273-120">-Force</span></span>
<span data-ttu-id="fd273-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd273-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd273-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fd273-122">-HybridConnection</span></span>
<span data-ttu-id="fd273-123">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="fd273-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd273-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fd273-124">-Name</span></span>
<span data-ttu-id="fd273-125">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="fd273-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd273-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd273-126">-Namespace</span></span>
<span data-ttu-id="fd273-127">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="fd273-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd273-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd273-128">-PassThru</span></span>
<span data-ttu-id="fd273-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fd273-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fd273-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd273-130">-ResourceGroupName</span></span>
<span data-ttu-id="fd273-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd273-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd273-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fd273-132">-WcfRelay</span></span>
<span data-ttu-id="fd273-133">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="fd273-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd273-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd273-134">-Confirm</span></span>
<span data-ttu-id="fd273-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd273-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd273-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd273-136">-WhatIf</span></span>
<span data-ttu-id="fd273-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd273-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd273-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd273-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd273-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd273-139">CommonParameters</span></span>
<span data-ttu-id="fd273-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd273-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd273-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd273-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd273-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd273-142">INPUTS</span></span>

### <span data-ttu-id="fd273-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fd273-143">System.String</span></span>

## <span data-ttu-id="fd273-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd273-144">OUTPUTS</span></span>

### <span data-ttu-id="fd273-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd273-145">System.Boolean</span></span>

## <span data-ttu-id="fd273-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd273-146">NOTES</span></span>

## <span data-ttu-id="fd273-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd273-147">RELATED LINKS</span></span>
