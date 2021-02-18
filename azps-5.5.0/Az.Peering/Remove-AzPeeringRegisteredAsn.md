---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206286"
---
# <span data-ttu-id="a1d79-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a1d79-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a1d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d79-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d79-103">Törölhet vagy eltávolíthat egy regisztrált asn-t a szülő társviszony-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a1d79-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="a1d79-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1d79-104">SYNTAX</span></span>

### <span data-ttu-id="a1d79-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d79-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d79-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d79-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d79-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d79-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1d79-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d79-109">Lehetővé teszi a regisztrált ASN eltávolítását a szülő társviszony-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a1d79-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="a1d79-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1d79-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d79-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a1d79-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="a1d79-112">A regisztrált ASN eltávolítása erőforrás-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="a1d79-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="a1d79-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d79-113">PARAMETERS</span></span>

### <span data-ttu-id="a1d79-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d79-114">-AsJob</span></span>
<span data-ttu-id="a1d79-115">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a1d79-115">Run in the background.</span></span>

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

### <span data-ttu-id="a1d79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d79-116">-DefaultProfile</span></span>
<span data-ttu-id="a1d79-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d79-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a1d79-118">-Force</span></span>
<span data-ttu-id="a1d79-119">A művelet befejezésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="a1d79-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="a1d79-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d79-120">-InputObject</span></span>
<span data-ttu-id="a1d79-121">A Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a1d79-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a1d79-122">-Name</span></span>
<span data-ttu-id="a1d79-123">A regisztrált ASN neve</span><span class="sxs-lookup"><span data-stu-id="a1d79-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d79-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1d79-124">-PassThru</span></span>
<span data-ttu-id="a1d79-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a1d79-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a1d79-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a1d79-126">-PeeringName</span></span>
<span data-ttu-id="a1d79-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a1d79-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d79-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d79-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1d79-129">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="a1d79-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d79-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d79-130">-ResourceId</span></span>
<span data-ttu-id="a1d79-131">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="a1d79-131">The resource id string name.</span></span>

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

### <span data-ttu-id="a1d79-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1d79-132">-Confirm</span></span>
<span data-ttu-id="a1d79-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1d79-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d79-134">-WhatIf</span></span>
<span data-ttu-id="a1d79-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1d79-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d79-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1d79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d79-137">CommonParameters</span></span>
<span data-ttu-id="a1d79-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d79-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1d79-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d79-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1d79-140">INPUTS</span></span>

### <span data-ttu-id="a1d79-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a1d79-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="a1d79-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a1d79-142">System.String</span></span>

## <span data-ttu-id="a1d79-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d79-143">OUTPUTS</span></span>

### <span data-ttu-id="a1d79-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1d79-144">System.Boolean</span></span>

## <span data-ttu-id="a1d79-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1d79-145">NOTES</span></span>

## <span data-ttu-id="a1d79-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d79-146">RELATED LINKS</span></span>
