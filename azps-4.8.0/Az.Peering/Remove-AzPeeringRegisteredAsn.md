---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184718"
---
# <span data-ttu-id="fbce6-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="fbce6-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="fbce6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbce6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbce6-103">A fölérendelt társközi erőforrásból törölheti vagy távolíthatja el a regisztrált ASN-t.</span><span class="sxs-lookup"><span data-stu-id="fbce6-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="fbce6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbce6-104">SYNTAX</span></span>

### <span data-ttu-id="fbce6-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbce6-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbce6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fbce6-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbce6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbce6-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbce6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbce6-108">DESCRIPTION</span></span>
<span data-ttu-id="fbce6-109">Lehetővé teszi a Registered ASN-nek a fölérendelt társközi erőforrásból való eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="fbce6-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="fbce6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fbce6-110">EXAMPLES</span></span>

### <span data-ttu-id="fbce6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbce6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="fbce6-112">Az ASN-es regisztráció erőforrás-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fbce6-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="fbce6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbce6-113">PARAMETERS</span></span>

### <span data-ttu-id="fbce6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbce6-114">-AsJob</span></span>
<span data-ttu-id="fbce6-115">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="fbce6-115">Run in the background.</span></span>

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

### <span data-ttu-id="fbce6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbce6-116">-DefaultProfile</span></span>
<span data-ttu-id="fbce6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbce6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbce6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fbce6-118">-Force</span></span>
<span data-ttu-id="fbce6-119">A művelet elvégzésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="fbce6-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="fbce6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbce6-120">-InputObject</span></span>
<span data-ttu-id="fbce6-121">Get-AzPeeringServicePrefix használata</span><span class="sxs-lookup"><span data-stu-id="fbce6-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="fbce6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbce6-122">-Name</span></span>
<span data-ttu-id="fbce6-123">A regisztrált ASN-név</span><span class="sxs-lookup"><span data-stu-id="fbce6-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="fbce6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbce6-124">-PassThru</span></span>
<span data-ttu-id="fbce6-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fbce6-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fbce6-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="fbce6-126">-PeeringName</span></span>
<span data-ttu-id="fbce6-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="fbce6-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="fbce6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbce6-128">-ResourceGroupName</span></span>
<span data-ttu-id="fbce6-129">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="fbce6-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="fbce6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbce6-130">-ResourceId</span></span>
<span data-ttu-id="fbce6-131">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="fbce6-131">The resource id string name.</span></span>

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

### <span data-ttu-id="fbce6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbce6-132">-Confirm</span></span>
<span data-ttu-id="fbce6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbce6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbce6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbce6-134">-WhatIf</span></span>
<span data-ttu-id="fbce6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbce6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbce6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbce6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbce6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbce6-137">CommonParameters</span></span>
<span data-ttu-id="fbce6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbce6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbce6-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fbce6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbce6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbce6-140">INPUTS</span></span>

### <span data-ttu-id="fbce6-141">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="fbce6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="fbce6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fbce6-142">System.String</span></span>

## <span data-ttu-id="fbce6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbce6-143">OUTPUTS</span></span>

### <span data-ttu-id="fbce6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbce6-144">System.Boolean</span></span>

## <span data-ttu-id="fbce6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbce6-145">NOTES</span></span>

## <span data-ttu-id="fbce6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbce6-146">RELATED LINKS</span></span>
