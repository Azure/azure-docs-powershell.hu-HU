---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195680"
---
# <span data-ttu-id="0506a-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0506a-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="0506a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0506a-102">SYNOPSIS</span></span>
<span data-ttu-id="0506a-103">Bekapja az alkalmazás biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="0506a-103">Gets an application security group.</span></span>

## <span data-ttu-id="0506a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0506a-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0506a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0506a-105">DESCRIPTION</span></span>
<span data-ttu-id="0506a-106">A **Get-AzApplicationSecurityGroup** parancsmag az alkalmazások biztonsági csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="0506a-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="0506a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0506a-107">EXAMPLES</span></span>

### <span data-ttu-id="0506a-108">Példa 1: az összes alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="0506a-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="0506a-109">A fenti parancs a minden alkalmazás biztonsági csoportját visszaállítja az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0506a-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="0506a-110">2. példa: az alkalmazás biztonsági csoportjainak beolvasása egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="0506a-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="0506a-111">A fenti parancs az erőforráscsoport MyResourceGroup tartozó összes alkalmazás biztonsági csoportját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="0506a-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="0506a-112">3. példa: egy adott alkalmazás biztonsági csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="0506a-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="0506a-113">A fenti parancs az MyApplicationSecurityGroup MyResourceGroup az alkalmazás biztonsági csoportjának értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0506a-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="0506a-114">4. példa: az alkalmazás biztonsági csoportjai szűréssel olvashatók be.</span><span class="sxs-lookup"><span data-stu-id="0506a-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="0506a-115">A fenti parancs a "MyApplicationSecurityGroup" kezdetű összes alkalmazás biztonsági csoportját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="0506a-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="0506a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0506a-116">PARAMETERS</span></span>

### <span data-ttu-id="0506a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0506a-117">-DefaultProfile</span></span>
<span data-ttu-id="0506a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0506a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0506a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0506a-119">-Name</span></span>
<span data-ttu-id="0506a-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0506a-120">The resource name.</span></span>

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

### <span data-ttu-id="0506a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0506a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0506a-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0506a-122">The resource group name.</span></span>

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

### <span data-ttu-id="0506a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0506a-123">CommonParameters</span></span>
<span data-ttu-id="0506a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0506a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0506a-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0506a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0506a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0506a-126">INPUTS</span></span>

### <span data-ttu-id="0506a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0506a-127">System.String</span></span>

## <span data-ttu-id="0506a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0506a-128">OUTPUTS</span></span>

### <span data-ttu-id="0506a-129">Microsoft. Azure. commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0506a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="0506a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0506a-130">NOTES</span></span>

## <span data-ttu-id="0506a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0506a-131">RELATED LINKS</span></span>

[<span data-ttu-id="0506a-132">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0506a-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="0506a-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0506a-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="0506a-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0506a-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0506a-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0506a-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
