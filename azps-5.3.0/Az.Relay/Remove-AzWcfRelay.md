---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467221"
---
# <span data-ttu-id="2468f-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="2468f-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="2468f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2468f-102">SYNOPSIS</span></span>
<span data-ttu-id="2468f-103">Eltávolítja a WcfRelay tartományt a megadott Továbbítás névterből.</span><span class="sxs-lookup"><span data-stu-id="2468f-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="2468f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2468f-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2468f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2468f-105">DESCRIPTION</span></span>
<span data-ttu-id="2468f-106">A **Remove-AzWcfRelay** parancsmag eltávolítja a WcfRelay értéket a megadott Továbbítás névtérből.</span><span class="sxs-lookup"><span data-stu-id="2468f-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="2468f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2468f-107">EXAMPLES</span></span>

### <span data-ttu-id="2468f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2468f-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="2468f-109">A WcfRelay eltávolítása `TestWCFRelay1` a névtérből. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="2468f-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2468f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2468f-110">PARAMETERS</span></span>

### <span data-ttu-id="2468f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2468f-111">-DefaultProfile</span></span>
<span data-ttu-id="2468f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2468f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2468f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2468f-113">-Name</span></span>
<span data-ttu-id="2468f-114">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="2468f-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2468f-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2468f-115">-Namespace</span></span>
<span data-ttu-id="2468f-116">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="2468f-116">Namespace Name.</span></span>

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

### <span data-ttu-id="2468f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2468f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2468f-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2468f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="2468f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2468f-119">-Confirm</span></span>
<span data-ttu-id="2468f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2468f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2468f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2468f-121">-WhatIf</span></span>
<span data-ttu-id="2468f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2468f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2468f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2468f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2468f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2468f-124">CommonParameters</span></span>
<span data-ttu-id="2468f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2468f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2468f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2468f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2468f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2468f-127">INPUTS</span></span>

### <span data-ttu-id="2468f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2468f-128">System.String</span></span>

## <span data-ttu-id="2468f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2468f-129">OUTPUTS</span></span>

### <span data-ttu-id="2468f-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="2468f-130">System.Void</span></span>

## <span data-ttu-id="2468f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2468f-131">NOTES</span></span>

## <span data-ttu-id="2468f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2468f-132">RELATED LINKS</span></span>
