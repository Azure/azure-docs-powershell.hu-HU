---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364082"
---
# <span data-ttu-id="ca668-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca668-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ca668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca668-102">SYNOPSIS</span></span>
<span data-ttu-id="ca668-103">Privát végpont lekérte</span><span class="sxs-lookup"><span data-stu-id="ca668-103">Get a private endpoint</span></span>

## <span data-ttu-id="ca668-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca668-104">SYNTAX</span></span>

### <span data-ttu-id="ca668-105">NoExpand (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca668-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca668-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="ca668-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca668-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca668-107">DESCRIPTION</span></span>
<span data-ttu-id="ca668-108">A **Get-AzPrivateEndpoint** parancsmag egy vagy több privát végpontot kap.</span><span class="sxs-lookup"><span data-stu-id="ca668-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="ca668-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca668-109">EXAMPLES</span></span>

### <span data-ttu-id="ca668-110">1. példa: Privát végpont lekérése</span><span class="sxs-lookup"><span data-stu-id="ca668-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="ca668-111">Ez a parancs a MyPrivateEndpoint1 nevű privát végpontot a TestResourceGroup erőforráscsoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ca668-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="ca668-112">2. példa: Az összes magánjellegű végpont felsorolása az ResourceGroupban</span><span class="sxs-lookup"><span data-stu-id="ca668-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="ca668-113">Ez a parancs a TestResourceGroup erőforráscsoport összes magánjellegű végpontja</span><span class="sxs-lookup"><span data-stu-id="ca668-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ca668-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca668-114">PARAMETERS</span></span>

### <span data-ttu-id="ca668-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca668-115">-DefaultProfile</span></span>
<span data-ttu-id="ca668-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca668-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca668-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ca668-117">-ExpandResource</span></span>
<span data-ttu-id="ca668-118">A kibontani szükséges erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="ca668-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ca668-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ca668-119">-Name</span></span>
<span data-ttu-id="ca668-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ca668-120">The resource name.</span></span>

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

### <span data-ttu-id="ca668-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca668-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca668-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca668-122">The resource group name.</span></span>

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

### <span data-ttu-id="ca668-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca668-123">CommonParameters</span></span>
<span data-ttu-id="ca668-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca668-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca668-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca668-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca668-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca668-126">INPUTS</span></span>

### <span data-ttu-id="ca668-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ca668-127">System.String</span></span>

## <span data-ttu-id="ca668-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca668-128">OUTPUTS</span></span>

### <span data-ttu-id="ca668-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ca668-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ca668-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca668-130">NOTES</span></span>

## <span data-ttu-id="ca668-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca668-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca668-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca668-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="ca668-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca668-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)