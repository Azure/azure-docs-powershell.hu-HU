---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: f52f6a2872d6f7567a51e1433336ccb8e1629fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837583"
---
# <span data-ttu-id="1065d-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1065d-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="1065d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1065d-102">SYNOPSIS</span></span>
<span data-ttu-id="1065d-103">A NAT-átjáró erőforrásait név vagy NatGateway vagy az erőforráscsoport összes NAT-átjáró erőforrásával kapja.</span><span class="sxs-lookup"><span data-stu-id="1065d-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="1065d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1065d-104">SYNTAX</span></span>

### <span data-ttu-id="1065d-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1065d-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1065d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1065d-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1065d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1065d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1065d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1065d-108">DESCRIPTION</span></span>
<span data-ttu-id="1065d-109">A NAT-átjáró erőforrásait név vagy NatGateway vagy az erőforráscsoport összes NAT-átjáró erőforrásával kapja.</span><span class="sxs-lookup"><span data-stu-id="1065d-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="1065d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1065d-110">EXAMPLES</span></span>

### <span data-ttu-id="1065d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1065d-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="1065d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1065d-112">PARAMETERS</span></span>

### <span data-ttu-id="1065d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1065d-113">-DefaultProfile</span></span>
<span data-ttu-id="1065d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1065d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1065d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1065d-115">-Name</span></span>
<span data-ttu-id="1065d-116">A NAT-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="1065d-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1065d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1065d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1065d-118">A NAT-átjáró erőforrás-csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="1065d-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1065d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1065d-119">-ResourceId</span></span>
<span data-ttu-id="1065d-120">NAT-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="1065d-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1065d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1065d-121">CommonParameters</span></span>
<span data-ttu-id="1065d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1065d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1065d-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1065d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1065d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1065d-124">INPUTS</span></span>

### <span data-ttu-id="1065d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1065d-125">System.String</span></span>

## <span data-ttu-id="1065d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1065d-126">OUTPUTS</span></span>

### <span data-ttu-id="1065d-127">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="1065d-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="1065d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1065d-128">NOTES</span></span>

## <span data-ttu-id="1065d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1065d-129">RELATED LINKS</span></span>
