---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186208"
---
# <span data-ttu-id="8ce85-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ce85-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="8ce85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ce85-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce85-103">Privát végpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="8ce85-103">Get a private endpoint</span></span>

## <span data-ttu-id="8ce85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ce85-104">SYNTAX</span></span>

### <span data-ttu-id="8ce85-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ce85-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ce85-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="8ce85-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ce85-107">DESCRIPTION</span></span>
<span data-ttu-id="8ce85-108">A **Get-AzPrivateEndpoint** parancsmag egy vagy több privát végpontot kap.</span><span class="sxs-lookup"><span data-stu-id="8ce85-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="8ce85-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8ce85-109">EXAMPLES</span></span>

### <span data-ttu-id="8ce85-110">Példa 1: privát végpont beolvasása</span><span class="sxs-lookup"><span data-stu-id="8ce85-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="8ce85-111">Ez a parancs a MyPrivateEndpoint1 nevű privát végpontot kapja meg az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ce85-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="8ce85-112">2. példa: az összes privát végpont listázása az ResourceGroup-on</span><span class="sxs-lookup"><span data-stu-id="8ce85-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="8ce85-113">Ez a parancs minden titkos végpontot beolvas az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ce85-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="8ce85-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ce85-114">PARAMETERS</span></span>

### <span data-ttu-id="8ce85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce85-115">-DefaultProfile</span></span>
<span data-ttu-id="8ce85-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ce85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ce85-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8ce85-117">-ExpandResource</span></span>
<span data-ttu-id="8ce85-118">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="8ce85-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce85-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ce85-119">-Name</span></span>
<span data-ttu-id="8ce85-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8ce85-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce85-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ce85-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ce85-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce85-123">CommonParameters</span></span>
<span data-ttu-id="8ce85-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ce85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce85-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8ce85-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce85-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce85-126">INPUTS</span></span>

### <span data-ttu-id="8ce85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce85-127">System.String</span></span>

## <span data-ttu-id="8ce85-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce85-128">OUTPUTS</span></span>

### <span data-ttu-id="8ce85-129">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ce85-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8ce85-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ce85-130">NOTES</span></span>

## <span data-ttu-id="8ce85-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ce85-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ce85-132">Új – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ce85-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="8ce85-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ce85-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)