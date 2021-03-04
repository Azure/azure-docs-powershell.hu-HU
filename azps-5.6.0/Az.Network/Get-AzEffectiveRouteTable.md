---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926570"
---
# <span data-ttu-id="aecdd-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="aecdd-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="aecdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aecdd-102">SYNOPSIS</span></span>
<span data-ttu-id="aecdd-103">A hálózati felület hatékony útvonaltábláját használja.</span><span class="sxs-lookup"><span data-stu-id="aecdd-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="aecdd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aecdd-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aecdd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aecdd-105">DESCRIPTION</span></span>
<span data-ttu-id="aecdd-106">A **Get-AzEffectiveRouteTable** parancsmag a hálózati felületen alkalmazott tényleges útvonaltáblát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="aecdd-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="aecdd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aecdd-107">EXAMPLES</span></span>

### <span data-ttu-id="aecdd-108">1. példa: A hatékony útvonaltábla lekérte egy hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="aecdd-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="aecdd-109">Ez a parancs a MyResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati felületével társított hatékony útvonaltáblát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aecdd-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="aecdd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aecdd-110">PARAMETERS</span></span>

### <span data-ttu-id="aecdd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aecdd-111">-AsJob</span></span>
<span data-ttu-id="aecdd-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aecdd-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecdd-113">-DefaultProfile</span></span>
<span data-ttu-id="aecdd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aecdd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aecdd-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="aecdd-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="aecdd-116">A hálózati felület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aecdd-116">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aecdd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecdd-117">-ResourceGroupName</span></span>
<span data-ttu-id="aecdd-118">Egy hálózati felület erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aecdd-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aecdd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecdd-119">CommonParameters</span></span>
<span data-ttu-id="aecdd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aecdd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecdd-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aecdd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecdd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aecdd-122">INPUTS</span></span>

### <span data-ttu-id="aecdd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="aecdd-123">System.String</span></span>

## <span data-ttu-id="aecdd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aecdd-124">OUTPUTS</span></span>

### <span data-ttu-id="aecdd-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="aecdd-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="aecdd-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aecdd-126">NOTES</span></span>

## <span data-ttu-id="aecdd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aecdd-127">RELATED LINKS</span></span>

[<span data-ttu-id="aecdd-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aecdd-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


