---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161146"
---
# <span data-ttu-id="6d35d-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6d35d-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="6d35d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d35d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d35d-103">Alkalmazásbiztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="6d35d-103">Gets an application security group.</span></span>

## <span data-ttu-id="6d35d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d35d-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d35d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d35d-105">DESCRIPTION</span></span>
<span data-ttu-id="6d35d-106">A **Get-AzApplicationSecurityGroup** parancsmag alkalmazásbiztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="6d35d-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="6d35d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d35d-107">EXAMPLES</span></span>

### <span data-ttu-id="6d35d-108">1. példa: Az összes alkalmazásbiztonsági csoport beolvasása.</span><span class="sxs-lookup"><span data-stu-id="6d35d-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6d35d-109">A fenti parancs az előfizetésben az összes alkalmazásbiztonsági csoportot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="6d35d-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="6d35d-110">2. példa: Alkalmazásbiztonsági csoportok lekérése egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6d35d-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6d35d-111">A fenti parancs a MyResourceGroup erőforráscsoporthoz tartozó összes alkalmazásbiztonsági csoportot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="6d35d-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6d35d-112">3. példa: Adott alkalmazásbiztonsági csoport lekérése.</span><span class="sxs-lookup"><span data-stu-id="6d35d-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="6d35d-113">A fenti parancs a MyApplicationSecurityGroup alkalmazásbiztonsági csoportot adja vissza a MyResourceGroup erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="6d35d-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6d35d-114">4. példa: Alkalmazásbiztonsági csoportok lekérése szűrés használatával.</span><span class="sxs-lookup"><span data-stu-id="6d35d-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6d35d-115">A fenti parancs a "MyApplicationSecurityGroup" kezdetű összes alkalmazásbiztonsági csoportot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="6d35d-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="6d35d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d35d-116">PARAMETERS</span></span>

### <span data-ttu-id="6d35d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d35d-117">-DefaultProfile</span></span>
<span data-ttu-id="6d35d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d35d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d35d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6d35d-119">-Name</span></span>
<span data-ttu-id="6d35d-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6d35d-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6d35d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d35d-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d35d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d35d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6d35d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d35d-123">CommonParameters</span></span>
<span data-ttu-id="6d35d-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d35d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d35d-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d35d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d35d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d35d-126">INPUTS</span></span>

### <span data-ttu-id="6d35d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6d35d-127">System.String</span></span>

## <span data-ttu-id="6d35d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d35d-128">OUTPUTS</span></span>

### <span data-ttu-id="6d35d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6d35d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="6d35d-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d35d-130">NOTES</span></span>

## <span data-ttu-id="6d35d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d35d-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d35d-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6d35d-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6d35d-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6d35d-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6d35d-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d35d-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6d35d-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d35d-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
