---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: 49fbc411d8da95ed2ea968224be139d01fc5df0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942442"
---
# <span data-ttu-id="c2a1c-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c2a1c-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c2a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a1c-103">CustomIpPrefix erőforrást kap</span><span class="sxs-lookup"><span data-stu-id="c2a1c-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="c2a1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2a1c-104">SYNTAX</span></span>

### <span data-ttu-id="c2a1c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2a1c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a1c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a1c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a1c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="c2a1c-108">A **Get-AzCustomIpPrefix** parancsmag egy vagy több CustomIpPrefixe-et kap a bemeneti paraméterek készlete alapján.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="c2a1c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="c2a1c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2a1c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="c2a1c-111">Ez a parancs egy MyCustomIpPrefix nevű CustomIpPrefix erőforrást kap a myRg erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="c2a1c-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="c2a1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="c2a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="c2a1c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c2a1c-115">-Name</span></span>
<span data-ttu-id="c2a1c-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2a1c-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a1c-119">-ResourceId</span></span>
<span data-ttu-id="c2a1c-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a1c-121">CommonParameters</span></span>
<span data-ttu-id="c2a1c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a1c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2a1c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a1c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2a1c-124">INPUTS</span></span>

### <span data-ttu-id="c2a1c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c2a1c-125">System.String</span></span>

## <span data-ttu-id="c2a1c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2a1c-126">OUTPUTS</span></span>

### <span data-ttu-id="c2a1c-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c2a1c-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c2a1c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2a1c-128">NOTES</span></span>

## <span data-ttu-id="c2a1c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2a1c-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2a1c-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c2a1c-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="c2a1c-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c2a1c-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="c2a1c-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c2a1c-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)