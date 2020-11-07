---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678950"
---
# <span data-ttu-id="ea156-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea156-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="ea156-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea156-102">SYNOPSIS</span></span>
<span data-ttu-id="ea156-103">Eltávolítja egy HybridConnection engedélyezési szabályát az adott továbbító entitásokból (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea156-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea156-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea156-104">SYNTAX</span></span>

### <span data-ttu-id="ea156-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea156-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea156-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea156-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea156-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea156-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea156-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea156-108">DESCRIPTION</span></span>
<span data-ttu-id="ea156-109">A **Remove-AzureRmRelayAuthorizationRule** parancsmag eltávolítja a megadott továbbítóügynök engedélyezési szabályait (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea156-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea156-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ea156-110">EXAMPLES</span></span>

### <span data-ttu-id="ea156-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ea156-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="ea156-112">Eltávolítja a névtér engedélyezési szabályát `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea156-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ea156-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ea156-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="ea156-114">Eltávolítja a `AuthoRule1` névtérből származó WcfRelay engedélyezési szabályát `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea156-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ea156-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ea156-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="ea156-116">Eltávolítja a `AuthoRule1` névtérből származó HybridConnection engedélyezési szabályát `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea156-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ea156-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea156-117">PARAMETERS</span></span>

### <span data-ttu-id="ea156-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea156-118">-DefaultProfile</span></span>
<span data-ttu-id="ea156-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea156-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ea156-120">-Force</span></span>
<span data-ttu-id="ea156-121">Ne kérjen megerősítést</span><span class="sxs-lookup"><span data-stu-id="ea156-121">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea156-122">-HybridConnection</span></span>
<span data-ttu-id="ea156-123">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="ea156-123">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea156-124">-Name</span></span>
<span data-ttu-id="ea156-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="ea156-125">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea156-126">-Namespace</span></span>
<span data-ttu-id="ea156-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ea156-127">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea156-128">-PassThru</span></span>
<span data-ttu-id="ea156-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ea156-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea156-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea156-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ea156-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea156-132">-WcfRelay</span></span>
<span data-ttu-id="ea156-133">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="ea156-133">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea156-134">-Confirm</span></span>
<span data-ttu-id="ea156-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea156-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea156-136">-WhatIf</span></span>
<span data-ttu-id="ea156-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea156-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea156-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea156-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea156-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea156-139">CommonParameters</span></span>
<span data-ttu-id="ea156-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea156-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea156-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea156-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea156-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea156-142">INPUTS</span></span>

### <span data-ttu-id="ea156-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ea156-143">System.String</span></span>

## <span data-ttu-id="ea156-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea156-144">OUTPUTS</span></span>

### <span data-ttu-id="ea156-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea156-145">System.Boolean</span></span>

## <span data-ttu-id="ea156-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea156-146">NOTES</span></span>

## <span data-ttu-id="ea156-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea156-147">RELATED LINKS</span></span>

