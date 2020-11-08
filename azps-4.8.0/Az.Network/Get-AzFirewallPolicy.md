---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184142"
---
# <span data-ttu-id="6263c-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6263c-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="6263c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6263c-102">SYNOPSIS</span></span>
<span data-ttu-id="6263c-103">Azure tűzfal-házirendet kap</span><span class="sxs-lookup"><span data-stu-id="6263c-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="6263c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6263c-104">SYNTAX</span></span>

### <span data-ttu-id="6263c-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6263c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6263c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6263c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6263c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6263c-107">DESCRIPTION</span></span>
<span data-ttu-id="6263c-108">A **Get-AzFirewallPolicy** parancsmag egy vagy több tűzfalat kap egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="6263c-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="6263c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6263c-109">EXAMPLES</span></span>

### <span data-ttu-id="6263c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6263c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="6263c-111">Ez a példa beolvassa a "firewallPolicy" nevű tűzfal-házirendet az "TestRg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="6263c-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="6263c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6263c-112">PARAMETERS</span></span>

### <span data-ttu-id="6263c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6263c-113">-DefaultProfile</span></span>
<span data-ttu-id="6263c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6263c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6263c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6263c-115">-Name</span></span>
<span data-ttu-id="6263c-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6263c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6263c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6263c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6263c-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6263c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6263c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6263c-119">-ResourceId</span></span>
<span data-ttu-id="6263c-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6263c-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6263c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6263c-121">CommonParameters</span></span>
<span data-ttu-id="6263c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6263c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6263c-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6263c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6263c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6263c-124">INPUTS</span></span>

### <span data-ttu-id="6263c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6263c-125">System.String</span></span>

## <span data-ttu-id="6263c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6263c-126">OUTPUTS</span></span>

### <span data-ttu-id="6263c-127">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6263c-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="6263c-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 1.12.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6263c-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6263c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6263c-129">NOTES</span></span>

## <span data-ttu-id="6263c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6263c-130">RELATED LINKS</span></span>
