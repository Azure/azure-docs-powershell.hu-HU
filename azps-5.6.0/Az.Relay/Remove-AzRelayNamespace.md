---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000454"
---
# <span data-ttu-id="75ac8-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="75ac8-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="75ac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="75ac8-103">Eltávolítja a névteret a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="75ac8-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="75ac8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75ac8-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ac8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="75ac8-106">A **Remove-AzRelayNamespace** parancsmag eltávolítja a névteret a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="75ac8-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="75ac8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="75ac8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="75ac8-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="75ac8-109">Eltávolítja a Továbbítás `TestNameSpace-Relay1` névteret a megadott erőforráscsoportból. `Default-ServiceBus-WestUS`</span><span class="sxs-lookup"><span data-stu-id="75ac8-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="75ac8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75ac8-110">PARAMETERS</span></span>

### <span data-ttu-id="75ac8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ac8-111">-DefaultProfile</span></span>
<span data-ttu-id="75ac8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75ac8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ac8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="75ac8-113">-Name</span></span>
<span data-ttu-id="75ac8-114">Relay Namespace Name (Továbbítás neve)</span><span class="sxs-lookup"><span data-stu-id="75ac8-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ac8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ac8-115">-ResourceGroupName</span></span>
<span data-ttu-id="75ac8-116">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75ac8-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="75ac8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75ac8-117">-Confirm</span></span>
<span data-ttu-id="75ac8-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75ac8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ac8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ac8-119">-WhatIf</span></span>
<span data-ttu-id="75ac8-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75ac8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ac8-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75ac8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ac8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ac8-122">CommonParameters</span></span>
<span data-ttu-id="75ac8-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ac8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ac8-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ac8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ac8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75ac8-125">INPUTS</span></span>

### <span data-ttu-id="75ac8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="75ac8-126">System.String</span></span>

## <span data-ttu-id="75ac8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75ac8-127">OUTPUTS</span></span>

### <span data-ttu-id="75ac8-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="75ac8-128">System.Void</span></span>

## <span data-ttu-id="75ac8-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75ac8-129">NOTES</span></span>

## <span data-ttu-id="75ac8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75ac8-130">RELATED LINKS</span></span>
