---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940042"
---
# <span data-ttu-id="ecda4-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="ecda4-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="ecda4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecda4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecda4-103">Eltávolít egy DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="ecda4-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="ecda4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecda4-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecda4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecda4-105">DESCRIPTION</span></span>
<span data-ttu-id="ecda4-106">A **Remove-AzPrivateDnsZoneGroup** parancsmag eltávolít egy DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="ecda4-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="ecda4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecda4-107">EXAMPLES</span></span>

### <span data-ttu-id="ecda4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ecda4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="ecda4-109">A fenti példa eltávolítja a DNS-csoport1 nevű DNS-zóna grupját a végpontteszt-pr-végpontból.</span><span class="sxs-lookup"><span data-stu-id="ecda4-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="ecda4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecda4-110">PARAMETERS</span></span>

### <span data-ttu-id="ecda4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecda4-111">-AsJob</span></span>
<span data-ttu-id="ecda4-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ecda4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecda4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecda4-113">-DefaultProfile</span></span>
<span data-ttu-id="ecda4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecda4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecda4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ecda4-115">-Force</span></span>
<span data-ttu-id="ecda4-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="ecda4-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ecda4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ecda4-117">-Name</span></span>
<span data-ttu-id="ecda4-118">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecda4-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecda4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecda4-119">-PassThru</span></span>
<span data-ttu-id="ecda4-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ecda4-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ecda4-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="ecda4-121">-PrivateEndpointName</span></span>
<span data-ttu-id="ecda4-122">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="ecda4-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="ecda4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecda4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ecda4-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecda4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecda4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecda4-125">-Confirm</span></span>
<span data-ttu-id="ecda4-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ecda4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecda4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecda4-127">-WhatIf</span></span>
<span data-ttu-id="ecda4-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ecda4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecda4-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecda4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecda4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecda4-130">CommonParameters</span></span>
<span data-ttu-id="ecda4-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecda4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecda4-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecda4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecda4-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecda4-133">INPUTS</span></span>

### <span data-ttu-id="ecda4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ecda4-134">System.String</span></span>

## <span data-ttu-id="ecda4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecda4-135">OUTPUTS</span></span>

### <span data-ttu-id="ecda4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecda4-136">System.Boolean</span></span>

## <span data-ttu-id="ecda4-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecda4-137">NOTES</span></span>

## <span data-ttu-id="ecda4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecda4-138">RELATED LINKS</span></span>
