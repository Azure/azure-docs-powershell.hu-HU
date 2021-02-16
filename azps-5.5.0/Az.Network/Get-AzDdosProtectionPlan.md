---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157034"
---
# <span data-ttu-id="0be3b-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0be3b-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="0be3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0be3b-103">DDoS védelmi tervet kap.</span><span class="sxs-lookup"><span data-stu-id="0be3b-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="0be3b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0be3b-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be3b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0be3b-105">DESCRIPTION</span></span>
<span data-ttu-id="0be3b-106">A Get-AzDdosProtectionPlan parancsmag DDoS védelmi tervet kap.</span><span class="sxs-lookup"><span data-stu-id="0be3b-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="0be3b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0be3b-107">EXAMPLES</span></span>

### <span data-ttu-id="0be3b-108">1. példa: Adott DDoS védelmi csomag lekérte</span><span class="sxs-lookup"><span data-stu-id="0be3b-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="0be3b-109">Ebben az esetben a **ResourceGroupName** és a **Name** attribútumot is meg kell adnunk, amelyek megfelelnek az erőforráscsoportnak és a DDoS védelmi terv nevének.</span><span class="sxs-lookup"><span data-stu-id="0be3b-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="0be3b-110">2. példa: Az összes DDoS védelmi terv lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="0be3b-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="0be3b-111">Ebben az esetben csak az **ResourceGroupName** paramétert adhatja meg a DDoS védelmi tervek listájának beszerkosításához.</span><span class="sxs-lookup"><span data-stu-id="0be3b-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="0be3b-112">3. példa: Az összes DDoS-védelmi csomag lekérte az előfizetést</span><span class="sxs-lookup"><span data-stu-id="0be3b-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="0be3b-113">Itt nem adunk meg paramétereket az előfizetésben található összes DDoS védelmi csomag listájának lekértéhez.</span><span class="sxs-lookup"><span data-stu-id="0be3b-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="0be3b-114">4. példa: Az összes DDoS védelmi csomag lekérte az előfizetést</span><span class="sxs-lookup"><span data-stu-id="0be3b-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="0be3b-115">Ez a parancsmag visszaadja az összes olyan DdosProtectionPlans értéket, amely a "test" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="0be3b-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="0be3b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0be3b-116">PARAMETERS</span></span>

### <span data-ttu-id="0be3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be3b-117">-DefaultProfile</span></span>
<span data-ttu-id="0be3b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0be3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be3b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0be3b-119">-Name</span></span>
<span data-ttu-id="0be3b-120">A DDoS védelmi terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0be3b-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="0be3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="0be3b-122">A DDoS védelmi terv erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0be3b-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="0be3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be3b-123">CommonParameters</span></span>
<span data-ttu-id="0be3b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be3b-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0be3b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be3b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0be3b-126">INPUTS</span></span>

### <span data-ttu-id="0be3b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0be3b-127">System.String</span></span>

## <span data-ttu-id="0be3b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0be3b-128">OUTPUTS</span></span>

### <span data-ttu-id="0be3b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0be3b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="0be3b-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0be3b-130">NOTES</span></span>

## <span data-ttu-id="0be3b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0be3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0be3b-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0be3b-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="0be3b-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="0be3b-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="0be3b-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0be3b-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="0be3b-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0be3b-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="0be3b-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0be3b-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)