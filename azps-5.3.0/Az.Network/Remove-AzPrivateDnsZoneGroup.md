---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481209"
---
# <span data-ttu-id="e79ce-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="e79ce-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="e79ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e79ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e79ce-103">Eltávolít egy DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="e79ce-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="e79ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e79ce-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e79ce-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e79ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e79ce-106">A **Remove-AzPrivateDnsZoneGroup** parancsmag eltávolít egy DNS-zónacsoportot.</span><span class="sxs-lookup"><span data-stu-id="e79ce-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="e79ce-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e79ce-107">EXAMPLES</span></span>

### <span data-ttu-id="e79ce-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e79ce-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="e79ce-109">A fenti példa eltávolítja a DNS-csoport1 nevű DNS-zóna grupját a végpontteszt-pr-végpontról.</span><span class="sxs-lookup"><span data-stu-id="e79ce-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="e79ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e79ce-110">PARAMETERS</span></span>

### <span data-ttu-id="e79ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e79ce-111">-AsJob</span></span>
<span data-ttu-id="e79ce-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e79ce-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e79ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79ce-113">-DefaultProfile</span></span>
<span data-ttu-id="e79ce-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e79ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e79ce-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e79ce-115">-Force</span></span>
<span data-ttu-id="e79ce-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="e79ce-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e79ce-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e79ce-117">-Name</span></span>
<span data-ttu-id="e79ce-118">A privát DNS-zónacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e79ce-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="e79ce-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e79ce-119">-PassThru</span></span>
<span data-ttu-id="e79ce-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e79ce-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e79ce-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="e79ce-121">-PrivateEndpointName</span></span>
<span data-ttu-id="e79ce-122">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="e79ce-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="e79ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e79ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="e79ce-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e79ce-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e79ce-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e79ce-125">-Confirm</span></span>
<span data-ttu-id="e79ce-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e79ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e79ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e79ce-127">-WhatIf</span></span>
<span data-ttu-id="e79ce-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e79ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e79ce-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e79ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e79ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79ce-130">CommonParameters</span></span>
<span data-ttu-id="e79ce-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e79ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79ce-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e79ce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79ce-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e79ce-133">INPUTS</span></span>

### <span data-ttu-id="e79ce-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e79ce-134">System.String</span></span>

## <span data-ttu-id="e79ce-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79ce-135">OUTPUTS</span></span>

### <span data-ttu-id="e79ce-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e79ce-136">System.Boolean</span></span>

## <span data-ttu-id="e79ce-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e79ce-137">NOTES</span></span>

## <span data-ttu-id="e79ce-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79ce-138">RELATED LINKS</span></span>
