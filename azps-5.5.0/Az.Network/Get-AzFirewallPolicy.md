---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161098"
---
# <span data-ttu-id="3f547-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3f547-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="3f547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f547-102">SYNOPSIS</span></span>
<span data-ttu-id="3f547-103">Azure tűzfal-házirendet kap</span><span class="sxs-lookup"><span data-stu-id="3f547-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="3f547-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f547-104">SYNTAX</span></span>

### <span data-ttu-id="3f547-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f547-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f547-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f547-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f547-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f547-107">DESCRIPTION</span></span>
<span data-ttu-id="3f547-108">A **Get-AzFirewallPolicy** parancsmag egy vagy több tűzfalat kap egy erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="3f547-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="3f547-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f547-109">EXAMPLES</span></span>

### <span data-ttu-id="3f547-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f547-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="3f547-111">Ebben a példában egy "firewallPolicy" nevű tűzfal-házirendet talál a "TestRg" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="3f547-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="3f547-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f547-112">PARAMETERS</span></span>

### <span data-ttu-id="3f547-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f547-113">-DefaultProfile</span></span>
<span data-ttu-id="3f547-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f547-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f547-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3f547-115">-Name</span></span>
<span data-ttu-id="3f547-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3f547-116">The resource name.</span></span>

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

### <span data-ttu-id="3f547-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f547-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f547-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f547-118">The resource group name.</span></span>

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

### <span data-ttu-id="3f547-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f547-119">-ResourceId</span></span>
<span data-ttu-id="3f547-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3f547-120">The resource Id.</span></span>

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

### <span data-ttu-id="3f547-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f547-121">CommonParameters</span></span>
<span data-ttu-id="3f547-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f547-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f547-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f547-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f547-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f547-124">INPUTS</span></span>

### <span data-ttu-id="3f547-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3f547-125">System.String</span></span>

## <span data-ttu-id="3f547-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f547-126">OUTPUTS</span></span>

### <span data-ttu-id="3f547-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3f547-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="3f547-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3f547-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f547-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f547-129">NOTES</span></span>

## <span data-ttu-id="3f547-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f547-130">RELATED LINKS</span></span>
