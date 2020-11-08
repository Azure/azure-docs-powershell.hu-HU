---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195591"
---
# <span data-ttu-id="9d40a-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d40a-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="9d40a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d40a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d40a-103">CustomIpPrefix-erőforrást kap</span><span class="sxs-lookup"><span data-stu-id="9d40a-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="9d40a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d40a-104">SYNTAX</span></span>

### <span data-ttu-id="9d40a-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d40a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d40a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d40a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d40a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d40a-107">DESCRIPTION</span></span>
<span data-ttu-id="9d40a-108">A **Get-AzCustomIpPrefix** parancsmag egy vagy több CustomIpPrefixes kap, amely a bemeneti paraméterek halmazát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d40a-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="9d40a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9d40a-109">EXAMPLES</span></span>

### <span data-ttu-id="9d40a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9d40a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="9d40a-111">Ez a parancs egy myCustomIpPrefix nevű CustomIpPrefix-erőforrást kap az erőforráscsoport myRg</span><span class="sxs-lookup"><span data-stu-id="9d40a-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="9d40a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d40a-112">PARAMETERS</span></span>

### <span data-ttu-id="9d40a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d40a-113">-DefaultProfile</span></span>
<span data-ttu-id="9d40a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d40a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d40a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d40a-115">-Name</span></span>
<span data-ttu-id="9d40a-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9d40a-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d40a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d40a-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d40a-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d40a-119">-ResourceId</span></span>
<span data-ttu-id="9d40a-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9d40a-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d40a-121">CommonParameters</span></span>
<span data-ttu-id="9d40a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d40a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d40a-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d40a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d40a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d40a-124">INPUTS</span></span>

### <span data-ttu-id="9d40a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9d40a-125">System.String</span></span>

## <span data-ttu-id="9d40a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d40a-126">OUTPUTS</span></span>

### <span data-ttu-id="9d40a-127">Microsoft. Azure. commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d40a-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="9d40a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d40a-128">NOTES</span></span>

## <span data-ttu-id="9d40a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d40a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d40a-130">Új – AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d40a-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="9d40a-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d40a-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="9d40a-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9d40a-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)