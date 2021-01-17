---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384759"
---
# <span data-ttu-id="b9a5b-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b9a5b-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b9a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a5b-103">Regisztrált ASN létrehozása társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="b9a5b-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="b9a5b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9a5b-104">SYNTAX</span></span>

### <span data-ttu-id="b9a5b-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9a5b-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a5b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a5b-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a5b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a5b-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a5b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9a5b-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a5b-109">Regisztrált ASN-eket hozhat létre társviszony-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="b9a5b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9a5b-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a5b-111">Társviszony-létesítés és regisztrált asn-hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9a5b-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="b9a5b-112">Szerezze be azt a társviszonyt, amelybe regisztrált asn-t szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="b9a5b-113">Ezután adja át a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="b9a5b-114">Regisztrált asn létrehozása társviszony-erőforrásazonosítóval</span><span class="sxs-lookup"><span data-stu-id="b9a5b-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="b9a5b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9a5b-115">PARAMETERS</span></span>

### <span data-ttu-id="b9a5b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9a5b-116">-AsJob</span></span>
<span data-ttu-id="b9a5b-117">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-117">Run in the background.</span></span>

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

### <span data-ttu-id="b9a5b-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="b9a5b-118">-Asn</span></span>
<span data-ttu-id="b9a5b-119">A regisztrálható ASN</span><span class="sxs-lookup"><span data-stu-id="b9a5b-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a5b-120">-DefaultProfile</span></span>
<span data-ttu-id="b9a5b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a5b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a5b-122">-InputObject</span></span>
<span data-ttu-id="b9a5b-123">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b9a5b-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b9a5b-124">-Name</span></span>
<span data-ttu-id="b9a5b-125">A regisztrálható ASN</span><span class="sxs-lookup"><span data-stu-id="b9a5b-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b9a5b-126">-PeeringName</span></span>
<span data-ttu-id="b9a5b-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a5b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9a5b-129">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a5b-130">-ResourceId</span></span>
<span data-ttu-id="b9a5b-131">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a5b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9a5b-132">-Confirm</span></span>
<span data-ttu-id="b9a5b-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a5b-134">-WhatIf</span></span>
<span data-ttu-id="b9a5b-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a5b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a5b-137">CommonParameters</span></span>
<span data-ttu-id="b9a5b-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a5b-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9a5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a5b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a5b-140">INPUTS</span></span>

### <span data-ttu-id="b9a5b-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="b9a5b-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b9a5b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b9a5b-142">System.String</span></span>

## <span data-ttu-id="b9a5b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9a5b-143">OUTPUTS</span></span>

### <span data-ttu-id="b9a5b-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b9a5b-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b9a5b-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9a5b-145">NOTES</span></span>

## <span data-ttu-id="b9a5b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9a5b-146">RELATED LINKS</span></span>
