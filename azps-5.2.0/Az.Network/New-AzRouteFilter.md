---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367526"
---
# <span data-ttu-id="fa084-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fa084-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="fa084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa084-102">SYNOPSIS</span></span>
<span data-ttu-id="fa084-103">Útvonalszűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fa084-103">Creates a route filter.</span></span>

## <span data-ttu-id="fa084-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa084-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa084-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa084-105">DESCRIPTION</span></span>
<span data-ttu-id="fa084-106">A New-AzRouteFilter parancsmag létrehoz egy Azure útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="fa084-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="fa084-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa084-107">EXAMPLES</span></span>

### <span data-ttu-id="fa084-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fa084-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="fa084-109">A parancs létrehoz egy új útvonalszűrőt.</span><span class="sxs-lookup"><span data-stu-id="fa084-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="fa084-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa084-110">PARAMETERS</span></span>

### <span data-ttu-id="fa084-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa084-111">-AsJob</span></span>
<span data-ttu-id="fa084-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fa084-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa084-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa084-113">-DefaultProfile</span></span>
<span data-ttu-id="fa084-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa084-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa084-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa084-115">-Force</span></span>
<span data-ttu-id="fa084-116">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útvonaltáblát, ha már létezik egy azonos nevű útvonalszűrő.</span><span class="sxs-lookup"><span data-stu-id="fa084-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="fa084-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fa084-117">-Location</span></span>
<span data-ttu-id="fa084-118">Azt az Azure-régiót adja meg, amelyben ez a parancsmag útvonalszűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fa084-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa084-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fa084-119">-Name</span></span>
<span data-ttu-id="fa084-120">Megadja az útvonalszűrő nevét.</span><span class="sxs-lookup"><span data-stu-id="fa084-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa084-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa084-121">-ResourceGroupName</span></span>
<span data-ttu-id="fa084-122">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag útvonalszűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fa084-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa084-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="fa084-123">-Rule</span></span>
<span data-ttu-id="fa084-124">Az útvonalszűrővel társítandó Útválasztási szűrőszabály-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="fa084-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa084-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa084-125">-Tag</span></span>
<span data-ttu-id="fa084-126">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="fa084-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fa084-127">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="fa084-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa084-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa084-128">-Confirm</span></span>
<span data-ttu-id="fa084-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa084-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa084-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa084-130">-WhatIf</span></span>
<span data-ttu-id="fa084-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa084-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa084-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa084-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa084-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa084-133">CommonParameters</span></span>
<span data-ttu-id="fa084-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa084-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa084-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa084-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa084-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa084-136">INPUTS</span></span>

### <span data-ttu-id="fa084-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fa084-137">System.String</span></span>

### <span data-ttu-id="fa084-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="fa084-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="fa084-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fa084-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fa084-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa084-140">OUTPUTS</span></span>

### <span data-ttu-id="fa084-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fa084-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fa084-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa084-142">NOTES</span></span>
<span data-ttu-id="fa084-143">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="fa084-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fa084-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa084-144">RELATED LINKS</span></span>

[<span data-ttu-id="fa084-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fa084-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="fa084-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fa084-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="fa084-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fa084-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="fa084-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa084-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fa084-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa084-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fa084-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa084-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fa084-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa084-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fa084-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa084-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
