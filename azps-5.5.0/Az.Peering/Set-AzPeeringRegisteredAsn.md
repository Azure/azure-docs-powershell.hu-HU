---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160426"
---
# <span data-ttu-id="b2f79-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b2f79-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b2f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f79-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f79-103">Beállítja vagy frissíti a regisztrált ASN-t a szülő társviszony-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="b2f79-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="b2f79-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2f79-104">SYNTAX</span></span>

### <span data-ttu-id="b2f79-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2f79-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f79-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f79-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f79-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f79-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2f79-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f79-109">Lehetővé teszi egy regisztrált asn frissítését a szülő társviszony-létesítő erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="b2f79-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="b2f79-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2f79-110">EXAMPLES</span></span>

### <span data-ttu-id="b2f79-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b2f79-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="b2f79-112">Frissíti az ASN-t erőforrásazonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="b2f79-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="b2f79-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2f79-113">PARAMETERS</span></span>

### <span data-ttu-id="b2f79-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2f79-114">-AsJob</span></span>
<span data-ttu-id="b2f79-115">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b2f79-115">Run in the background.</span></span>

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

### <span data-ttu-id="b2f79-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="b2f79-116">-Asn</span></span>
<span data-ttu-id="b2f79-117">A regisztrálható ASN</span><span class="sxs-lookup"><span data-stu-id="b2f79-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="b2f79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f79-118">-DefaultProfile</span></span>
<span data-ttu-id="b2f79-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2f79-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f79-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f79-120">-InputObject</span></span>
<span data-ttu-id="b2f79-121">Használjon Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b2f79-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b2f79-122">-Name</span></span>
<span data-ttu-id="b2f79-123">A regisztrálható ASN</span><span class="sxs-lookup"><span data-stu-id="b2f79-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f79-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b2f79-124">-PeeringName</span></span>
<span data-ttu-id="b2f79-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="b2f79-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b2f79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f79-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2f79-127">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="b2f79-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b2f79-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f79-128">-ResourceId</span></span>
<span data-ttu-id="b2f79-129">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="b2f79-129">The resource id string name.</span></span>

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

### <span data-ttu-id="b2f79-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2f79-130">-Confirm</span></span>
<span data-ttu-id="b2f79-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b2f79-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f79-132">-WhatIf</span></span>
<span data-ttu-id="b2f79-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2f79-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f79-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2f79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f79-135">CommonParameters</span></span>
<span data-ttu-id="b2f79-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f79-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2f79-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f79-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2f79-138">INPUTS</span></span>

### <span data-ttu-id="b2f79-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b2f79-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="b2f79-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b2f79-140">System.String</span></span>

## <span data-ttu-id="b2f79-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2f79-141">OUTPUTS</span></span>

### <span data-ttu-id="b2f79-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b2f79-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b2f79-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2f79-143">NOTES</span></span>

## <span data-ttu-id="b2f79-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2f79-144">RELATED LINKS</span></span>
