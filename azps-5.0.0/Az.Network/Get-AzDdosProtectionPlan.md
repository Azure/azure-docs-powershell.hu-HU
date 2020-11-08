---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195592"
---
# <span data-ttu-id="24ddd-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="24ddd-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="24ddd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="24ddd-103">Kap egy DDoS védelmi csomagot.</span><span class="sxs-lookup"><span data-stu-id="24ddd-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="24ddd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24ddd-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ddd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="24ddd-106">A Get-AzDdosProtectionPlan parancsmag a DDoS védelmi csomagot kapja.</span><span class="sxs-lookup"><span data-stu-id="24ddd-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="24ddd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="24ddd-108">Példa 1: konkrét DDoS védelmi csomag beszerzése</span><span class="sxs-lookup"><span data-stu-id="24ddd-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="24ddd-109">Ebben az esetben meg kell adnia a **ResourceGroupName** és a **Name** attribútumot is, amely megfelel az erőforráscsoport és a DDoS védelmi terv nevének.</span><span class="sxs-lookup"><span data-stu-id="24ddd-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="24ddd-110">2. példa: egy erőforráscsoport minden DDoS védelmi tervének beszerzése</span><span class="sxs-lookup"><span data-stu-id="24ddd-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="24ddd-111">Ebben az esetben csak az **ResourceGroupName** paramétert adjuk meg a DDoS védelmi csomagok listájának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="24ddd-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="24ddd-112">3. példa: az előfizetésben szereplő összes DDoS védelmi csomag beszerzése</span><span class="sxs-lookup"><span data-stu-id="24ddd-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="24ddd-113">Itt nem adunk meg semmilyen paramétert az előfizetésben szereplő összes DDoS védelmi csomag listájának beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="24ddd-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="24ddd-114">Példa 4: az összes DDoS védelmi csomag beszerzése előfizetésben</span><span class="sxs-lookup"><span data-stu-id="24ddd-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="24ddd-115">Ez a parancsmag a "teszt" kezdetű összes DdosProtectionPlans visszaadja.</span><span class="sxs-lookup"><span data-stu-id="24ddd-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="24ddd-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24ddd-116">PARAMETERS</span></span>

### <span data-ttu-id="24ddd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ddd-117">-DefaultProfile</span></span>
<span data-ttu-id="24ddd-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24ddd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ddd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24ddd-119">-Name</span></span>
<span data-ttu-id="24ddd-120">A DDoS védelmi terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24ddd-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="24ddd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ddd-121">-ResourceGroupName</span></span>
<span data-ttu-id="24ddd-122">A DDoS védelem terve erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24ddd-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="24ddd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ddd-123">CommonParameters</span></span>
<span data-ttu-id="24ddd-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24ddd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ddd-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24ddd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ddd-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24ddd-126">INPUTS</span></span>

### <span data-ttu-id="24ddd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="24ddd-127">System.String</span></span>

## <span data-ttu-id="24ddd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24ddd-128">OUTPUTS</span></span>

### <span data-ttu-id="24ddd-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="24ddd-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="24ddd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24ddd-130">NOTES</span></span>

## <span data-ttu-id="24ddd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24ddd-131">RELATED LINKS</span></span>

[<span data-ttu-id="24ddd-132">Új – AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="24ddd-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="24ddd-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="24ddd-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="24ddd-134">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="24ddd-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="24ddd-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="24ddd-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="24ddd-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="24ddd-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)