---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919666"
---
# <span data-ttu-id="eac3f-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac3f-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="eac3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eac3f-102">SYNOPSIS</span></span>
<span data-ttu-id="eac3f-103">Nyilvános IP-előtagot kap</span><span class="sxs-lookup"><span data-stu-id="eac3f-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="eac3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eac3f-104">SYNTAX</span></span>

### <span data-ttu-id="eac3f-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eac3f-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eac3f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac3f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eac3f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eac3f-107">DESCRIPTION</span></span>
<span data-ttu-id="eac3f-108">A **Get-AzPublicIpPrefix** parancsmag egy vagy több nyilvános IP-előtagot kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="eac3f-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="eac3f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eac3f-109">EXAMPLES</span></span>

### <span data-ttu-id="eac3f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="eac3f-110">Example 1</span></span>
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
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="eac3f-111">Ez a parancs nyilvános IP-előtagforrást kap aPublicIpPrefix1 értékével a myRg erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="eac3f-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="eac3f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="eac3f-112">Example 2</span></span>
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
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="eac3f-113">Ez a parancs az összes nyilvános IP-előtagforrást megkapja, amely a SajátPublicIpPrefix előtaggal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="eac3f-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="eac3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eac3f-114">PARAMETERS</span></span>

### <span data-ttu-id="eac3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac3f-115">-DefaultProfile</span></span>
<span data-ttu-id="eac3f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eac3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac3f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="eac3f-117">-Name</span></span>
<span data-ttu-id="eac3f-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="eac3f-118">The resource name.</span></span>

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

### <span data-ttu-id="eac3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac3f-119">-ResourceGroupName</span></span>
<span data-ttu-id="eac3f-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eac3f-120">The resource group name.</span></span>

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

### <span data-ttu-id="eac3f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac3f-121">-ResourceId</span></span>
<span data-ttu-id="eac3f-122">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eac3f-122">The resource Id.</span></span>

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

### <span data-ttu-id="eac3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac3f-123">CommonParameters</span></span>
<span data-ttu-id="eac3f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac3f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eac3f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac3f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eac3f-126">INPUTS</span></span>

### <span data-ttu-id="eac3f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eac3f-127">System.String</span></span>

## <span data-ttu-id="eac3f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac3f-128">OUTPUTS</span></span>

### <span data-ttu-id="eac3f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac3f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="eac3f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eac3f-130">NOTES</span></span>

## <span data-ttu-id="eac3f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eac3f-131">RELATED LINKS</span></span>

[<span data-ttu-id="eac3f-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac3f-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="eac3f-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac3f-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="eac3f-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac3f-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
