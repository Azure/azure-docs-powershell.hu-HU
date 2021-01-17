---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467227"
---
# <span data-ttu-id="82132-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="82132-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="82132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82132-102">SYNOPSIS</span></span>
<span data-ttu-id="82132-103">Eltávolítja a HybridConnectiont a megadott HybridConnection névtérből.</span><span class="sxs-lookup"><span data-stu-id="82132-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="82132-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82132-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82132-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82132-105">DESCRIPTION</span></span>
<span data-ttu-id="82132-106">A **Remove-AzRelayHybridConnection** parancsmag eltávolítja a HybridConnectiont a megadott továbbítási névtérből.</span><span class="sxs-lookup"><span data-stu-id="82132-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="82132-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82132-107">EXAMPLES</span></span>

### <span data-ttu-id="82132-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="82132-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="82132-109">Eltávolítja a HybridConnectiont `TestHybridConnection` a névtérből. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="82132-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="82132-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82132-110">PARAMETERS</span></span>

### <span data-ttu-id="82132-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82132-111">-DefaultProfile</span></span>
<span data-ttu-id="82132-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82132-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82132-113">-Name</span><span class="sxs-lookup"><span data-stu-id="82132-113">-Name</span></span>
<span data-ttu-id="82132-114">HybridConnections Name.</span><span class="sxs-lookup"><span data-stu-id="82132-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82132-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="82132-115">-Namespace</span></span>
<span data-ttu-id="82132-116">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="82132-116">Namespace Name.</span></span>

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

### <span data-ttu-id="82132-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82132-117">-ResourceGroupName</span></span>
<span data-ttu-id="82132-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="82132-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="82132-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82132-119">-Confirm</span></span>
<span data-ttu-id="82132-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82132-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82132-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82132-121">-WhatIf</span></span>
<span data-ttu-id="82132-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82132-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82132-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82132-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82132-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82132-124">CommonParameters</span></span>
<span data-ttu-id="82132-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82132-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82132-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82132-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82132-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82132-127">INPUTS</span></span>

### <span data-ttu-id="82132-128">System.String</span><span class="sxs-lookup"><span data-stu-id="82132-128">System.String</span></span>

## <span data-ttu-id="82132-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82132-129">OUTPUTS</span></span>

### <span data-ttu-id="82132-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="82132-130">System.Void</span></span>

## <span data-ttu-id="82132-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82132-131">NOTES</span></span>

## <span data-ttu-id="82132-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82132-132">RELATED LINKS</span></span>
