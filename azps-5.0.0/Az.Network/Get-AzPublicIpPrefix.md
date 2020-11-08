---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195410"
---
# <span data-ttu-id="fc8d3-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fc8d3-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="fc8d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8d3-103">Nyilvános IP-előtagot kap</span><span class="sxs-lookup"><span data-stu-id="fc8d3-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="fc8d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc8d3-104">SYNTAX</span></span>

### <span data-ttu-id="fc8d3-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc8d3-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc8d3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc8d3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc8d3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc8d3-107">DESCRIPTION</span></span>
<span data-ttu-id="fc8d3-108">A **Get-AzPublicIpPrefix** parancsmag egy vagy több nyilvános IP-előtagokat kap egy erőforráscsoport esetében.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="fc8d3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fc8d3-109">EXAMPLES</span></span>

### <span data-ttu-id="fc8d3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc8d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="fc8d3-111">Ez a parancs nyilvános IP-előtag-erőforrást kap a myPublicIpPrefix1 az erőforráscsoport myRg</span><span class="sxs-lookup"><span data-stu-id="fc8d3-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="fc8d3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fc8d3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="fc8d3-113">Ez a parancs beilleszti az összes nyilvános IP-előtagot, amely a myPublicIpPrefix kezdődik.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="fc8d3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc8d3-114">PARAMETERS</span></span>

### <span data-ttu-id="fc8d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8d3-115">-DefaultProfile</span></span>
<span data-ttu-id="fc8d3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc8d3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc8d3-117">-Name</span></span>
<span data-ttu-id="fc8d3-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fc8d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc8d3-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fc8d3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc8d3-121">-ResourceId</span></span>
<span data-ttu-id="fc8d3-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-122">The resource Id.</span></span>

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

### <span data-ttu-id="fc8d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8d3-123">CommonParameters</span></span>
<span data-ttu-id="fc8d3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc8d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8d3-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc8d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8d3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc8d3-126">INPUTS</span></span>

### <span data-ttu-id="fc8d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8d3-127">System.String</span></span>

## <span data-ttu-id="fc8d3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc8d3-128">OUTPUTS</span></span>

### <span data-ttu-id="fc8d3-129">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fc8d3-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fc8d3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc8d3-130">NOTES</span></span>

## <span data-ttu-id="fc8d3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc8d3-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc8d3-132">Új – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fc8d3-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="fc8d3-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fc8d3-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="fc8d3-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fc8d3-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
