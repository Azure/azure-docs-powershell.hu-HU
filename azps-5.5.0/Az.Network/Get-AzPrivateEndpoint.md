---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156954"
---
# <span data-ttu-id="9eaf5-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9eaf5-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="9eaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaf5-103">Privát végpont lekérte</span><span class="sxs-lookup"><span data-stu-id="9eaf5-103">Get a private endpoint</span></span>

## <span data-ttu-id="9eaf5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9eaf5-104">SYNTAX</span></span>

### <span data-ttu-id="9eaf5-105">NoExpand (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9eaf5-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eaf5-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="9eaf5-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eaf5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9eaf5-107">DESCRIPTION</span></span>
<span data-ttu-id="9eaf5-108">A **Get-AzPrivateEndpoint** parancsmag egy vagy több privát végpontot kap.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="9eaf5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9eaf5-109">EXAMPLES</span></span>

### <span data-ttu-id="9eaf5-110">1. példa: Privát végpont lekérése</span><span class="sxs-lookup"><span data-stu-id="9eaf5-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="9eaf5-111">Ez a parancs a MyPrivateEndpoint1 nevű privát végpontot a TestResourceGroup erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="9eaf5-112">2. példa: Az összes magánjellegű végpont felsorolása az ResourceGroupban</span><span class="sxs-lookup"><span data-stu-id="9eaf5-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="9eaf5-113">Ez a parancs a TestResourceGroup erőforráscsoport összes magánjellegű végpontja</span><span class="sxs-lookup"><span data-stu-id="9eaf5-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="9eaf5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eaf5-114">PARAMETERS</span></span>

### <span data-ttu-id="9eaf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaf5-115">-DefaultProfile</span></span>
<span data-ttu-id="9eaf5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eaf5-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9eaf5-117">-ExpandResource</span></span>
<span data-ttu-id="9eaf5-118">A kibontani szükséges erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="9eaf5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9eaf5-119">-Name</span></span>
<span data-ttu-id="9eaf5-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-120">The resource name.</span></span>

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

### <span data-ttu-id="9eaf5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eaf5-121">-ResourceGroupName</span></span>
<span data-ttu-id="9eaf5-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-122">The resource group name.</span></span>

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

### <span data-ttu-id="9eaf5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaf5-123">CommonParameters</span></span>
<span data-ttu-id="9eaf5-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eaf5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaf5-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eaf5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaf5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9eaf5-126">INPUTS</span></span>

### <span data-ttu-id="9eaf5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9eaf5-127">System.String</span></span>

## <span data-ttu-id="9eaf5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eaf5-128">OUTPUTS</span></span>

### <span data-ttu-id="9eaf5-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9eaf5-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9eaf5-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9eaf5-130">NOTES</span></span>

## <span data-ttu-id="9eaf5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eaf5-131">RELATED LINKS</span></span>

[<span data-ttu-id="9eaf5-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9eaf5-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="9eaf5-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9eaf5-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)